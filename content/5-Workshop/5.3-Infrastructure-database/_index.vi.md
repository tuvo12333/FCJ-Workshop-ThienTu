---
title: "Cơ sở dữ liệu & Hạ tầng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 5.3. </b> "
---

Trong phần này, chúng ta sẽ bắt đầu khởi chạy các dịch vụ hạ tầng cốt lõi phục vụ lưu trữ dữ liệu, xác thực người dùng và truyền thông báo, bao gồm: **DynamoDB**, **S3 Bucket**, **SQS Queue** và **Amazon Cognito**.

Dự án cung cấp sẵn một số script giúp tự động hóa quá trình cấu hình này.

---

### Bước 1: Cài đặt thư viện phụ thuộc (npm packages)

Di chuyển vào thư mục dự án trên máy tính của bạn và cài đặt các thư viện cần thiết cho cả backend và frontend:

```bash
# 1. Di chuyển vào thư mục backend và cài đặt thư viện
cd backend
npm install

# 2. Di chuyển vào thư mục frontend và cài đặt thư viện
cd ../frontend
npm install
```

---

### Bước 2: Tạo các bảng DynamoDB

Hệ thống quản lý sinh viên sử dụng 5 bảng DynamoDB để lưu trữ thông tin nghiệp vụ độc lập:
* **Students**: Lưu hồ sơ sinh viên (PK: `id` - studentId).
* **Teachers**: Lưu hồ sơ giáo viên (PK: `id` - teacherId).
* **Grades**: Lưu điểm số môn học (PK: `id` - `${studentId}-${subject}-${timestamp}`).
* **Materials**: Lưu tài liệu học tập của giáo viên (PK: `id` - `${type}-${timestamp}`).
* **Documents**: Lưu metadata hồ sơ của sinh viên (PK: `id` - `${studentId}-${timestamp}`).

Chạy script sau để tự động tạo toàn bộ các bảng trên AWS với chế độ Billing `PAY_PER_REQUEST` (On-Demand):

```bash
cd ..
bash scripts/deploy-dynamodb.sh us-east-1
```

*(Hoặc nếu bạn muốn tạo thủ công, bạn có thể thực hiện lệnh `aws dynamodb create-table` cho từng bảng với các Partition Key tương ứng).*

---

### Bước 3: Tạo S3 Document Bucket & Cấu hình CORS

S3 Bucket dùng để lưu trữ file tài liệu thực tế của sinh viên và giáo viên. Do Frontend React (chạy tại trình duyệt) sẽ tải trực tiếp file lên S3 qua **Presigned URL**, chúng ta cần cấu hình **CORS** (Cross-Origin Resource Sharing) để trình duyệt không chặn request.

#### 1. Tạo S3 Bucket lưu tài liệu
Lưu ý: Tên bucket của S3 phải là **duy nhất toàn cầu**. Bạn hãy thay `<yourname>` bằng tên viết tắt hoặc mã số cá nhân của bạn:
```bash
aws s3 mb s3://student-documents-<yourname> --region us-east-1
```

#### 2. Áp dụng cấu hình CORS
Sử dụng file cấu hình `cors.json` có sẵn trong dự án:
```bash
aws s3api put-bucket-cors --bucket student-documents-<yourname> --cors-configuration file://cors.json
```

Nội dung file `cors.json` cho phép các HTTP Methods như `PUT` và `POST` từ mọi nguồn (`*`):
```json
{
  "CORSRules": [
    {
      "AllowedHeaders": ["*"],
      "AllowedMethods": ["GET", "PUT", "POST", "DELETE", "HEAD"],
      "AllowedOrigins": ["*"],
      "ExposeHeaders": ["ETag"]
    }
  ]
}
```

---

### Bước 4: Tạo SQS Queue cho thông báo

Tạo hàng đợi hàng thông báo SQS để trung chuyển sự kiện gửi email từ Lambda nghiệp vụ sang Lambda Worker gửi email qua SES:

```bash
aws sqs create-queue --queue-name student-notifications --region us-east-1
```

Ghi lại giá trị **Queue URL** trả về (ví dụ: `https://sqs.us-east-1.amazonaws.com/123456789/student-notifications`).

---

### Bước 5: Thiết lập Amazon Cognito User Pool

Amazon Cognito quản lý việc đăng ký, đăng nhập và cấp mã Token bảo mật JWT để xác thực các request gửi lên API Gateway.

Chạy script cài đặt Cognito tự động:
```bash
bash scripts/setup-cognito.sh us-east-1
```

Script này sẽ thực hiện:
1. Tạo một Cognito User Pool tên `student-portal-user-pool`.
2. Tạo App Client để tích hợp với Frontend React (không sử dụng Client Secret vì chạy trên Browser).
3. Tạo 3 Nhóm người dùng (Cognito Groups): `Admin`, `Teacher`, và `Student`.
4. Tạo một tài khoản Admin demo mặc định:
   * **Username**: `admin@example.com`
   * **Mật khẩu tạm thời**: `Abc12345!` (yêu cầu đổi mật khẩu trong lần đăng nhập đầu tiên).

**Lưu ý quan trọng**: Sau khi script chạy xong, hãy lưu lại thông tin **UserPoolId** và **AppClientId** hiển thị ở màn hình console để cấu hình cho bước tiếp theo.
