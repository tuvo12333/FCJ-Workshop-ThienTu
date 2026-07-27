---
title: "Worklog Tuần 6"
date: 2026
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---


### Mục tiêu tuần 6:

* Tìm hiểu quy trình tự động hóa triển khai ứng dụng lên EC2 bằng AWS CodePipeline và CodeDeploy.
* Nắm được cách kiểm soát quyền truy cập EC2 thông qua IAM Policy kết hợp với điều kiện dựa trên tag.
* Thực hành triển khai Grafana và tích hợp với Amazon CloudWatch để giám sát tài nguyên.
* Khám phá AWS Systems Manager trong việc quản lý tập trung EC2 và thu thập memory metrics phục vụ tối ưu hóa tài nguyên.
* Tìm hiểu cơ chế mã hóa dữ liệu và giám sát truy cập S3 bằng AWS KMS, CloudTrail và Amazon Athena.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Triển khai quy trình CI/CD cho ứng dụng trên EC2 bằng AWS CodePipeline. <br> - Tích hợp GitHub, CodePipeline, S3 Artifact, CodeDeploy, AppSpec hooks, PM2 deployment script và CodeDeploy Agent trên EC2. | 08/05/2026 | 08/05/2026 | <https://000017.awsstudygroup.com/><https://000023.awsstudygroup.com/> |
| 2   | - Thực hành quản lý quyền truy cập EC2 bằng IAM kết hợp với tag.<br> - Xây dựng IAM Policy yêu cầu tag Environment=Test khi tạo EC2 và chỉ cho phép Start, Stop hoặc Terminate đối với các instance đáp ứng điều kiện tag.<br> | 09/05/2026 | 09/05/2026 | <https://000028.awsstudygroup.com/> |
| 3   | - Triển khai Grafana trên EC2 và tích hợp với Amazon CloudWatch.<br> - Cấu hình VPC, Security Group, EC2, mở cổng 3000, gắn IAM Role và trực quan hóa chỉ số CPUUtilization trên Grafana Dashboard. | 10/05/2026 | 10/05/2026 | <https://000029.awsstudygroup.com/> |
| 4   | - Quản lý EC2 bằng AWS Systems Manager. <br> - Gắn IAM Role AmazonSSMManagedInstanceCore, xử lý lỗi Managed Nodes ở trạng thái Offline và thực thi lệnh đồng thời trên nhiều EC2 instance. <br> | 10/05/2026 | 10/05/2026 | <https://000031.awsstudygroup.com/> |
| 5   | - Thu thập memory metrics để tối ưu cấu hình EC2 bằng CloudWatch Agent. <br> - Cài đặt CloudWatch Agent, thu thập dữ liệu RAM và chuẩn bị dữ liệu phục vụ Compute Optimizer và Cost Explorer. | 11/05/2026 | 11/05/2026 | <https://000032.awsstudygroup.com/> |
| 6   | - Thực hành mã hóa dữ liệu bằng AWS KMS và giám sát truy cập S3. <br> - Sử dụng CloudTrail Data Events kết hợp với Athena SQL để phân tích lịch sử truy cập và xác minh cơ chế từ chối giải mã (Decrypt) khi không đủ quyền KMS. | 12/05/2026 | 12/05/2026 | <https://000033.awsstudygroup.com/> |

### Kết quả đạt được tuần 6:

* Tổng quan:

Trong tuần này, tôi tập trung vào việc tự động hóa quy trình triển khai ứng dụng, tăng cường quản trị quyền truy cập, giám sát hệ thống và bảo vệ dữ liệu trên AWS. Nội dung dưới đây được tổng hợp từ các worklog hằng ngày và biên soạn lại thành báo cáo tổng kết theo tuần.

* Kiến thức đã học:

- Hiểu quy trình xây dựng CI/CD trên AWS bằng CodePipeline và CodeDeploy để tự động hóa triển khai ứng dụng.
- Nắm được cách kiểm soát quyền thao tác EC2 thông qua IAM Policy và điều kiện dựa trên tag.
- Biết cách triển khai Grafana và tích hợp với CloudWatch để trực quan hóa các chỉ số giám sát.
- Tìm hiểu AWS Systems Manager trong việc quản lý tập trung EC2 và thu thập memory metrics phục vụ tối ưu tài nguyên.
- Hiểu cơ chế mã hóa dữ liệu bằng AWS KMS cũng như phương pháp theo dõi truy cập S3 bằng CloudTrail và Athena.

* Thực hành:

- Xây dựng thành công quy trình CI/CD và xử lý các sự cố phổ biến liên quan đến CodeDeploy, IAM và AppSpec.
- Áp dụng IAM Policy, tag và KMS để tăng cường quản trị và bảo vệ tài nguyên AWS.
- Triển khai Grafana, CloudWatch Agent và AWS Systems Manager nhằm nâng cao khả năng giám sát và vận hành hệ thống.
