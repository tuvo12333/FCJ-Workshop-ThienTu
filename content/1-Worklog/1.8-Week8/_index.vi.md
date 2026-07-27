---
title: "Worklog Tuần 8"
date: 2026
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---


### Mục tiêu tuần 8:

* Nâng cao khả năng quản lý quyền truy cập AWS bằng cách áp dụng Permission Boundary để kiểm soát quyền của delegated administrator.
* Thực hành Infrastructure as Code (IaC) với AWS CDK nhằm tự động hóa việc xây dựng hạ tầng thay vì cấu hình thủ công trên Console.
* Tìm hiểu quy trình chuyển đổi và di chuyển cơ sở dữ liệu bằng AWS DMS để hạn chế thời gian gián đoạn dịch vụ.
* Xây dựng cơ chế kiểm soát truy cập IAM Role dựa trên các điều kiện môi trường và giới hạn thực tế của hệ thống.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Áp dụng IAM Permission Boundary để kiểm soát quyền người dùng.<br> - Xây dựng cơ chế phân quyền giới hạn cho các tài khoản quản trị và developer nhằm ngăn chặn việc cấp quyền vượt quá phạm vi cho phép và hạn chế truy cập tài nguyên nhạy cảm như RDS. | 18/05/2026 | 18/05/2026      | <https://000030.awsstudygroup.com/> |
| 2   | - Triển khai hạ tầng AWS bằng AWS CDK.<br> - Sử dụng TypeScript CDK để định nghĩa VPC, EC2 public subnet, RDS MariaDB private subnet, Security Group và UserData để khởi tạo dữ liệu ban đầu cho database.<br> | 19/05/2026 | 19/05/2026      | <https://000038.awsstudygroup.com/> |
| 3   | - Thực hiện quá trình chuyển đổi cấu trúc và di chuyển database.<br> - Di chuyển cơ sở dữ liệu của ứng dụng web từ RDS MySQL sang RDS MariaDB bằng AWS DMS với cấu hình endpoint, Full Load và Change Data Capture (CDC). | 20/05/2026 | 20/05/2026      | <https://000043.awsstudygroup.com/> |
| 4   | - Kiểm tra IAM Role với Condition Policy.<br> - Điều chỉnh điều kiện truy cập từ giới hạn theo địa chỉ IP sang điều kiện aws:RequestedRegion do môi trường mạng sử dụng IP thay đổi, sau đó kiểm tra quyền truy cập tại các Region khác nhau.<br> | 21/05/2026 | 21/05/2026      | <https://000044.awsstudygroup.com/> |


### Kết quả đạt được tuần 8:

* Tổng quan:

Trong tuần này, tôi tập trung vào các nội dung nâng cao liên quan đến IAM governance, Infrastructure as Code với AWS CDK, database migration và kiểm soát truy cập theo điều kiện. Nội dung được tổng hợp từ các worklog hằng ngày và biên soạn lại thành báo cáo tổng kết theo tuần.

* Kiến thức đã học:

- Hiểu cách sử dụng Permission Boundary để giới hạn quyền tối đa của delegated administrator và kiểm soát việc cấp quyền trong AWS.
- Nắm được phương pháp xây dựng hạ tầng full-stack bằng AWS CDK thay vì triển khai thủ công qua Console hoặc các file cấu hình dài.
- Hiểu quy trình di chuyển database bằng AWS DMS nhằm giảm thiểu downtime trong quá trình chuyển đổi hệ thống.
- Biết cách thiết kế IAM Role Condition dựa trên các yếu tố thực tế như Region, Network và môi trường triển khai.

* Thực hành:

- Hiểu rõ Permission Boundary đóng vai trò là giới hạn quyền cao nhất, không phải là một chính sách cấp quyền truy cập thông thường.
- Triển khai thành công hạ tầng bằng AWS CDK và thiết lập kết nối an toàn giữa Application Layer và Database Layer.
- Thực hành database migration giữa các hệ quản trị khác nhau và điều chỉnh IAM Condition phù hợp với các yêu cầu thực tế của môi trường.
