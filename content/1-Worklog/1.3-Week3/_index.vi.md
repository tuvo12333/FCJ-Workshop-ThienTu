---
title: "Worklog Tuần 3"
date: 2026
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---


### Mục tiêu tuần 3:

* Thiết lập các cơ chế kiểm soát tài chính nhằm hạn chế phát sinh chi phí AWS ngoài dự kiến.
* Hiểu rõ sự khác biệt giữa Cost Budget, Usage Budget, RI Budget và Savings Plans Budget.
* Phát triển kỹ năng giám sát hệ thống thông qua CloudWatch metrics, logs, alarms, dashboards và SNS.
* Thực hành phân tích metrics bằng search expressions, metric math và dashboard widgets.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Tạo AWS Cost Budget. <br> - Cấu hình theo dõi tổng chi phí unblended của các dịch vụ AWS và thiết lập các ngưỡng cảnh báo ở mức 50%, 80% và 100%. | 29/04/2026 | 29/04/2026 | <https://000007.awsstudygroup.com/> |
| 2   | - Tạo AWS Usage Budget.<br> - Theo dõi số giờ hoạt động của EC2 để duy trì trong giới hạn Free Tier và nhận biết rủi ro phát sinh chi phí khi quên xóa tài nguyên không còn sử dụng.<br> | 30/04/2026 | 30/04/2026 | <https://000007.awsstudygroup.com/> |
| 3   | - Tìm hiểu RI Budget và Savings Plans Budget.<br> - So sánh việc giám sát mức sử dụng Reserved Instances với giám sát cam kết tài nguyên tính toán trong quản lý chi phí doanh nghiệp. | 31/04/2026 | 31/04/2026 | <https://0000042.awsstudygroup.com/> |
| 4   | - Bắt đầu Amazon CloudWatch Workshop. <br> - Triển khai hạ tầng EC2 bằng CloudFormation và nhận diện các lỗi liên quan đến Region và giới hạn vCPU khi tạo stack.<br> | 01/05/2026 | 01/05/2026 | <https://000008.awsstudygroup.com/> <https://0000036.awsstudygroup.com/> |

### Kết quả đạt được tuần 3:

* Tổng quan:

Trong tuần này, tôi tập trung vào việc quản lý chi phí AWS và xây dựng nền tảng quan sát hệ thống. Nội dung dưới đây được tổng hợp từ các worklog hằng ngày và biên soạn lại thành báo cáo tổng kết theo tuần.

* Kiến thức đã học:

- Biết cách thiết lập các cơ chế kiểm soát tài chính nhằm giảm thiểu rủi ro phát sinh chi phí AWS ngoài mong muốn.
- Hiểu rõ mục đích và sự khác biệt giữa Cost Budget, Usage Budget, RI Budget và Savings Plans Budget.
- Tìm hiểu các tính năng giám sát cốt lõi của Amazon CloudWatch, bao gồm metrics, logs, alarms, dashboards và thông báo qua SNS.
- Thực hành phân tích CloudWatch metrics bằng search expressions, metric math và dashboard widgets.

* Thực hành:

- Cấu hình thành công các cảnh báo ngân sách dựa trên cả chi phí và mức sử dụng dịch vụ.
- Hiểu được tầm quan trọng của việc thiết lập các cơ chế kiểm soát chi phí trước khi thực hiện nhiều bài lab trên AWS.
- Bắt đầu làm việc với Amazon CloudWatch metrics và biết cách xử lý các giới hạn khi triển khai hạ tầng, chẳng hạn như Region và hạn mức vCPU.
