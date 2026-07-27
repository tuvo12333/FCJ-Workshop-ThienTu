---
title: "Worklog Tuần 2"
date: 2026
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---


### Mục tiêu tuần 2:

* Chuyển dịch từ cơ sở dữ liệu cài đặt cục bộ sang mô hình cơ sở dữ liệu được quản lý (managed database) trên AWS.
* Thực hành thiết lập kiến trúc mạng cô lập, đảm bảo tách biệt an toàn giữa web server (public) và database (private).
* Ứng dụng thẻ (tag) và nhóm tài nguyên (resource group) để phân loại, quản lý tài nguyên đám mây hiệu quả.
* Xây dựng nền tảng vững chắc để chuẩn bị cho các quy trình tự động hóa và tích hợp/triển khai liên tục (CI/CD) ở các giai đoạn sau.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Tìm hiểu cách tích hợp Amazon RDS với ứng dụng Node.js. <br> - Khởi tạo RDS MySQL trong private subnet, thiết lập DB subnet group và cấu hình kết nối từ web server EC2.                                                  | 24/04/2026 | 26/04/2026      | <https://000005.awsstudygroup.com/> |
| 2   | - Triển khai cơ chế security group chaining để tăng cường bảo mật cho cơ sở dữ liệu.<br> - Cấu hình chỉ cho phép luồng dữ liệu MySQL đi từ Security Group của EC2 Web App, tuyệt đối không mở port database ra Internet. <br>                                              | 25/04/2026 | 26/04/2026      | <https://000005.awsstudygroup.com/><https://000003.awsstudygroup.com/> |
| 3   | - Làm quen với chiến lược gắn thẻ (tagging) tài nguyên.<br> - Khởi tạo các EC2 instance cho từng môi trường riêng biệt và thực hành quản lý tag hàng loạt thông qua giao diện EC2 Tags..<br>  | 27/04/2026   | 28/04/2026      | <https://000027.awsstudygroup.com/> |
| 4   | - Xây dựng Resource Group dựa trên các tag đã định nghĩa. <br> - Preview và lưu nhóm tài nguyên theo điều kiện tag của EC2 để dễ tìm kiếm và quản lý. <br>                           | 28/04/2026   | 29/04/2026      | <https://000027.awsstudygroup.com/> |



### Kết quả đạt được tuần 2:

* Tổng quan:

Tuần này em tập chung vào tìm hiểu dịch vụ Amazon RDS, kỹ thuật gắn thẻ tài nguyên và thiết lập nền tảng để triển khai ứng dụng. Các nội dung dưới đây được đúc kết từ nhật ký làm việc (worklog) hằng ngày và hệ thống lại thành báo cáo tổng kết tuần

*Kiến thức đã học:

- Nắm được phương pháp chuyển đổi từ cơ sở dữ liệu truyền thống sang kiến trúc managed database của AWS.

- Hiểu rõ phương pháp cô lập mạng lưới, đảm bảo an toàn giữa tầng web (public) và tầng dữ liệu (private).
- Biết cách dùng thẻ (tag) và nhóm tài nguyên (resource group) để sắp xếp, tổ chức hạ tầng cloud một cách khoa học.
- Tạo tiền đề về mặt hệ thống cho các bài toán tự động hóa và CI/CD trong tương lai.

* Thực hành:

- Cấu hình và triển khai thành công ứng dụng web cơ bản có kết nối với Amazon RDS.

- Phân chia rõ ràng kiến trúc mạng theo mô hình public/private cho từng tầng (application và database).

- Vận dụng thành thạo tag và resource group vào việc tổ chức tài nguyên, tạo cơ sở cho các hoạt động quản trị (governance) hạ tầng sau này.



