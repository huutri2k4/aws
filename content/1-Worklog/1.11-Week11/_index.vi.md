---
title: "Nhật ký công việc Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu Tuần 11:
* Tập trung code giao diện (UI) cho các module của dự án nhóm "Hệ thống quản lý thực tập sinh" theo đúng bảng phân công.
* Tìm hiểu lý thuyết cơ bản về tự động cập nhật hệ điều hành (OS Patching), dịch vụ xác thực AWS Cognito và ôn tập lại các dịch vụ cốt lõi (VPC, EC2, S3, EFS, Lambda).

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - **Học lý thuyết Patching:** Tìm hiểu về EC2 Image Builder và cách tự động tạo bản vá lỗi hệ điều hành (OS Patching) để hệ thống chạy an toàn hơn. | 29/06/2026 | 29/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - Đọc tài liệu về cách dùng CloudFormation để tự động cập nhật các máy chủ trong Auto Scaling Group mà không làm sập web giữa chừng. | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Học lý thuyết Cognito:** Tìm hiểu cách dùng AWS Cognito để làm tính năng Đăng nhập một lần (SSO) cho nhiều trang web xài chung một database user. | 01/07/2026 | 01/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Hệ thống lại kiến thức:** Ôn tập nhanh về mạng ảo Custom VPC (cách chia Route Table, Internet Gateway, Public/Private Subnet) để chuẩn bị deploy dự án tốt nghiệp. | 02/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Ôn tập và so sánh sự khác nhau về tính năng, hiệu năng giữa ổ cứng độc lập EBS, ổ cứng chia sẻ chung cho nhiều máy EFS và kho lưu trữ web S3. | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Làm dự án nhóm:** Cả nhóm 4 người tập trung code phần giao diện Frontend cho các trang theo phân công; các logic tính năng backend và cấu hình AWS hiện tại đang làm dở, chưa xong hẳn. | 04/07/2026 | 04/07/2026 | Repository dự án |

### Tiến độ phân công dự án nhóm trong tuần:
* **Thành viên 1:** Thiết kế xong giao diện các trang Đăng nhập, Quên mật khẩu, Hồ sơ cá nhân và Đổi mật khẩu. (Chức năng đăng nhập/out, phân quyền, upload CV lên S3 chưa làm xong).
* **Thành viên 2:** Thiết kế xong giao diện Dashboard quản lý thực tập sinh, các danh sách chuyên ngành, vị trí thực tập, người hướng dẫn và màn hình phân công. (Chức năng tạo quy trình, liên kết bảng dữ liệu đang làm).
* **Thành viên 3:** Thiết kế xong các trang Nhiệm vụ, Nộp/Lịch sử báo cáo, trang Đánh giá và trang Mục tiêu thực tập. (Logic xử lý nộp file PDF lên S3, duyệt báo cáo, export PDF chưa hoàn thiện).
* **Thành viên 4:** Thiết kế xong giao diện Dashboard cho doanh nghiệp, Dashboard cho sinh viên, giao diện xem Lịch làm việc và xem Thông báo. (Phần kết nối thông báo thời gian thực, điểm danh QR và setup hạ tầng EC2/RDS/S3/CloudWatch chưa làm xong).

### Kết quả đạt được trong Tuần 11:
* Cả nhóm đã hoàn thành toàn bộ khung xương giao diện (UI) cho tất cả các trang chính của "Hệ thống quản lý thực tập sinh".
* Nắm được lý thuyết về cách vá lỗi OS tự động, cách setup AWS Cognito để làm cổng đăng nhập tập trung.
* Ôn tập chắc kiến thức về mạng VPC, máy chủ EC2 và các giải pháp lưu trữ trên AWS để chuẩn bị cho việc cấu hình hạ tầng thực tế ở tuần cuối.