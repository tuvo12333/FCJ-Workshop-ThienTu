---
title: "Week 5 Worklog"
date: 2026
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Week 5 Objectives:

* Learn how to strengthen security monitoring by using AWS Security Hub and AWS Config.
* Understand the process of deploying containerized applications with a microservices architecture on Amazon ECS and AWS Fargate.
* Compare VPC Peering and Transit Gateway to identify the most suitable solution for connecting multiple VPCs.
* Practice building an event-driven automation workflow for AWS cost optimization using CloudWatch, SNS, and Lambda.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Study AWS Security Hub and AWS Config.<br> - Enable Security Hub CSPM and explore AWS Foundational Security Best Practices, CIS Benchmark, and PCI DSS standards to evaluate the security posture of an AWS environment. | 04/05/2026 | 04/05/2026 | <https://000018.awsstudygroup.com/> |
| 2   | - Explore application deployment with Amazon ECS. <br> - Practice packaging applications with Docker, storing container images in Amazon ECR, deploying Fargate tasks, configuring Task Definitions, Private Subnets, NAT Gateway, and separating services.<br> | 05/05/2026 | 05/05/2026 | <https://000016.awsstudygroup.com/><https://000067.awsstudygroup.com/> |
| 3   | - Practice configuring VPC Peering. <br> - Create two VPCs with non-overlapping CIDR blocks, configure Route Tables and Security Groups, verify private connectivity, and evaluate the limitations of VPC Peering. | 06/05/2026 | 06/05/2026 | <https://000019.awsstudygroup.com/> |
| 4   | - Build a hub-and-spoke network architecture using Transit Gateway.<br> - Connect four VPCs through Transit Gateway Attachments, troubleshoot missing route propagation, verify inter-VPC connectivity, and clean up Transit Gateway resources after testing to optimize costs.<br> | 06/05/2026 | 06/05/2026 | <https://000020.awsstudygroup.com/> |\
| 5   | - Build an automated EC2 cost optimization workflow using AWS Lambda.<br> - Use VPC Flow Logs, CloudWatch Metric Filters, CloudWatch Alarms, SNS, and Lambda (boto3) to automatically stop EC2 instances when ICMP traffic is detected.<br> | 07/05/2026 | 08/05/2026 | <https://000022.awsstudygroup.com/><https://000074.awsstudygroup.com/> |

### Week 5 Achievements:

* Overview:

This week, I focused on improving cloud security, deploying containerized applications, and implementing networking solutions across multiple VPCs. The content below summarizes my daily worklogs and has been organized into a weekly internship report.

* Knowledge Acquired:

- Learned how to use AWS Security Hub and AWS Config to monitor and assess the security posture of AWS infrastructure.
- Gained an understanding of deploying containerized applications with a microservices architecture using Amazon ECS and AWS Fargate.
- Understood the strengths, limitations, and appropriate use cases of VPC Peering and Transit Gateway.
- Learned how to build event-driven automation workflows for monitoring infrastructure and optimizing AWS operational costs.

* Hands-on Practice:

- Successfully integrated security, containerization, networking, and automation services within a single hands-on environment.
- Configured both VPC Peering and Transit Gateway to connect multiple VPCs using different networking architectures.
- Built an event-driven workflow that collects logs, detects specific events, and triggers AWS Lambda functions to perform automated actions.