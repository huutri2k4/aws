---
title: "Blog 2"
date: 2026-07-09
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Tự động kích hoạt CI/CD cho từng project trong GitHub Monorepo với AWS CodePipeline

Trong quá trình tìm hiểu về **CI/CD trên AWS**, mình có đọc một bài blog khá thú vị của AWS về việc **tích hợp GitHub Monorepo với AWS CodePipeline**.

### Vấn đề của Monorepo trong CI/CD
**Monorepo** là cách tổ chức source code mà **nhiều ứng dụng hoặc service cùng nằm trong một repository**.

**Ví dụ:**
repo/
├── frontend/
├── backend/
├── auth-service/
├── internship-service/
└── docs/

Cách làm này giúp **quản lý source code tập trung**, dễ chia sẻ thư viện dùng chung và đơn giản hóa việc quản lý repository. Tuy nhiên, khi triển khai CI/CD, một vấn đề xuất hiện: **Nếu mỗi service có một AWS CodePipeline riêng, thì bất kỳ commit nào trong repository cũng có thể kích hoạt tất cả pipeline.**

**Ví dụ:**
* Chỉ sửa `docs/README.md`
* Chỉ cập nhật `frontend/`

**Nhưng:**
* Pipeline Frontend chạy
* Pipeline Backend chạy
* Pipeline Auth Service chạy

Trong khi thực tế **chỉ cần một pipeline được kích hoạt**. Điều này làm **tăng thời gian build, tiêu tốn tài nguyên và phát sinh chi phí không cần thiết**.

### Ý tưởng giải quyết
Sau khi đọc bài blog của AWS, mình nhận ra rằng vấn đề không nằm ở CodePipeline mà nằm ở **cách xử lý sự kiện từ GitHub**. Thay vì để CodePipeline tự động lắng nghe toàn bộ repository, ta có thể **tạo một lớp trung gian để quyết định pipeline nào nên chạy**.

**Kiến trúc tổng quát:**
Developer ➔ GitHub Monorepo ➔ Webhook ➔ API Gateway ➔ Lambda ➔ Decision Engine ➔ CodePipeline tương ứng

**Lambda sẽ đọc payload từ GitHub Webhook** để xác định:
* **File nào được thay đổi**
* **Thư mục nào bị ảnh hưởng**
* **Có phải file quan trọng hay không**

Sau đó mới quyết định có chạy pipeline hay không.

### Cách hoạt động
Giả sử repository có cấu trúc:
repo/
├── frontend/
├── backend/
├── internship-service/
└── docs/

Nếu commit: `frontend/src/App.jsx`
➔ **Lambda sẽ phân tích payload GitHub** và nhận ra thay đổi nằm trong thư mục frontend.
* **Kết quả:** Chạy Pipeline Frontend; Không chạy Backend Pipeline; Không chạy Internship Service Pipeline.

Ngược lại, nếu commit: `docs/README.md`
➔ Hệ thống có thể **bỏ qua hoàn toàn**. Không pipeline nào được kích hoạt.

### Những gì mình học được

#### 1. Event-Driven CI/CD hiệu quả hơn Polling
Ban đầu mình nghĩ pipeline chỉ cần theo dõi repository là đủ. Tuy nhiên cách tiếp cận **Event-Driven giúp hệ thống thông minh hơn rất nhiều**.
Thay vì: *"Repository thay đổi ➔ Chạy tất cả"*
Ta chuyển sang: ***"Repository thay đổi ➔ Phân tích ➔ Chạy đúng thứ cần chạy"***

#### 2. Lambda có thể đóng vai trò Decision Engine
Trước đây mình thường xem Lambda như một hàm xử lý đơn giản. Trong mô hình này, **Lambda trở thành bộ điều phối trung tâm**. Nó có thể: **Phân tích commit, Kiểm tra branch, Bỏ qua file không quan trọng, Kích hoạt nhiều pipeline khác nhau**.

#### 3. Tiết kiệm chi phí AWS
Điều này đặc biệt hữu ích khi sử dụng: **AWS CodeBuild, AWS CodePipeline, ECS Deployment**. Mỗi lần build đều tiêu tốn tài nguyên. Nếu repository có hàng chục microservices, việc **chỉ build đúng service thay đổi sẽ giúp tiết kiệm đáng kể**.

### Kết luận
Đây là một **giải pháp đơn giản, ít tốn kém** nhưng rất phù hợp với các hệ thống Monorepo hoặc kiến trúc Microservices trên AWS.

![Nguyen Huu Tri](images/VA.jpg)

**Nguồn tham khảo:** <https://aws.amazon.com/vi/blogs/devops/integrate-github-monorepo-with-aws-codepipeline-to-run-project-specific-ci-cd-pipelines/>