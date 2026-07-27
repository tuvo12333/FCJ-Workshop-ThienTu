---
title: "Worklog Tuần 4"
date: 2026
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---


### Mục tiêu tuần 4:

* Hiểu cách thiết lập cơ chế phân giải DNS hai chiều giữa môi trường on-premises mô phỏng và AWS.
* Thực hành sử dụng AWS CLI để triển khai và quản lý các dịch vụ AWS như S3, SNS, IAM, VPC và EC2.
* Tìm hiểu quy trình xây dựng chiến lược sao lưu và khôi phục dữ liệu với AWS Backup.
* Rèn luyện kỹ năng dọn dẹp tài nguyên đúng thứ tự phụ thuộc nhằm tối ưu chi phí sử dụng AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1   | - Tìm hiểu kiến trúc Route 53 Resolver. <br> - Xây dựng môi trường on-premises mô phỏng và AWS VPC, cấu hình VPC Peering, Route Table, Inbound/Outbound Endpoint và Resolver Rules để thiết lập kết nối phân giải DNS. | 01/05/2026 | 01/05/2026 | <https://000010.awsstudygroup.com/> |
| 2   | - Thực hành quản lý tài nguyên bằng AWS CLI.<br> - Cài đặt AWS CLI v2, cấu hình thông tin xác thực, quản lý các dịch vụ S3, SNS, IAM và triển khai hạ tầng VPC, EC2 thông qua dòng lệnh.<br> | 02/05/2026 | 02/05/2026 | <https://000011.awsstudygroup.com/> |
| 3   | - Cấu hình AWS Backup Plan và tạo Backup Vault.<br> - Áp dụng tag để liên kết các EC2 instance với chính sách sao lưu, đồng thời cấu hình quyền IAM và SNS để nhận thông báo về quá trình backup. | 02/05/2026 | 03/05/2026 | <https://000013.awsstudygroup.com/> |
| 4   | - Kiểm tra quy trình khôi phục dữ liệu và dọn dẹp tài nguyên.<br> - Tìm hiểu Recovery Point, cơ chế restore không ghi đè (non-overwrite restore), Idempotency Token và thứ tự dọn dẹp các tài nguyên liên quan đến AWS Backup.<br> | 03/05/2026 | 04/05/2026 | <https://000013.awsstudygroup.com/> |

### Kết quả đạt được tuần 4:

* Tổng quan:

Trong tuần này, tôi tập trung vào việc cấu hình DNS cho mô hình hybrid, quản trị hạ tầng bằng AWS CLI và triển khai các giải pháp sao lưu, khôi phục dữ liệu. Nội dung dưới đây được tổng hợp từ nhật ký công việc hằng ngày và biên soạn lại theo định dạng báo cáo thực tập theo tuần.

* Kiến thức đã học:

- Hiểu cách thiết lập cơ chế phân giải DNS hai chiều giữa môi trường on-premises mô phỏng và AWS.
- Nâng cao kỹ năng quản lý tài nguyên AWS thông qua AWS CLI, bao gồm S3, SNS, IAM, VPC và EC2.
- Nắm được quy trình xây dựng kế hoạch sao lưu và khôi phục tài nguyên với AWS Backup.
- Hiểu các nguyên tắc dọn dẹp tài nguyên theo mối quan hệ phụ thuộc nhằm tối ưu chi phí vận hành trên AWS.

* Thực hành:

- Triển khai thành công mô hình chuyển tiếp DNS giữa môi trường hybrid mô phỏng.
- Thực hiện triển khai và quản lý hạ tầng bằng AWS CLI thay vì chỉ sử dụng AWS Management Console.
- Cấu hình chính sách sao lưu tự động, thực hiện khôi phục EC2 instance và hiểu rõ vòng đời của quy trình backup và restore.

