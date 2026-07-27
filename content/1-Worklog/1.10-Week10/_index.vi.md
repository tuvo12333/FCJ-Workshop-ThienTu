---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---


## Mục tiêu tuần 10

Trong tuần 10, mục tiêu chính là tìm hiểu nhóm nội dung về **tối ưu chi phí và nâng cao bảo mật hệ thống** trên AWS. Đây là một phần trong giai đoạn **Optimize / Tối ưu hệ thống** của AWS Cloud Journey, tập trung vào việc cải thiện hiệu suất vận hành, tăng cường bảo mật, kiểm soát chi phí và quản lý hệ thống sau khi triển khai trên AWS.

Các nội dung chính trong tuần bao gồm:

* Tìm hiểu tổng quan về chiến lược tối ưu chi phí trên AWS.
* Khám phá **AWS Budgets** để tạo ngân sách và thiết lập cảnh báo chi phí.
* Tìm hiểu **AWS Cost Explorer** để phân tích mức sử dụng dịch vụ và chi phí AWS.
* Nghiên cứu **AWS KMS** trong việc quản lý khóa mã hóa và bảo vệ dữ liệu.
* Tìm hiểu **AWS WAF** nhằm bảo vệ ứng dụng web và API khỏi các mối đe dọa phổ biến.
* Khám phá **AWS Security Hub** để đánh giá trạng thái bảo mật và các tiêu chuẩn tuân thủ.
* Ghi chú các phương pháp thực hành tốt nhất về bảo mật và quản lý chi phí trên AWS.

---

## Các công việc cần triển khai trong tuần này

