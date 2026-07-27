---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

# Week 9 Worklog

## Week 9 Objectives

The primary objective of Week 9 is to study **AWS monitoring, logging, and system activity tracking services**, including **Amazon CloudWatch** and **AWS CloudTrail**. These services play an important role in helping administrators monitor resource performance, detect issues, configure alerts, and review activity history within an AWS account.

This week's content belongs to the **Optimize** phase of AWS, focusing on system operations, monitoring, security, performance optimization, and post-deployment management. ([Cloud Journey][1])

The main topics covered this week include:

* Understanding the fundamentals of AWS system monitoring.
* Learning about **Amazon CloudWatch Metrics**.
* Learning about **Amazon CloudWatch Logs** and **CloudWatch Logs Insights**.
* Creating **CloudWatch Alarms**.
* Building **CloudWatch Dashboards**.
* Learning how **AWS CloudTrail** records API calls and user activities.
* Comparing the roles of CloudWatch and CloudTrail in AWS system operations.

---

## Tasks to Complete This Week

| No. | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| **1** | Study the fundamentals of AWS monitoring and understand the roles of CloudWatch and CloudTrail in system operations, troubleshooting, and security. | 22/05/2026 | 22/05/2026 | [https://cloudjourney.awsstudygroup.com/vi/3-optimize/](https://cloudjourney.awsstudygroup.com/vi/3-optimize/) <br> [https://000008.awsstudygroup.com/vi/](https://000008.awsstudygroup.com/vi/) <br> [https://docs.aws.amazon.com/decision-guides/latest/cloudtrail-or-cloudwatch/cloudtrail-or-cloudwatch.html](https://docs.aws.amazon.com/decision-guides/latest/cloudtrail-or-cloudwatch/cloudtrail-or-cloudwatch.html) |
| **2** | Learn about CloudWatch Metrics, including how to monitor metrics for EC2, RDS, EBS, and other AWS services, as well as namespaces, dimensions, and statistics. | 22/05/2026 | 22/05/2026 | [https://000008.awsstudygroup.com/vi/3-cloud-watch-metric/](https://000008.awsstudygroup.com/vi/3-cloud-watch-metric/) <br> [https://000008.awsstudygroup.com/vi/3-cloud-watch-metric/3.1-viewing-metrics/](https://000008.awsstudygroup.com/vi/3-cloud-watch-metric/3.1-viewing-metrics/) <br> [https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/working_with_metrics.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/working_with_metrics.html) |
| **3** | Study CloudWatch Logs, Log Groups, Log Streams, and Logs Insights, and learn how logs are used for troubleshooting and system analysis. | 23/05/2026 | 23/05/2026 | [https://000008.awsstudygroup.com/vi/4-cloud-watch-log/](https://000008.awsstudygroup.com/vi/4-cloud-watch-log/) <br> [https://000008.awsstudygroup.com/vi/4-cloud-watch-log/4.1-cloud-watch-logs/](https://000008.awsstudygroup.com/vi/4-cloud-watch-log/4.1-cloud-watch-logs/) <br> [https://000008.awsstudygroup.com/vi/4-cloud-watch-log/4.2-cloud-watch-logs-insights/](https://000008.awsstudygroup.com/vi/4-cloud-watch-log/4.2-cloud-watch-logs-insights/) |
| **4** | Learn about CloudWatch Alarms and CloudWatch Dashboards; practice configuring alarms based on metric thresholds and creating dashboards for resource monitoring. | 24/05/2026 | 24/05/2026 | [https://000008.awsstudygroup.com/vi/5-cloud-watch-alarm/](https://000008.awsstudygroup.com/vi/5-cloud-watch-alarm/) <br> [https://000008.awsstudygroup.com/vi/6-cloud-watch-dashboard/](https://000008.awsstudygroup.com/vi/6-cloud-watch-dashboard/) <br> [https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Alarms.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Alarms.html) <br> [https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Dashboards.html](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Dashboards.html) |
| **5** | Learn about AWS CloudTrail, understand how it records API activity within an AWS account, compare CloudWatch with CloudTrail, summarize the knowledge gained, and document common issues encountered during practice. | 25/05/2026 | 25/05/2026 | [https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html) <br> [https://aws.amazon.com/cloudtrail/](https://aws.amazon.com/cloudtrail/) <br> [https://docs.aws.amazon.com/decision-guides/latest/cloudtrail-or-cloudwatch/cloudtrail-or-cloudwatch.html](https://docs.aws.amazon.com/decision-guides/latest/cloudtrail-or-cloudwatch/cloudtrail-or-cloudwatch.html) <br> [https://cloudjourney.awsstudygroup.com/vi/3-optimize/](https://cloudjourney.awsstudygroup.com/vi/3-optimize/) |

---

## Week 9 Achievements

### Overview

This week, I focused on studying AWS services for **system monitoring, logging, and activity tracking**. Amazon CloudWatch was used to monitor metrics, logs, alarms, and dashboards, while AWS CloudTrail was used to record API calls and user activities within an AWS account. Together, these services improve system monitoring, auditing, and operational management after deployment.

### Knowledge Gained

After completing Week 9, I acquired the following knowledge:

* Understood the importance of **monitoring** and **logging** in AWS system administration.
* Learned how **Amazon CloudWatch** monitors AWS resources and applications through metrics, logs, alarms, and dashboards.
* Understood that **CloudWatch Metrics** collect and display performance data such as CPU Utilization, Network In/Out, Disk Read/Write, and custom metrics.
* Learned that **CloudWatch Logs** provide centralized storage, management, and search capabilities for system logs.
* Understood how **CloudWatch Logs Insights** enables querying and analyzing logs to detect errors and unusual events.
* Learned that **CloudWatch Alarms** automatically notify users when configured metric thresholds are exceeded.
* Understood that **CloudWatch Dashboards** provide a unified view of multiple metrics and alarms.
* Learned that **AWS CloudTrail** records API calls and activities performed by users, IAM roles, and AWS services.
* Distinguished the different purposes of CloudWatch for **performance monitoring** and CloudTrail for **security auditing and activity tracking**.

---

## Hands-on Practice

During this week's practice, I completed the following tasks:

* Accessed Amazon CloudWatch through the AWS Management Console.
* Monitored basic metrics of an EC2 instance.
* Practiced filtering metrics using namespaces and dimensions.
* Explored Log Groups and Log Streams in CloudWatch Logs.
* Used CloudWatch Logs Insights to query and analyze log data.
* Created CloudWatch Alarms to monitor metrics and trigger notifications.
* Built CloudWatch Dashboards to visualize multiple metrics on a single interface.
* Accessed AWS CloudTrail and reviewed Event History.
* Observed how CloudTrail records resource creation, modification, and deletion events.
* Documented common issues such as missing CloudWatch Agent configuration, insufficient IAM permissions, incorrect AWS Region selection, unavailable metrics, or improperly configured alarm thresholds.

---

## Comparison Between CloudWatch and CloudTrail

| Criteria | Amazon CloudWatch | AWS CloudTrail |
| -------- | ----------------- | -------------- |
| **Primary Purpose** | Monitor system performance and operational health | Record API calls and account activity history |
| **Data Monitored** | Metrics, logs, alarms, dashboards | Events, API calls, user activity |
| **When to Use** | Monitor system resources, application logs, and performance | Audit account activity and review operational history |
| **Troubleshooting Support** | Analyze performance issues, application logs, and resource health | Investigate configuration changes and user actions |
| **Example Use Case** | Alert when EC2 CPU utilization exceeds a threshold | Identify who created, modified, or deleted an AWS resource |

---

## Week 9 Summary

**Week 9:** Studied Amazon CloudWatch and AWS CloudTrail to monitor AWS resources, analyze metrics and logs, configure alarms, build dashboards, and review account activity history for system monitoring and security auditing.

[1]: https://cloudjourney.awsstudygroup.com/3-optimize/ "Optimizing the System - The First Cloud Journey"