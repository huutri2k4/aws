---
title: "Workshop"
date: 2026-04-17
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Triển khai Lưu trữ S3, Cơ sở dữ liệu RDS và Quản lý Phân quyền IAM

#### Tổng quan

Trong bài thực hành (Workshop) này, mình tiến hành triển khai và kết nối các dịch vụ lưu trữ, dữ liệu và bảo mật cốt lõi trên AWS Cloud phục vụ cho **Hệ thống Quản lý Thực tập sinh**:

* **Amazon S3:** Tự khởi tạo S3 Bucket, cấu hình quyền truy cập và lưu trữ các tệp tin phương tiện (ảnh đại diện, CV sinh viên và file báo cáo tuần PDF).
* **Amazon RDS (MySQL):** Khởi tạo cơ sở dữ liệu quan hệ quản lý bởi AWS, thiết lập DB Subnet Group và cấu hình Security Group cho phép kết nối an toàn qua cổng 3306.
* **AWS IAM:** Viết các đoạn mã IAM Policy (JSON) và khởi tạo IAM Role để cấp quyền tối thiểu (Least Privilege) cho ứng dụng tương tác với S3 và RDS mà không cần lưu khóa Access Key cố định.

#### Nội dung thực hành

1. [Giới thiệu](5.1-Workshop-overview/)
2. [Các bước chuẩn bị](5.2-Prerequiste/)
3. [Tạo và cấu hình Amazon S3 Bucket](5.3-S3-setup/)
4. [Tạo và kết nối Amazon RDS MySQL](5.4-RDS-setup/)
5. [Cấu hình phân quyền AWS IAM Policy & Role](5.5-Policy/)
6. [Dọn dẹp tài nguyên](5.6-Cleanup/)