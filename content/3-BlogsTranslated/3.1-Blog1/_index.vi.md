---
title: "Blog 1"
date: 2026
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Hiện đại hóa KYC với các giải pháp serverless của AWS và AI agent cho dịch vụ tài chính

Trong bối cảnh ngành tài chính yêu cầu tốc độ xử lý nhanh và tính bảo mật khắt khe, quy trình KYC truyền thống thường gặp trở ngại do thao tác thủ công, thời gian chờ đợi kéo dài và khả năng sai sót cao. Bài viết này trình bày cách các tổ chức tài chính có thể chuyển đổi quy trình này bằng kiến trúc Serverless kết hợp với AI Agents.


## Vai trò quan trọng của KYC

- Bảo vệ hệ thống tài chính: KYC thực hiện xác minh danh tính khách hàng và phát hiện gian lận để bảo vệ sự an toàn của hệ thống.

- Hỗ trợ tuân thủ quy định pháp lý: KYC đóng vai trò then chốt trong việc tuân thủ các quy định về chống rửa tiền (AML) và chống tài trợ khủng bố (CTF).

- Ngăn chặn gian lận: Quy trình này giúp phát hiện và ngăn chặn các hành vi đánh cắp danh tính cũng như sử dụng tài liệu giả mạo.

- Quản lý rủi ro: KYC hỗ trợ đánh giá hồ sơ khách hàng và giám sát các giao dịch tài chính để kiểm soát rủi ro.

- Xây dựng lòng tin: Việc thực hiện KYC tạo ra sự minh bạch, từ đó củng cố lòng tin của khách hàng đối với tổ chức tài chính.

- Sự phức tạp khi mở rộng: Việc tuân thủ KYC ngày càng trở nên khó khăn khi các tổ chức tài chính mở rộng sang nhiều sản phẩm, phân khúc khách hàng (bán lẻ, SME, doanh nghiệp) và khu vực địa lý khác nhau.

- Yêu cầu về khuôn khổ pháp lý: Hoạt động trên nhiều khu vực đòi hỏi phải tuân thủ các khuôn khổ quy định đa dạng như BSA, Đạo luật USA PATRIOT (Hoa Kỳ), AMLD (EU), cũng như các hướng dẫn từ FATF và MAS (Singapore).

## KYC truyền thống 

Các quy trình KYC truyền thống xác minh danh tính khách hàng, đánh giá rủi ro và giám sát rửa tiền. Chúng dựa vào việc thu thập tài liệu thủ công, kiểm tra danh tính trên nhiều cơ sở dữ liệu và đánh giá định kỳ. 
Mặc dù các quy trình đã được thiết lập này đã phục vụ ngành tài chính trong nhiều thập kỷ, nhưng chúng được thiết kế cho một kỷ nguyên khác với khối lượng giao dịch thấp hơn, các sản phẩm đơn giản hơn và bối cảnh mối đe dọa ít tinh vi hơn. Môi trường tài chính ưu tiên kỹ thuật số ngày nay đòi hỏi một sự tái hình dung cơ bản về KYC ở quy mô lớn.

## Kiến trúc giải pháp KYC gốc đám mây sử dụng AI tác nhân

![Kiến trúc tác nhân cấp cao cho KYC theo thời gian thực](/images/3-BlogsTranslated/kientruc.png)

## The pub/sub hub

Việc sử dụng kiến trúc **hub-and-spoke** (hay message broker) hoạt động tốt với một số lượng nhỏ các microservices liên quan chặt chẽ.  
- Mỗi microservice chỉ phụ thuộc vào *hub*  
- Kết nối giữa các microservice chỉ giới hạn ở nội dung của message được xuất  
- Giảm số lượng synchronous calls vì pub/sub là *push* không đồng bộ một chiều

Nhược điểm: cần **phối hợp và giám sát** để tránh microservice xử lý nhầm message.

---

## Core microservice

Cung cấp dữ liệu nền tảng và lớp truyền thông, gồm:  
- **Amazon S3** bucket cho dữ liệu  
- **Amazon DynamoDB** cho danh mục dữ liệu  
- **AWS Lambda** để ghi message vào data lake và danh mục  
- **Amazon SNS** topic làm *hub*  
- **Amazon S3** bucket cho artifacts như mã Lambda

> Chỉ cho phép truy cập ghi gián tiếp vào data lake qua hàm Lambda → đảm bảo nhất quán.

---

## Front door microservice

- Cung cấp API Gateway để tương tác REST bên ngoài  
- Xác thực & ủy quyền dựa trên **OIDC** thông qua **Amazon Cognito**  
- Cơ chế *deduplication* tự quản lý bằng DynamoDB thay vì SNS FIFO vì:
  1. SNS deduplication TTL chỉ 5 phút
  2. SNS FIFO yêu cầu SQS FIFO
  3. Chủ động báo cho sender biết message là bản sao

---

## Staging ER7 microservice

- Lambda “trigger” đăng ký với pub/sub hub, lọc message theo attribute  
- Step Functions Express Workflow để chuyển ER7 → JSON  
- Hai Lambda:
  1. Sửa format ER7 (newline, carriage return)
  2. Parsing logic  
- Kết quả hoặc lỗi được đẩy lại vào pub/sub hub

---

## Tính năng mới trong giải pháp

### 1. AWS CloudFormation cross-stack references
Ví dụ *outputs* trong core microservice:
```yaml
Outputs:
  Bucket:
    Value: !Ref Bucket
    Export:
      Name: !Sub ${AWS::StackName}-Bucket
  ArtifactBucket:
    Value: !Ref ArtifactBucket
    Export:
      Name: !Sub ${AWS::StackName}-ArtifactBucket
  Topic:
    Value: !Ref Topic
    Export:
      Name: !Sub ${AWS::StackName}-Topic
  Catalog:
    Value: !Ref Catalog
    Export:
      Name: !Sub ${AWS::StackName}-Catalog
  CatalogArn:
    Value: !GetAtt Catalog.Arn
    Export:
      Name: !Sub ${AWS::StackName}-CatalogArn

