---
title: "Week 7 Worklog"
date: 2026
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---


### Week 7 Objectives:

* Automate infrastructure provisioning using AWS CloudFormation.
* Analyze cost and usage data with Amazon S3, AWS Glue, and Amazon Athena.
* Compare Savings Plans, Reserved Instances, and Reserved DB Instances.
* Deploy Amazon FSx for Windows File Server integrated with Microsoft Active Directory.
* Protect web applications using AWS WAF in front of an Application Load Balancer (ALB).

### Tasks to be completed this week:
| No. | Tasks                                                                                                                                                                                   | Start Date | Completion Date | Reference                                  |
| ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------ |
| 1    | - Learn to automate web application and RDS infrastructure using AWS CloudFormation.<br> - Create a template to provision a VPC, public subnet, Internet Gateway, route table, EC2, RDS, security groups, and deployment scripts. | 13/05/2026 | 13/05/2026      | <https://000037.awsstudygroup.com/> |
| 2    | - Analyze AWS cost and usage data with AWS Glue and Amazon Athena.<br> - Create S3 buckets for data and query results, configure a Glue crawler and Data Catalog, then query CUR data using Athena SQL.<br> | 14/05/2026 | 14/05/2026      | <https://000040.awsstudygroup.com/> |
| 3    | - Study Savings Plans, Reserved Instances, and Reserved DB Instances.<br> - Compare commitment scope, payment options, discount trade-offs, underutilization risks, and recommendation reports. | 15/05/2026 | 15/05/2026      | <https://000042.awsstudygroup.com/> |
| 4    | - Deploy Amazon FSx for Windows File Server.<br> - Integrate FSx with Microsoft Active Directory, test SMB access from a Linux EC2 instance using cifs-utils/samba-client, and verify file synchronization across nodes.<br> | 16/05/2026 | 16/05/2026      | <https://000025.awsstudygroup.com/> |
| 5    | - Configure AWS WAF to secure a web application.<br> - Place AWS WAF in front of the ALB, connect the ALB to the EC2 application and RDS database, then verify traffic filtering and application protection. | 17/05/2026 | 17/05/2026      | <https://000026.awsstudygroup.com/> |

### Week 7 Results:

* **Overview:**

This week, I focused on learning AWS CloudFormation, cost analysis, commitment-based pricing models, Amazon FSx, and AWS WAF. The content was compiled from my daily worklogs and organized into a weekly report.

* **Knowledge Gained:**

- Learned how to automate infrastructure deployment using AWS CloudFormation.
- Understood how to analyze AWS cost and usage data with Amazon S3, AWS Glue, and Amazon Athena.
- Compared the features of Savings Plans, Reserved Instances, and Reserved DB Instances.
- Learned how to deploy Amazon FSx for Windows File Server integrated with Microsoft Active Directory.
- Understood how AWS WAF protects web applications when deployed in front of an Application Load Balancer.

* **Hands-on Practice:**

- Deployed infrastructure using CloudFormation templates instead of manual configuration.
- Practiced storing, cataloging, and querying cost data with AWS serverless analytics services.
- Implemented Amazon FSx and configured AWS WAF to improve file storage and enhance web application security.