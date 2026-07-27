---
title: "Week 4 Worklog"
date: 2026
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---


### Week 4 Objectives:

* Understand how to establish bidirectional DNS name resolution between an on-premises environment and AWS.
* Gain practical experience using AWS CLI to provision and manage AWS services such as S3, SNS, IAM, VPC, and EC2.
* Learn how to implement backup strategies and recovery procedures with AWS Backup.
* Develop good practices for resource cleanup while maintaining cost efficiency.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1   | - Explore the Route 53 Resolver architecture. <br> - Create a simulated on-premises network and an AWS VPC, configure VPC peering, route tables, inbound/outbound endpoints, and resolver rules for DNS communication. | 01/05/2026 | 01/05/2026 | <https://000010.awsstudygroup.com/> |
| 2   | - Learn AWS CLI operations for resource management.<br> - Install AWS CLI v2, configure access credentials, manage S3, SNS, IAM resources, and provision VPC and EC2 infrastructure using command-line operations.<br> | 02/05/2026 | 02/05/2026 | <https://000011.awsstudygroup.com/> |
| 3   | - Configure an AWS Backup plan and create a Backup Vault.<br> - Apply tags to associate EC2 instances with backup policies and configure IAM and SNS permissions for backup notifications. | 02/05/2026 | 03/05/2026 | <https://000013.awsstudygroup.com/> |
| 4   | - Validate the backup restore process and perform resource cleanup.<br> - Explore recovery points, non-overwrite restore behavior, idempotency tokens, and the recommended cleanup sequence for backup resources.<br> | 03/05/2026 | 04/05/2026 | <https://000013.awsstudygroup.com/> |

### Week 4 Achievements:

* Overview:

This week, I concentrated on hybrid DNS configuration, AWS CLI administration, and backup and recovery services. The following summary is compiled from my daily worklogs and reorganized into a weekly internship report.

* Knowledge Acquired:

- Learned how to configure bidirectional DNS resolution between simulated on-premises and AWS environments.
- Improved proficiency in managing AWS resources through the AWS CLI, including S3, SNS, IAM, VPC, and EC2.
- Understood the workflow of creating backup plans and restoring resources with AWS Backup.
- Learned best practices for dependency-aware resource cleanup and AWS cost optimization.

* Hands-on Labs:

- Successfully implemented DNS forwarding between simulated hybrid network environments.
- Performed infrastructure provisioning and management using AWS CLI instead of relying solely on the AWS Management Console.
- Configured automated backup policies, executed restore operations for EC2 instances, and gained practical experience with backup lifecycle management.

