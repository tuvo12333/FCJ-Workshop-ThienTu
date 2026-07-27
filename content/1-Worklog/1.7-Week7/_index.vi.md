---
title: "Worklog Tuần 7"
date: 2026
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---


### Mục tiêu tuần 7:

* Tìm hiểu cách triển khai hạ tầng tự động bằng CloudFormation.
* Khai thác và phân tích dữ liệu chi phí bằng Amazon S3, AWS Glue và Amazon Athena.
* Tìm hiểu sự khác nhau giữa Savings Plans, Reserved Instances và Reserved DB Instances.
* Triển khai Amazon FSx for Windows File Server tích hợp với Microsoft Active Directory.
* Thiết lập AWS WAF để bảo vệ ứng dụng web phía trước Application Load Balancer.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Tìm hiểu triển khai hạ tầng web application và RDS bằng CloudFormation. <br> - Xây dựng template tạo VPC, public subnet, IGW, route table, EC2, RDS, security group và script khởi tạo hạ tầng tự động. | 13/05/2026 | 13/05/2026      | <https://000037.awsstudygroup.com/> |
| 2   | - Phân tích dữ liệu chi phí và mức sử dụng với AWS Glue và Athena.<br> - Tạo S3 bucket chứa dữ liệu và kết quả truy vấn, cấu hình Glue crawler, Data Catalog và thực hiện truy vấn Athena trên dữ liệu CUR.<br> | 14/05/2026 | 14/05/2026      | <https://000040.awsstudygroup.com/> |
| 3   | - Nghiên cứu Savings Plans, Reserved Instances và Reserved DB Instances.<br> - So sánh phạm vi áp dụng, phương thức thanh toán, mức chiết khấu, rủi ro khi cam kết và cách xem recommendation. | 15/05/2026 | 15/05/2026      | <https://000042.awsstudygroup.com/> |
| 4   | - Triển khai Amazon FSx for Windows File Server.<br> - Kết nối FSx với Microsoft Active Directory, kiểm tra truy cập SMB từ Linux EC2 bằng cifs-utils/samba-client và xác minh khả năng đồng bộ dữ liệu giữa các node.<br> | 16/05/2026 | 16/05/2026      | <https://000025.awsstudygroup.com/> |
| 5   | - Cấu hình AWS WAF để bảo vệ web application. <br> - Đặt WAF phía trước ALB, kết nối ALB với EC2 application và RDS database, sau đó kiểm tra khả năng lọc lưu lượng và bảo vệ ứng dụng. | 17/05/2026 | 17/05/2026      | <https://000026.awsstudygroup.com/> |

### Kết quả đạt được tuần 7:

* **Tổng quan:**

Trong tuần này, tôi tập trung nghiên cứu về CloudFormation, phân tích dữ liệu chi phí trên AWS, các hình thức cam kết tài nguyên, Amazon FSx và AWS WAF. Toàn bộ nội dung được tổng hợp từ worklog hằng ngày và chỉnh sửa thành báo cáo theo tuần.

* **Kiến thức đã học:**

- Hiểu cách tự động hóa việc triển khai hạ tầng bằng AWS CloudFormation.
- Nắm được quy trình thu thập và phân tích dữ liệu chi phí với Amazon S3, AWS Glue và Amazon Athena.
- Phân biệt đặc điểm của Savings Plans, Reserved Instances và Reserved DB Instances.
- Tìm hiểu quy trình triển khai Amazon FSx for Windows File Server tích hợp Microsoft Active Directory.
- Hiểu cách cấu hình AWS WAF để tăng cường bảo mật cho ứng dụng web thông qua ALB.

* **Thực hành:**

- Thực hiện triển khai hạ tầng bằng CloudFormation template thay cho cấu hình thủ công.
- Thực hành lưu trữ, lập Data Catalog và truy vấn dữ liệu chi phí bằng mô hình serverless trên AWS.
- Triển khai Amazon FSx và cấu hình AWS WAF nhằm nâng cao khả năng lưu trữ và bảo vệ web application.

