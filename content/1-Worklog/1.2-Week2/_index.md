---
title: "Week 2 Worklog"
date: 2026
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Transition from a locally installed database to a managed database model on AWS.
* Practice setting up an isolated network architecture to ensure secure separation between the web server (public) and the database (private).
* Apply tags and resource groups to classify and manage cloud resources efficiently.
* Build a solid foundation for automation and Continuous Integration/Continuous Deployment (CI/CD) processes in the following stages.

### Tasks to be completed this week:
| Day | Tasks                                                                                                                                                                                   | Start Date | Completion Date | Reference                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Learn how to integrate Amazon RDS with a Node.js application. <br> - Create an RDS MySQL instance in a private subnet, configure a DB subnet group, and set up the connection from the EC2 web server. | 24/04/2026 | 26/04/2026 | <https://000005.awsstudygroup.com/> |
| 2   | - Implement the Security Group chaining mechanism to enhance database security.<br> - Configure the database to allow MySQL traffic only from the EC2 Web App Security Group, and never expose the database port to the Internet. <br> | 25/04/2026 | 26/04/2026 | <https://000005.awsstudygroup.com/><https://000003.awsstudygroup.com/> |
| 3   | - Get familiar with the resource tagging strategy.<br> - Launch EC2 instances for different environments and practice managing tags in bulk through the EC2 Tags interface.<br> | 27/04/2026 | 28/04/2026 | <https://000027.awsstudygroup.com/> |
| 4   | - Build Resource Groups based on predefined tags. <br> - Preview and save resource groups according to EC2 tag conditions for easier searching and management. <br> | 28/04/2026 | 29/04/2026 | <https://000027.awsstudygroup.com/> |

### Week 2 Achievements:

* Overview:

This week, I focused on learning about Amazon RDS, resource tagging techniques, and establishing the foundation for application deployment. The content below is summarized from my daily worklogs and organized into a weekly report.

*Knowledge Acquired:

- Learned how to migrate from a traditional database to AWS's managed database architecture.

- Understood the approach to network isolation, ensuring secure separation between the web tier (public) and the data tier (private).
- Learned how to use tags and resource groups to organize and manage cloud infrastructure efficiently.
- Established a solid system foundation for future automation and CI/CD workflows.

* Hands-on Practice:

- Successfully configured and deployed a basic web application connected to Amazon RDS.

- Clearly separated the network architecture into public/private layers for the application and database tiers.

- Effectively applied tags and resource groups to organize cloud resources, laying the groundwork for future infrastructure governance.