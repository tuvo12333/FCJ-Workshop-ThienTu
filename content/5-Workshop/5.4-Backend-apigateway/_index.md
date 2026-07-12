---
title: "Backend & API Gateway"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 5.4. </b> "
---

In this section, we will package and deploy the backend source code (Node.js) to **AWS Lambda** and configure **Amazon API Gateway** to act as a secure API entry point integrated with a **Cognito Authorizer**.

---

### Step 1: Create an IAM Role for Lambda

Before deploying the Lambda functions, you must configure an IAM Role to grant the necessary minimum permissions required for backend logic execution:
* Read and write permissions on the 5 **DynamoDB** tables.
* Permission to generate Presigned URLs and write objects to the **S3 Bucket**.
* Permission to publish messages to the **SQS Queue**.
* Permission to send automated emails via **Amazon SES**.
* Permission to write execution logs to **Amazon CloudWatch Logs**.

You can create an IAM Role named `student-portal-lambda` through the IAM Console or let the infrastructure setup script configure it:
```bash
# Retrieve the IAM Role ARN after creation
LAMBDA_ROLE_ARN=arn:aws:iam::<ACCOUNT_ID>:role/student-portal-lambda
```

---

### Step 2: Deploy Lambda Functions

The backend consists of 21 separate Lambda functions, each handling dedicated business APIs (CRUD operations for students, teachers, grades, presigned URL generation, and the background email notification worker).

To deploy all functions to AWS Lambda, export the configuration environment variables and run the deployment script:

```bash
# 1. Configure deployment environment variables
export LAMBDA_ROLE_ARN="arn:aws:iam::<ACCOUNT_ID>:role/student-portal-lambda"
export DOCUMENTS_BUCKET="student-documents-<yourname>"
export NOTIFICATION_QUEUE_URL="https://sqs.us-east-1.amazonaws.com/<ACCOUNT_ID>/student-notifications"
export FROM_EMAIL="your-verified-email@example.com"

# 2. Run the packaging and deployment script
bash scripts/deploy-lambdas.sh us-east-1
```

> [!TIP]
> Ensure the email configured in `FROM_EMAIL` has been successfully verified in **Amazon SES** (under Sandbox mode, both sender and recipient email addresses must be verified to prevent delivery failures).

---

### Step 3: Deploy and Configure API Gateway

To allow the Frontend application to interact with the Lambda functions, we need a REST API Gateway to map HTTP Endpoints to their corresponding Lambda functions and enforce security.

Run the API Gateway deployment script:
```bash
# Set the Cognito User Pool ID saved from the previous step
export USER_POOL_ID="us-east-1_xxxxxxxxx"

# Execute the API gateway builder script
bash scripts/deploy-apigateway.sh us-east-1
```

This script automates the creation of the following API Gateway resources:
1. Creates a REST API named `student-portal-api`.
2. Creates a **Cognito Authorizer** linked with your User Pool.
3. Sets up path resources and methods:
   * `/students`, `/students/{id}` -> Maps to student CRUD Lambda functions.
   * `/teachers`, `/teachers/{id}` -> Maps to teacher CRUD Lambda functions.
   * `/grades`, `/grades/{id}` -> Maps to grade CRUD Lambda functions.
   * `/materials/upload-url`, `/materials/metadata` -> Maps to learning material Lambda functions.
   * `/documents/upload-url`, `/documents/metadata` -> Maps to student document Lambda functions.
4. Applies the Cognito Authorizer to all methods requiring authentication (e.g., POST, PUT, DELETE).
5. Enables **CORS** (Cross-Origin Resource Sharing) on all endpoints to permit requests from browser-based clients.
6. Deploys the API to a stage named `prod`.

When complete, copy the **Invoke URL** displayed in the terminal:
```text
https://xxxxxxxxxx.execute-api.us-east-1.amazonaws.com/prod
```
This is the API Gateway endpoint that your React Frontend will use to make backend requests.
