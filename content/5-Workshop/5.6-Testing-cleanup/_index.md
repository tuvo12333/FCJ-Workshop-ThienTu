---
title: "Testing & Clean up"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 5.6. </b> "
---

In this final section of the workshop, we will test the deployed API backend using a pre-configured **Postman Collection**, monitor system logs using **CloudWatch**, and tear down all AWS resources to prevent unwanted costs.

---

### 1. Test API Using Postman

The project includes a Postman Collection file to let you quickly execute and test all backend API endpoints without relying on the React frontend.

#### 1.1. Setup Postman
1. Open the **Postman** application.
2. Click **Import** → Choose the file `postman/student-management-api.postman_collection.json` from the project directory.
3. Configure the following environment variables in Postman:
   * `baseUrl`: The API Gateway Invoke URL (e.g., `https://xxxxxxxxxx.execute-api.us-east-1.amazonaws.com/prod`).
   * `idToken`: The JWT token returned from Cognito upon login.

#### 1.2. Retrieve JWT Token from Cognito for Authentication
After signing in with Cognito (e.g., as `admin@example.com`), Cognito returns an `idToken` (JWT string).
Copy this token value and paste it into the Bearer Token credentials field in Postman to authorize admin-only API endpoints (such as Creating a Student or Deleting a Teacher).

---

### 2. Monitor Application Logs via CloudWatch

Whenever a Lambda function is invoked from API Gateway or triggered by an SQS event, its stdout/stderr streams are piped to **Amazon CloudWatch Logs**.

* **Viewing logs**:
  1. Open the **CloudWatch Console** → click **Log groups** in the left navigation pane.
  2. Search for the log group associated with the Lambda function you want to debug (e.g., `/aws/lambda/getStudents` or `/aws/lambda/sendEmailWorker`).
  3. Click the latest log stream to view debug statements, execution times, or stack traces.

---

### 3. Tear Down AWS Resources (Cleanup)

> [!CAUTION]
> To avoid ongoing charges on your AWS billing account, ensure you execute all cleanup steps below once you have finished testing and presenting the project.

Run these AWS CLI commands in your Terminal or Git Bash to delete all deployed resources:

#### 1. Delete Lambda Functions
```bash
for fn in createStudent getStudents getStudentById updateStudent deleteStudent \
          createTeacher getTeachers getTeacherById updateTeacher deleteTeacher \
          createGrade getGrades getGradeById updateGrade deleteGrade \
          docUploadUrl docSaveMetadata materialUploadUrl materialSaveMetadata \
          getMaterials sendEmailWorker; do
  aws lambda delete-function --function-name $fn --region us-east-1
done
```

#### 2. Delete API Gateway REST API
```bash
aws apigateway delete-rest-api --rest-api-id <API_ID> --region us-east-1
```

#### 3. Delete Cognito User Pool
```bash
aws cognito-idp delete-user-pool --user-pool-id <USER_POOL_ID> --region us-east-1
```

#### 4. Delete SQS Queue
```bash
aws sqs delete-queue --queue-url <QUEUE_URL> --region us-east-1
```

#### 5. Delete DynamoDB Tables
```bash
for table in Students Teachers Grades Materials Documents; do
  aws dynamodb delete-table --table-name $table --region us-east-1
done
```

#### 6. Delete S3 Buckets
Note: AWS does not permit deleting non-empty buckets. You must recursively remove all objects first:
```bash
# Empty and delete the document S3 bucket
aws s3 rm s3://student-documents-<yourname> --recursive
aws s3 rb s3://student-documents-<yourname>

# Empty and delete the frontend hosting S3 bucket
aws s3 rm s3://student-portal-frontend-<yourname> --recursive
aws s3 rb s3://student-portal-frontend-<yourname>
```

#### 7. Delete CloudFront Distribution (If created)
1. Go to the CloudFront Console.
2. Select your distribution and click **Disable**.
3. Wait for the status to show disabled (about 5 minutes), then select the distribution again and click **Delete**.

#### 8. Delete the IAM Role
```bash
aws iam delete-role --role-name student-portal-lambda
```

Congratulations! You have completed the AWS Serverless Student Management Portal workshop!
