---
title: "Week 6 Worklog"
date: 2026
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---


### Week 6 Objectives:

* Learn how to automate application deployments to EC2 using AWS CodePipeline and CodeDeploy.
* Understand how to control EC2 access through IAM policies with tag-based conditions.
* Practice deploying Grafana and integrating it with Amazon CloudWatch for infrastructure monitoring.
* Explore AWS Systems Manager for centralized EC2 management and memory metrics collection for resource optimization.
* Learn how to encrypt data and audit S3 access using AWS KMS, CloudTrail, and Amazon Athena.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Build a CI/CD pipeline for deploying applications to EC2 using AWS CodePipeline. <br> - Integrate GitHub, CodePipeline, S3 Artifacts, CodeDeploy, AppSpec hooks, PM2 deployment scripts, and the CodeDeploy Agent on EC2. | 08/05/2026 | 08/05/2026 | <https://000017.awsstudygroup.com/><https://000023.awsstudygroup.com/> |
| 2   | - Practice managing EC2 permissions with IAM and resource tags.<br> - Create IAM policies that require the `Environment=Test` tag when launching EC2 instances and allow Start, Stop, or Terminate actions only on instances with the appropriate tags.<br> | 09/05/2026 | 09/05/2026 | <https://000028.awsstudygroup.com/> |
| 3   | - Deploy Grafana on EC2 and integrate it with Amazon CloudWatch.<br> - Configure a VPC, Security Group, and EC2 instance, open port 3000, attach an IAM Role, and visualize CPUUtilization metrics on a Grafana dashboard. | 10/05/2026 | 10/05/2026 | <https://000029.awsstudygroup.com/> |
| 4   | - Manage EC2 instances using AWS Systems Manager. <br> - Attach the AmazonSSMManagedInstanceCore IAM role, troubleshoot Managed Nodes in the Offline state, and execute commands across multiple EC2 instances simultaneously. <br> | 10/05/2026 | 10/05/2026 | <https://000031.awsstudygroup.com/> |
| 5   | - Collect memory metrics for EC2 rightsizing with CloudWatch Agent. <br> - Install CloudWatch Agent, gather RAM utilization metrics, and prepare monitoring data for Compute Optimizer and Cost Explorer. | 11/05/2026 | 11/05/2026 | <https://000032.awsstudygroup.com/> |
| 6   | - Practice data encryption with AWS KMS and audit S3 access. <br> - Use CloudTrail Data Events together with Athena SQL to analyze S3 access history and verify KMS Decrypt permission enforcement when access is denied. | 12/05/2026 | 12/05/2026 | <https://000033.awsstudygroup.com/> |

### Week 6 Achievements:

* Overview:

This week, I focused on deployment automation, access governance, infrastructure monitoring, and data protection on AWS. The content below is summarized from my daily worklogs and organized into a weekly internship report.

* Knowledge Acquired:

- Learned how to build CI/CD pipelines on AWS using CodePipeline and CodeDeploy to automate application deployments.
- Understood how to manage EC2 permissions through IAM policies with tag-based access control.
- Gained practical knowledge of deploying Grafana and integrating it with Amazon CloudWatch for infrastructure visualization.
- Explored AWS Systems Manager for centralized EC2 administration and memory metrics collection to support resource optimization.
- Learned how to protect data with AWS KMS and audit S3 access using CloudTrail and Amazon Athena.

* Hands-on Practice:

- Successfully implemented a CI/CD deployment pipeline and resolved common issues related to CodeDeploy, IAM, and AppSpec configurations.
- Applied IAM policies, resource tags, and AWS KMS to strengthen governance and secure AWS resources.
- Deployed Grafana, CloudWatch Agent, and AWS Systems Manager to improve infrastructure monitoring and operational management.