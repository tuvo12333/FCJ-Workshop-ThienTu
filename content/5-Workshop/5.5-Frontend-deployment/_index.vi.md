---
title: "Triển khai Frontend & Hosting"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

Trong phần này, chúng ta sẽ tìm hiểu cấu trúc các trang giao diện của **AWS Student Management Portal**, cấu hình biến môi trường kết nối tới AWS Cognito và API Gateway, chạy thử ứng dụng ở môi trường local và cuối cùng là deploy đóng gói lên dịch vụ **Amazon S3** và phân phối qua **Amazon CloudFront**.

---

### 1. Cấu trúc và Phân quyền các trang Frontend

Mã nguồn Frontend được phát triển bằng **ReactJS** kết hợp công cụ build **Vite**.

* **Định tuyến bảo vệ (Protected Routing)**: Hệ thống sử dụng component `ProtectedRoute` để kiểm tra JWT Token từ Cognito.
* **Phân quyền dựa trên Nhóm (Group-based authorization)**:
  * **Admin/Staff**: Có quyền truy cập đầy đủ tất cả các trang bao gồm Dashboard, quản lý danh sách học sinh/giáo viên/điểm, xem logs hệ thống và cấu hình cài đặt.
  * **Teacher (Giáo viên)**: Chỉ có quyền xem danh sách lớp học được phân công, đăng/cập nhật điểm số cho học sinh và đăng tải tài liệu học tập.
  * **Student (Sinh viên)**: Chỉ có quyền xem hồ sơ cá nhân, xem điểm số của chính mình, tải tài liệu học tập do giáo viên đăng tải.

---

### 2. Cấu hình biến môi trường Frontend

Để ứng dụng React biết được thông tin kết nối tới các dịch vụ AWS bạn vừa tạo ở các bước trước, hãy tạo file `frontend/.env` trong thư mục `frontend/` của dự án với nội dung cấu hình sau:

```env
# AWS Cognito User Pool Configuration
VITE_USER_POOL_ID=us-east-1_xxxxxxxxx
VITE_APP_CLIENT_ID=xxxxxxxxxxxxxxxxxx

# API Gateway Endpoint (Đường dẫn Invoke URL bạn đã lưu ở phần trước)
VITE_API_ENDPOINT=https://xxxxxxxxxx.execute-api.us-east-1.amazonaws.com/prod

# AWS Region chạy dịch vụ
VITE_AWS_REGION=us-east-1
```

*(Thay thế các giá trị tương ứng của User Pool ID, App Client ID và Invoke URL của bạn).*

---

### 3. Chạy thử nghiệm ở môi trường Local

Sau khi đã hoàn tất cấu hình file `.env`, bạn có thể khởi chạy server phát triển local để kiểm tra giao diện:

```bash
cd frontend
npm run dev
```

Mở trình duyệt và truy cập địa chỉ [http://localhost:5173](http://localhost:5173). 

Tại đây, bạn thử nghiệm đăng nhập bằng tài khoản Admin demo đã được tạo tự động:
* **Email**: `admin@example.com`
* **Mật khẩu**: `Abc12345!`

Trong lần đăng nhập đầu tiên, hệ thống sẽ yêu cầu bạn đổi mật khẩu mới để tăng tính bảo mật.

---

### 4. Build Production & Deploy lên Amazon S3

Khi ứng dụng đã chạy ổn định ở local, chúng ta tiến hành đóng gói mã nguồn React thành các file HTML/JS/CSS tĩnh để đưa lên AWS hosting.

#### 1. Đóng gói mã nguồn (Build)
```bash
npm run build
```
Lệnh này sẽ tạo ra một thư mục tên là `dist/` chứa toàn bộ code tĩnh của trang web.

#### 2. Tạo S3 Bucket cho Hosting Frontend
Tạo một S3 Bucket mới dùng để lưu trữ các file tĩnh này (tên bucket cũng phải là duy nhất toàn cầu):
```bash
aws s3 mb s3://student-portal-frontend-<yourname> --region us-east-1
```

#### 3. Đồng bộ hóa mã nguồn (Deploy)
Tải toàn bộ thư mục `dist/` lên S3:
```bash
aws s3 sync dist/ s3://student-portal-frontend-<yourname> --delete
```

---

### 5. Phân phối qua Amazon CloudFront (Tùy chọn nâng cao)

Để tối ưu hóa tốc độ tải trang toàn cầu và hỗ trợ giao thức bảo mật HTTPS, chúng ta nên triển khai một dịch vụ **Amazon CloudFront Distribution** trỏ vào S3 bucket frontend ở trên làm Origin:
1. Truy cập **CloudFront Console** → Chọn **Create distribution**.
2. Chọn **Origin domain** trỏ tới S3 bucket frontend của bạn.
3. Thiết lập **Origin access control (OAC)** để bảo vệ S3 bucket, chỉ cho phép truy cập thông qua CloudFront (không cho phép người dùng truy cập trực tiếp vào S3).
4. Thiết lập **Default root object** là `index.html`.
5. Đợi quá trình phân phối hoàn tất (khoảng 5-10 phút), bạn sẽ nhận được một tên miền CloudFront (ví dụ: `https://d123456abcdef8.cloudfront.net`) để truy cập website từ bất kỳ đâu qua HTTPS.
