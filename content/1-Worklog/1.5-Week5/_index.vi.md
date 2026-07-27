---
title: "Worklog Tuần 5"
date: 2026
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Mục tiêu tuần 5:

* Tìm hiểu các dịch vụ hỗ trợ giám sát và nâng cao bảo mật hệ thống với AWS Security Hub và AWS Config.
* Nắm được quy trình triển khai ứng dụng container theo kiến trúc microservices trên Amazon ECS và AWS Fargate.
* Hiểu sự khác biệt giữa VPC Peering và Transit Gateway trong việc kết nối nhiều VPC.
* Thực hành xây dựng quy trình tự động tối ưu chi phí dựa trên sự kiện bằng CloudWatch, SNS và Lambda.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Tìm hiểu AWS Security Hub và AWS Config.<br> - Kích hoạt Security Hub CSPM, khám phá các tiêu chuẩn AWS Foundational Security Best Practices, CIS Benchmark và PCI DSS để đánh giá mức độ bảo mật của môi trường AWS. | 04/05/2026 | 04/05/2026 | <https://000018.awsstudygroup.com/> |
| 2   | - Nghiên cứu mô hình triển khai ứng dụng bằng Amazon ECS. <br> - Thực hành đóng gói ứng dụng với Docker, lưu trữ image trên Amazon ECR, triển khai Fargate Task, cấu hình Task Definition, Private Subnet, NAT Gateway và tách biệt các service.<br> | 05/05/2026 | 05/05/2026 | <https://000016.awsstudygroup.com/><https://000067.awsstudygroup.com/> |
| 3   | - Thực hành cấu hình VPC Peering. <br> - Tạo hai VPC với CIDR không trùng lặp, cấu hình Route Table và Security Group, kiểm tra khả năng kết nối nội bộ và đánh giá các hạn chế của VPC Peering. | 06/05/2026 | 06/05/2026 | <https://000019.awsstudygroup.com/> |
| 4   | - Xây dựng mô hình mạng Hub-and-Spoke bằng Transit Gateway.<br> - Kết nối bốn VPC thông qua Transit Gateway Attachment, khắc phục lỗi thiếu Route Propagation, kiểm thử kết nối giữa các VPC và dọn dẹp Transit Gateway sau khi hoàn thành để tối ưu chi phí.<br> | 06/05/2026 | 06/05/2026 | <https://000020.awsstudygroup.com/> |\
| 5   | - Xây dựng quy trình tự động tối ưu chi phí EC2 bằng AWS Lambda.<br> - Sử dụng VPC Flow Logs, CloudWatch Metric Filter, CloudWatch Alarm, SNS và Lambda (boto3) để tự động dừng EC2 khi phát hiện lưu lượng ICMP.<br> | 07/05/2026 | 08/05/2026 | <https://000022.awsstudygroup.com/><https://000074.awsstudygroup.com/> |

### Kết quả đạt được tuần 5:

* Tổng quan:

Trong tuần này, tôi tập trung vào việc tăng cường bảo mật hệ thống, triển khai ứng dụng container và xây dựng mô hình kết nối mạng giữa nhiều VPC. Nội dung dưới đây được tổng hợp từ các worklog hằng ngày và biên soạn lại thành báo cáo tổng kết theo tuần.

* Kiến thức đã học:

- Hiểu cách sử dụng AWS Security Hub và AWS Config để giám sát và đánh giá trạng thái bảo mật của hạ tầng AWS.
- Nắm được quy trình triển khai ứng dụng container theo kiến trúc microservices với Amazon ECS và AWS Fargate.
- Hiểu rõ ưu điểm, hạn chế và trường hợp sử dụng của VPC Peering và Transit Gateway.
- Tìm hiểu cách xây dựng quy trình tự động hóa theo sự kiện nhằm giám sát và tối ưu chi phí vận hành.

* Thực hành:

- Triển khai và kết hợp các dịch vụ bảo mật, container, networking và automation trong cùng một môi trường thực hành.
- Thực hành cấu hình VPC Peering và Transit Gateway để kết nối các VPC theo nhiều mô hình khác nhau.
- Xây dựng thành công luồng tự động từ việc thu thập log, phát hiện sự kiện đến kích hoạt AWS Lambda để thực hiện hành động xử lý.
