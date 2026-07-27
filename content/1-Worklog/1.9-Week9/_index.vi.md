---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---


# Worklog Tuần 9
## Mục tiêu tuần 9

Trong tuần 9, mục tiêu chính là nghiên cứu các dịch vụ **giám sát, thu thập log và theo dõi hoạt động trên nền tảng AWS**, bao gồm **Amazon CloudWatch** và **AWS CloudTrail**. Đây là những dịch vụ hỗ trợ quản trị viên giám sát hiệu năng hệ thống, phát hiện sự cố, thiết lập cảnh báo và theo dõi lịch sử thao tác trong môi trường AWS.

Nội dung của tuần này thuộc nhóm **Optimize / Tối ưu hệ thống trên AWS**, tập trung vào việc giám sát, quản lý vận hành, tăng cường bảo mật và tối ưu hiệu suất của hệ thống sau khi được triển khai trên AWS. ([Cloud Journey][1])

Các nội dung trọng tâm của tuần bao gồm:

* Tìm hiểu khái quát về giám sát hệ thống trên AWS.
* Nghiên cứu **Amazon CloudWatch Metrics**.
* Nghiên cứu **Amazon CloudWatch Logs** và **CloudWatch Logs Insights**.
* Thực hành tạo **CloudWatch Alarm**.
* Thực hành xây dựng **CloudWatch Dashboard**.
* Tìm hiểu **AWS CloudTrail** để theo dõi API call và hoạt động của người dùng.
* So sánh chức năng của CloudWatch và CloudTrail trong quá trình quản trị hệ thống.

---

## Các công việc cần triển khai trong tuần này

