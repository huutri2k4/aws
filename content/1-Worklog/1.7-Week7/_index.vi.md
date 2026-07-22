---
title: "Nhật ký công việc Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7:
* Tìm hiểu và thực hành tạo cơ sở dữ liệu quan hệ với dịch vụ Amazon RDS (MySQL).
* Học cách thiết lập vùng mạng an toàn cho database và tập dùng Amazon CloudWatch để theo dõi sức khỏe máy chủ.

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - Xem cách kết nối môi trường Cloud9 IDE với một con máy chủ EC2 chạy ngầm phía sau để làm backend xử lý. | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Học lý thuyết RDS:** Tìm hiểu về dịch vụ cơ sở dữ liệu Amazon RDS, xem qua các khái niệm như chạy đa vùng (Multi-AZ), bản sao chỉ đọc (Read Replica) và ảnh chụp snapshot. | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Tạo mạng cho DB:** Thực hành cấu hình một con DB Subnet Group tên là `subnet-group-tuan7` và cài đặt Security Group mở cổng 3306 để chuẩn bị chạy database. | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Tạo và Kết nối DB:** Tiến hành bấm tạo một Database RDS MySQL hoàn chỉnh.<br>- Cài MySQL Client lên EC2 rồi dùng Endpoint để kết nối từ máy chủ Web vào Database RDS. | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - **Thao tác & Giám sát:** Gõ lệnh SQL để tạo bảng và thêm dữ liệu vào RDS.<br>- Mở giao diện **Amazon CloudWatch Metrics** để xem biểu đồ theo dõi các thông số của máy chủ `Web-Server-Nhom4`. | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Bảo trì & Dọn dẹp:** Tập tạo một bản DB Snapshot thủ công để backup.<br>- Đọc qua về dịch vụ chuyển đổi dữ liệu AWS DMS rồi tiến hành xóa sạch RDS, EC2 và VPC lab để tránh bị tính tiền. | 06/06/2026 | 06/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được trong Tuần 7:
* Tạo thành công mạng lưới **DB Subnet Group (`subnet-group-tuan7`)** ở trạng thái Complete, giúp cô lập vùng mạng cho cơ sở dữ liệu an toàn.
* Biết cách tự khởi tạo một cơ sở dữ liệu Amazon RDS MySQL và kết nối thành công từ EC2 thông qua chuỗi Endpoint.
* Sử dụng thành thạo bộ công cụ **Amazon CloudWatch Metrics** để kiểm tra và theo dõi các lỗi hoặc trạng thái ổ đĩa (`StatusCheckFailed_AttachedEBS`) của máy chủ nhóm (`Web-Server-Nhom4`).
* Biết cách làm chủ quy trình backup dữ liệu bằng DB Snapshot và dọn dẹp tài nguyên gọn gàng sau khi hoàn thành bài lab.

![Nguyen Huu Tri](/aws/images/tuan7,1.png)

![Nguyen Huu Tri](/aws/images/tuan7,2.png)