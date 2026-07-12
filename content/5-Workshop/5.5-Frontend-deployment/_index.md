---
title: "Frontend & Hosting"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

In this section, we will explore the frontend layout of the **AWS Student Management Portal**, configure connection variables for AWS Cognito and API Gateway, run the application locally, and deploy the packaged assets to **Amazon S3** distributed via **Amazon CloudFront**.

---

### 1. Frontend Layout & Authorization

The frontend is built using **ReactJS** and bundled via **Vite**.

* **Protected Routing**: The application uses a `ProtectedRoute` component to validate the user's Cognito-issued JWT Token.
* **Group-Based Authorization**:
  * **Admin/Staff**: Full administrative access to the Dashboard, student/teacher rosters, grade listings, system activity logs, and settings.
  * **Teacher**: Restricted to viewing assigned classes, entering or updating student grades, and uploading learning resources.
  * **Student**: Restricted to viewing personal academic profiles, checking individual grade sheets, and downloading resources uploaded by teachers.

---

### 2. Configure Frontend Environment Variables

To connect your React Frontend with the AWS resources created in previous steps, create a file named `.env` in the `frontend/` directory with the following variables:

```env
# AWS Cognito User Pool Configuration
VITE_USER_POOL_ID=us-east-1_xxxxxxxxx
VITE_APP_CLIENT_ID=xxxxxxxxxxxxxxxxxx

# API Gateway Endpoint (The Invoke URL copied from the previous section)
VITE_API_ENDPOINT=https://xxxxxxxxxx.execute-api.us-east-1.amazonaws.com/prod

# AWS Region running your services
VITE_AWS_REGION=us-east-1
```

*(Be sure to replace these placeholder values with your actual User Pool ID, App Client ID, and API Gateway Invoke URL).*

---

### 3. Run the Application Locally

Once your `.env` file is in place, install dependencies and launch the local development server to test the UI:

```bash
cd frontend
npm run dev
```

Open your browser and navigate to [http://localhost:5173](http://localhost:5173).

You can log in using the automatically generated Admin demo credentials:
* **Email**: `admin@example.com`
* **Password**: `Abc12345!`

Upon logging in for the first time, you will be prompted to choose a new permanent password.

---

### 4. Build Production Package & Deploy to Amazon S3

When you are satisfied with your local testing, compile the React source files into optimized, static HTML/JS/CSS assets ready for AWS hosting.

#### 1. Compile Assets (Build)
```bash
npm run build
```
This command generates a `dist/` directory containing all the production-ready static assets.

#### 2. Create S3 Bucket for Frontend Hosting
Create a new S3 bucket to store these static files (the name must be globally unique):
```bash
aws s3 mb s3://student-portal-frontend-<yourname> --region us-east-1
```

#### 3. Sync Assets (Deploy)
Upload the contents of the `dist/` folder to the S3 bucket:
```bash
aws s3 sync dist/ s3://student-portal-frontend-<yourname> --delete
```

---

### 5. Distribute via Amazon CloudFront (Advanced/Optional)

To optimize load times and serve the web portal securely over HTTPS, configure an **Amazon CloudFront Distribution** pointing to your S3 frontend bucket:
1. Open the **CloudFront Console** → click **Create distribution**.
2. Set the **Origin domain** to point directly to your frontend S3 bucket.
3. Configure **Origin Access Control (OAC)** to secure the bucket, restricting direct public access to S3 so that users can only access the files through CloudFront.
4. Set the **Default root object** to `index.html`.
5. Wait for the distribution deployment to complete (approximately 5-10 minutes). Once deployed, you will receive a CloudFront domain name (e.g., `https://d123456abcdef8.cloudfront.net`) to access your application securely from anywhere.