| Thứ tự | Công việc thực hiện                                                                                                                                                 | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| --- | --- | --- | --- | --- |
| **1**  | Nghiên cứu tổng quan về giám sát hệ thống trên AWS, tìm hiểu vai trò của CloudWatch và CloudTrail trong việc vận hành, xử lý sự cố và bảo vệ hệ thống. | 22/05/2026 | 22/05/2026 | [https://cloudjourney.awsstudygroup.com/vi/3-optimize/](https://cloudjourney.awsstudygroup.com/vi/3-optimize/) <br> [https://000008.awsstudygroup.com/vi/](https://000008.awsstudygroup.com/vi/) <br> [https://docs.aws.amazon.com/decision-guides/latest/cloudtrail-or-cloudwatch/cloudtrail-or-cloudwatch.html](https://docs.aws.amazon.com/decision-guides/latest/cloudtrail-or-cloudwatch/cloudtrail-or-cloudwatch.html) |
| **2**  | Tìm hiểu CloudWatch Metrics, cách theo dõi metric của EC2, RDS, EBS và các dịch vụ AWS khác; nghiên cứu namespace, dimension và statistic. | 22/05/2026 | 22/05/2026 | [https://000008.awsstudygroup.com/vi/3-cloud-watch-metric/](https://000008.awsstudygroup.com/vi/3-cloud-watch-metric/) <br> [https://000008.awsstudygroup.com/vi/3-cloud-watch-metric/3.1-viewing-metrics/](https://000008.awsstudygroup.com/vi/3-cloud-watch-metric/3.1-viewing-metrics/) <br> [https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/working_with_metrics.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/working_with_metrics.html) |
| **3**  | Nghiên cứu CloudWatch Logs, Log Group, Log Stream, Logs Insights và cách khai thác log phục vụ việc phân tích và xử lý lỗi của hệ thống. | 23/05/2026 | 23/05/2026 | [https://000008.awsstudygroup.com/vi/4-cloud-watch-log/](https://000008.awsstudygroup.com/vi/4-cloud-watch-log/) <br> [https://000008.awsstudygroup.com/vi/4-cloud-watch-log/4.1-cloud-watch-logs/](https://000008.awsstudygroup.com/vi/4-cloud-watch-log/4.1-cloud-watch-logs/) <br> [https://000008.awsstudygroup.com/vi/4-cloud-watch-log/4.2-cloud-watch-logs-insights/](https://000008.awsstudygroup.com/vi/4-cloud-watch-log/4.2-cloud-watch-logs-insights/) |
| **4**  | Tìm hiểu CloudWatch Alarm và CloudWatch Dashboard; thực hành cấu hình cảnh báo dựa trên metric và xây dựng dashboard để theo dõi tài nguyên AWS. | 24/05/2026 | 24/05/2026 | [https://000008.awsstudygroup.com/vi/5-cloud-watch-alarm/](https://000008.awsstudygroup.com/vi/5-cloud-watch-alarm/) <br> [https://000008.awsstudygroup.com/vi/6-cloud-watch-dashboard/](https://000008.awsstudygroup.com/vi/6-cloud-watch-dashboard/) <br> [https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Alarms.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Alarms.html) <br> [https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Dashboards.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Dashboards.html) |
| **5**  | Tìm hiểu AWS CloudTrail, cách theo dõi lịch sử API trong tài khoản AWS; so sánh CloudWatch với CloudTrail, tổng hợp kiến thức và ghi nhận các lỗi thường gặp trong quá trình thực hành. | 25/05/2026 | 25/05/2026 | [https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html) <br> [https://aws.amazon.com/cloudtrail/](https://aws.amazon.com/cloudtrail/) <br> [https://docs.aws.amazon.com/decision-guides/latest/cloudtrail-or-cloudwatch/cloudtrail-or-cloudwatch.html](https://docs.aws.amazon.com/decision-guides/latest/cloudtrail-or-cloudwatch/cloudtrail-or-cloudwatch.html) <br> [https://cloudjourney.awsstudygroup.com/vi/3-optimize/](https://cloudjourney.awsstudygroup.com/vi/3-optimize/) |

## Kết quả đạt được tuần 9

### Tổng quan

Trong tuần này, tôi tập trung nghiên cứu các dịch vụ hỗ trợ **giám sát, theo dõi và ghi nhận hoạt động trên AWS**. Amazon CloudWatch được sử dụng để theo dõi metric, log, alarm và dashboard của hệ thống, trong khi AWS CloudTrail đảm nhiệm việc ghi nhận lịch sử API call và các thao tác của người dùng trong tài khoản AWS. Hai dịch vụ này giúp nâng cao khả năng giám sát, kiểm tra và quản lý hệ thống sau khi triển khai.

### Kiến thức đã học

Sau khi hoàn thành tuần 9, tôi đã đạt được các kiến thức sau:

* Hiểu được vai trò của **monitoring** và **logging** trong quá trình quản trị hệ thống AWS.
* Nắm được chức năng của **Amazon CloudWatch** trong việc theo dõi tài nguyên và ứng dụng thông qua metric, log, alarm và dashboard.
* Hiểu **CloudWatch Metrics** dùng để thu thập và theo dõi các chỉ số hiệu năng như CPU Utilization, Network In/Out, Disk Read/Write và các custom metric.
* Hiểu **CloudWatch Logs** được sử dụng để lưu trữ, quản lý và tìm kiếm log của hệ thống.
* Hiểu **CloudWatch Logs Insights** hỗ trợ truy vấn và phân tích log nhằm phát hiện lỗi hoặc sự kiện bất thường.
* Hiểu **CloudWatch Alarm** giúp tự động gửi cảnh báo khi metric đạt đến ngưỡng được cấu hình.
* Hiểu **CloudWatch Dashboard** cho phép tổng hợp nhiều metric và alarm trên cùng một giao diện theo dõi.
* Hiểu **AWS CloudTrail** ghi nhận toàn bộ hoạt động API và thao tác của user, role hoặc dịch vụ AWS trong tài khoản.
* Phân biệt được CloudWatch chủ yếu phục vụ **giám sát và theo dõi hiệu năng**, còn CloudTrail phục vụ **kiểm tra lịch sử hoạt động và audit bảo mật**.

---

## Thực hành

Trong quá trình học tập và thực hành, tôi đã hoàn thành các nội dung sau:

* Truy cập và làm quen với Amazon CloudWatch trên AWS Management Console.
* Theo dõi các metric cơ bản của EC2 Instance.
* Thực hành lọc metric theo namespace và dimension.
* Tìm hiểu cấu trúc Log Group và Log Stream trong CloudWatch Logs.
* Sử dụng CloudWatch Logs Insights để truy vấn và phân tích log.
* Tạo CloudWatch Alarm để giám sát và cảnh báo khi metric vượt ngưỡng.
* Xây dựng CloudWatch Dashboard để theo dõi nhiều chỉ số trên cùng một màn hình.
* Truy cập AWS CloudTrail và kiểm tra Event History.
* Quan sát cách CloudTrail ghi nhận các thao tác tạo, cập nhật và xóa tài nguyên AWS.
* Tổng hợp các lỗi thường gặp như chưa cấu hình CloudWatch Agent, thiếu quyền IAM, chọn sai Region, metric chưa phát sinh dữ liệu hoặc cấu hình ngưỡng Alarm chưa phù hợp.

---

## Bảng so sánh CloudWatch và CloudTrail

| Tiêu chí                   | Amazon CloudWatch                                     | AWS CloudTrail                                  |
| -------------------------- | ----------------------------------------------------- | ----------------------------------------------- |
| **Mục đích chính**         | Theo dõi hiệu năng và trạng thái hoạt động của hệ thống | Ghi nhận lịch sử thao tác và API call           |
| **Dữ liệu theo dõi**       | Metric, log, alarm, dashboard                         | Event, API call, user activity                  |
| **Dùng khi nào**           | Khi cần giám sát tài nguyên, log hoặc hiệu năng hệ thống | Khi cần kiểm tra lịch sử thao tác trong tài khoản AWS |
| **Hỗ trợ troubleshooting** | Phân tích lỗi hiệu năng, log và tài nguyên            | Kiểm tra thay đổi cấu hình và hoạt động người dùng |
| **Ví dụ sử dụng**          | Cảnh báo khi CPU EC2 vượt ngưỡng cấu hình             | Kiểm tra ai đã tạo, sửa hoặc xóa tài nguyên AWS |

---

## Tóm tắt tuần 9

**Tuần 9:** Tìm hiểu Amazon CloudWatch và AWS CloudTrail để phục vụ việc giám sát hệ thống, theo dõi metric, quản lý log, thiết lập alarm, xây dựng dashboard và kiểm tra lịch sử hoạt động trong tài khoản AWS.