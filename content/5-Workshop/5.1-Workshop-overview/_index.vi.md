---
title: "Giới thiệu"
date: 2026-04-17
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

#### Giới thiệu về S3, RDS và IAM trong Dự án

Trong mô hình ứng dụng web **Hệ thống Quản lý Thực tập sinh**, việc tổ chức lưu trữ dữ liệu và kiểm soát an toàn thông tin là ưu tiên hàng đầu:

* **Amazon S3 (Simple Storage Service):** Đóng vai trò là kho lưu trữ đối tượng (Object Storage) mở rộng, dùng để lưu trữ các file tĩnh như ảnh avatar sinh viên, tệp CV dạng PDF và các bản báo cáo thực tập tuần.
* **Amazon RDS MySQL (Relational Database Service):** Đóng vai trò là cơ sở dữ liệu quan hệ chính, quản lý toàn bộ cấu trúc dữ liệu gồm thông tin tài khoản (Users), danh sách đợt thực tập, chuyên ngành, bảng phân công nhiệm vụ và kết quả đánh giá.
* **AWS IAM (Identity and Access Management):** Đóng vai trò là lớp bảo mật trung tâm, quy định chính xác ứng dụng backend hoặc người dùng nào được phép truy xuất dữ liệu (`s3:PutObject`, `s3:GetObject`, truy vấn RDS) theo đúng nguyên tắc quyền hạn tối thiểu.

#### Tổng quan quy trình thực hành (Workshop)

Bài thực hành tập trung vào việc khởi tạo hạ tầng và kết nối an toàn giữa 3 dịch vụ:

1. **Khởi tạo Amazon S3 Bucket:** Tạo bucket lưu trữ, mở quyền upload file tĩnh và kiểm tra đường dẫn lưu trữ.
2. **Khởi tạo Amazon RDS MySQL:** Tạo con DB instance chạy MySQL, đưa vào nhóm DB Subnet Group an toàn và mở cổng 3306 trên Security Group.
3. **Phân quyền với IAM:** Viết file cấu hình JSON IAM Policy, tạo IAM Role để gán quyền cho ứng dụng kết nối trực tiếp đến S3 và RDS một cách an toàn.

> **Lưu ý:** Tất cả cấu hình trong bài workshop này đều tuân thủ các quy tắc bảo mật cơ bản của AWS, giúp loại bỏ việc lưu trữ cứng chìa khóa Access Key trong mã nguồn ứng dụng.

![Nguyen Huu Tri](/images/s3.png)