| Thứ | Công việc                                                                                                                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| --- | --- | --- | --- | --- |
| **1** | Tìm hiểu tổng quan về nhóm Optimize trong AWS Cloud Journey, bao gồm tối ưu chi phí, bảo mật, độ tin cậy, hiệu suất và quản lý vận hành hệ thống. | 26/05/2026 | 26/05/2026 | [https://cloudjourney.awsstudygroup.com/3-optimize/](https://cloudjourney.awsstudygroup.com/3-optimize/) |
| **2** | Tìm hiểu AWS Budgets và AWS Cost Explorer, bao gồm cách tạo ngân sách, theo dõi chi phí, phân tích chi phí theo dịch vụ và thiết lập cảnh báo khi vượt quá giới hạn cho phép. | 27/05/2026 | 27/05/2026 | [https://000001.awsstudygroup.com/7-monitoring-v%C3%A0-t%E1%BB%91i-%C6%B0u-chi-ph%C3%AD/](https://000001.awsstudygroup.com/7-monitoring-v%C3%A0-t%E1%BB%91i-%C6%B0u-chi-ph%C3%AD/) <br> [https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html) <br> [https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html) |
| **3** | Tìm hiểu AWS KMS và vai trò của dịch vụ quản lý khóa trong việc tạo, quản lý khóa mã hóa và bảo vệ dữ liệu trên các dịch vụ AWS. | 28/05/2026 | 28/05/2026 | [https://000033.awsstudygroup.com/](https://000033.awsstudygroup.com/) <br> [https://docs.aws.amazon.com/kms/](https://docs.aws.amazon.com/kms/) |
| **4** | Tìm hiểu AWS WAF và cách Web Application Firewall bảo vệ website, API và ứng dụng khỏi các cuộc tấn công phổ biến như SQL Injection, XSS hoặc lưu lượng bot độc hại. | 29/05/2026 | 29/05/2026 | [https://000026.awsstudygroup.com/](https://000026.awsstudygroup.com/) <br> [https://aws.amazon.com/waf/](https://aws.amazon.com/waf/) <br> [https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-control-access-aws-waf.html](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-control-access-aws-waf.html) |
| **5** | Tìm hiểu AWS Security Hub và tổng hợp kiến thức về bảo mật, tối ưu chi phí; ghi chú các nguyên tắc như giám sát chi phí thường xuyên, giới hạn quyền truy cập, mã hóa dữ liệu và bảo vệ ứng dụng web. | 30/05/2026 | 30/05/2026 | [https://000018.awsstudygroup.com/](https://000018.awsstudygroup.com/) <br> [https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html](https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html) <br> [https://cloudjourney.awsstudygroup.com/3-optimize/](https://cloudjourney.awsstudygroup.com/3-optimize/) |

---

## Kết quả đạt được tuần 10

### Tổng quan

Trong tuần này, tôi tập trung tìm hiểu các dịch vụ AWS hỗ trợ **tối ưu chi phí và nâng cao bảo mật hệ thống**. Nội dung được chia thành hai nhóm chính: quản lý chi phí thông qua **AWS Budgets** và **AWS Cost Explorer**, cùng với việc tăng cường bảo mật bằng **AWS KMS**, **AWS WAF** và **AWS Security Hub**. Các dịch vụ này giúp theo dõi chi phí, bảo vệ dữ liệu quan trọng và cải thiện trạng thái bảo mật tổng thể của môi trường AWS.

### Kiến thức đã học

Sau khi hoàn thành tuần 10, tôi đã hiểu:

* Vai trò của tối ưu chi phí trong quá trình thiết kế và vận hành hệ thống trên AWS.
* Cách sử dụng **AWS Budgets** để tạo ngân sách, thiết lập ngưỡng cảnh báo và theo dõi chi phí sử dụng.
* Cách sử dụng **AWS Cost Explorer** để phân tích chi phí theo dịch vụ, thời gian, tài khoản hoặc tag tài nguyên.
* **AWS KMS** là dịch vụ quản lý khóa và mã hóa giúp bảo vệ dữ liệu được lưu trữ hoặc xử lý trên các dịch vụ AWS.
* **AWS WAF** là Web Application Firewall giúp bảo vệ website, API và ứng dụng khỏi bot, khai thác lỗ hổng và các cuộc tấn công ở tầng ứng dụng như SQL Injection hoặc Cross-site Scripting.
* **AWS Security Hub** hỗ trợ thu thập các phát hiện bảo mật và đánh giá môi trường AWS dựa trên các tiêu chuẩn bảo mật.
* Tầm quan trọng của việc kết hợp giám sát chi phí, phân quyền IAM hợp lý, mã hóa dữ liệu và bảo vệ ứng dụng bằng WAF.

---

## Thực hành

Trong quá trình học tập và thực hành, tôi đã có thể:

* Truy cập AWS Billing và Cost Management trên AWS Console.
* Kiểm tra mức sử dụng và chi phí của các dịch vụ AWS.
* Tạo AWS Budgets để theo dõi giới hạn chi phí hàng tháng.
* Cấu hình cảnh báo khi chi phí vượt quá ngưỡng được thiết lập.
* Sử dụng Cost Explorer để xem biểu đồ và phân tích chi phí dịch vụ.
* Tìm hiểu AWS KMS, Customer Managed Key và AWS Managed Key.
* Hiểu cách AWS KMS hỗ trợ mã hóa dữ liệu cho các dịch vụ như S3, EBS hoặc RDS.
* Khám phá AWS WAF, Web ACL, Rule và Managed Rule Group.
* Hiểu cách AWS WAF có thể tích hợp với CloudFront, Application Load Balancer hoặc API Gateway.
* Tìm hiểu AWS Security Hub và vai trò của Security Findings trong việc đánh giá bảo mật.
* Nhận biết các lỗi phổ biến như Cost Explorer chưa được kích hoạt, chưa tạo Budget, thiếu quyền IAM, cấu hình WAF Rule sai hoặc chưa bật mã hóa cho dữ liệu quan trọng.

---

## Tổng kết dịch vụ tuần 10

| Dịch vụ              | Mục đích chính                       | Vai trò trong hệ thống                                             |
| -------------------- | ---------------------------------- | -------------------------------------------------------------- |
| **AWS Budgets**      | Tạo ngân sách và cảnh báo chi phí     | Kiểm soát chi phí, tránh phát sinh vượt mức dự kiến                       |
| **AWS Cost Explorer**| Phân tích chi phí sử dụng AWS            | Xác định dịch vụ nào đang tiêu tốn nhiều chi phí nhất                      |
| **AWS KMS**          | Quản lý khóa và mã hóa dữ liệu       | Bảo vệ dữ liệu trong trạng thái lưu trữ và sử dụng                                |
| **AWS WAF**          | Bảo vệ website và API          | Ngăn chặn request độc hại, bot traffic, SQL Injection, XSS      |
| **AWS Security Hub** | Đánh giá trạng thái bảo mật            | Tổng hợp Security Findings và kiểm tra theo các tiêu chuẩn bảo mật |

---

## Tổng kết tuần 10

**Tuần 10:** Tìm hiểu AWS Budgets, Cost Explorer, KMS, WAF và Security Hub nhằm nâng cao khả năng tối ưu chi phí và bảo mật hệ thống AWS. Hiểu cách theo dõi chi phí, tạo cảnh báo ngân sách, phân tích mức sử dụng dịch vụ, mã hóa dữ liệu, bảo vệ ứng dụng web/API và đánh giá trạng thái bảo mật trong môi trường AWS.