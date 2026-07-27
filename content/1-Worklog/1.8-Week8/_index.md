### Week 8 Objectives:

* Enhance AWS access management by applying Permission Boundary to control delegated administrator permissions.
* Practice Infrastructure as Code (IaC) with AWS CDK to automate infrastructure provisioning instead of manually configuring resources through the AWS Console.
* Explore database transformation and migration processes using AWS DMS to minimize service downtime.
* Design IAM Role access control mechanisms based on environmental conditions and real-world system constraints.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 1   | - Apply IAM Permission Boundary to manage user permissions.<br> - Design layered permission boundaries for administrator and developer users to prevent privilege escalation and restrict access to sensitive resources such as RDS. | 18/05/2026 | 18/05/2026      | <https://000030.awsstudygroup.com/> |
| 2   | - Deploy AWS infrastructure using AWS CDK.<br> - Use TypeScript CDK to define VPC, public EC2 instances, private RDS MariaDB, Security Groups, and UserData scripts for initial database setup.<br> | 19/05/2026 | 19/05/2026      | <https://000038.awsstudygroup.com/> |
| 3   | - Perform database schema conversion and migration.<br> - Migrate the web application's database from RDS MySQL to RDS MariaDB using AWS DMS endpoints with Full Load and Change Data Capture (CDC) configurations. | 20/05/2026 | 20/05/2026      | <https://000043.awsstudygroup.com/> |
| 4   | - Test IAM Role conditions and access policies.<br> - Modify access restrictions from IP-based conditions to aws:RequestedRegion due to dynamic network environments, then validate access permissions across different AWS Regions.<br> | 21/05/2026 | 21/05/2026      | <https://000044.awsstudygroup.com/> |


### Week 8 Achievements:

* Overview:

During this week, I focused on advanced IAM governance, Infrastructure as Code with AWS CDK, database migration, and conditional access control. The content was summarized from daily worklogs and reorganized into a weekly internship report format.

* Knowledge Acquired:

- Understood how to use Permission Boundary to define maximum permissions for delegated administrators and control permission assignments in AWS.
- Learned how to build full-stack infrastructure using AWS CDK instead of manually configuring resources through the Console or lengthy YAML templates.
- Gained knowledge of database migration workflows using AWS DMS to reduce downtime during system transitions.
- Learned how to design IAM Role Conditions based on practical requirements such as Region restrictions, network environments, and deployment conditions.

* Hands-on Practice:

- Understood that Permission Boundary acts as a maximum permission limit rather than a standard permission-granting policy.
- Successfully provisioned infrastructure using AWS CDK and established secure communication between the application layer and database layer.
- Practiced heterogeneous database migration and adjusted IAM Conditions according to real-world environment constraints.