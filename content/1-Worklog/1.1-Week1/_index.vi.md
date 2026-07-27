---
title: "Worklog Tuần 1"
date: 2026
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---


### Mục tiêu tuần 1:

* Hiểu rõ lộ trình thực tập tổng thể và cách các dịch vụ AWS đóng vai trò cốt lõi trong việc xây dựng hệ thống thực tế.

- Xây dựng cơ chế bảo mật truy cập thông qua IAM (User, Group, Policy, Role) và cấp quyền quản lý chi phí (Billing).

- Thiết lập hạ tầng mạng đám mây cơ bản bao gồm VPC, các subnet (public/private), bảng định tuyến (route table), nhóm bảo mật (security group) và VPC endpoint.

- Cấu hình, khởi tạo máy chủ ảo EC2 và thực hành đưa ứng dụng cơ bản lên cả môi trường Linux lẫn Windows.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | -Tìm hiểu các thành phần cốt lõi của IAM: root account, account ID, group, policy, role và nguyên tắc cấp quyền tối thiểu.<br>- Thực hành tạo user/group quản trị, thiết lập Admin role, tạo tài khoản OperatorUser và test tính năng Switch Role.                                                                                        | 22/04/2026   | 22/04/2026      | <https://000002.awsstudygroup.com/> |
| 2   | - Nghiên cứu kiến trúc Amazon VPC và workshop AWS Site-to-Site VPN.<br>- Thực hành thiết kế hạ tầng mạng với subnet (public/private), internet gateway, route table, kết nối qua bastion host và thiết lập VPC endpoint để dùng các dịch vụ nội bộ.<br>                                                                                      | 23/04/2026   | 23/04/2026      | <https://000003.awsstudygroup.com/> |
| 3   | - Làm quen với dịch vụ Amazon EC2. <br> - Tiến hành dựng VPC, chạy các instance EC2 (Linux/Windows), cấu hình security group, cài đặt stack LAMP/Node.js và triển khai ứng dụng CRUD lên server. | 24/04/2026   | 24/04/2026      | <https://000004.awsstudygroup.com/> |
| 4   | -Thực hành troubleshooting (xử lý lỗi) kết nối máy chủ và quản lý tài nguyên. <br>- Khắc phục sự cố timeout bằng cách kiểm tra Security Group cùng tường lửa OS, sau đó xóa tài nguyên (terminate EC2/VPC) để đảm bảo tối ưu chi phí.<br>                  | 24/04/2026   | 24/04/2026      | <https://000004.awsstudygroup.com/> |


### Kết quả đạt được tuần 1:

*Tổng quan:

Trong tuần đầu tiên, tôi đã dành thời gian để làm quen với hệ sinh thái AWS, trọng tâm là các dịch vụ IAM, VPC và EC2. Các nội dung này được tôi đúc kết từ nhật ký công việc (worklog) hằng ngày và hệ thống lại thành định dạng báo cáo tuần.

* Kiến thức đã học:

- Nắm bắt được bức tranh toàn cảnh về kỳ thực tập và ứng dụng thực tiễn của các dịch vụ AWS.
- Biết cách quản lý phân quyền và bảo mật tài khoản qua các thành phần của IAM.
- Hiểu nguyên lý hoạt động và cách cấu hình mạng nội bộ trên nền tảng đám mây với Amazon VPC.
- Nắm vững quy trình tạo lập, vận hành máy chủ EC2 và đưa ứng dụng cơ bản lên môi trường thực.

* Thực hành:

- Triển khai thành công môi trường quản lý AWS an toàn, loại bỏ thói quen sử dụng trực tiếp tài khoản root.
- Vận dụng nhuần nhuyễn sự phối hợp giữa định tuyến VPC, security group, điểm truy cập bastion và VPC endpoint.
- Khởi tạo thành thạo các máy chủ EC2 và setup thành công môi trường chạy ứng dụng.
- Hình thành kỹ năng phát hiện, xử lý lỗi hệ thống và rèn luyện thói quen dọn dẹp tài nguyên đúng cách để tránh lãng phí.




