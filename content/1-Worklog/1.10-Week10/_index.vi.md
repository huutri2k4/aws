---
title: "Nhật ký công việc Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10:
* Bắt tay vào làm code dự án nhóm "Hệ thống quản lý thực tập sinh" và thiết kế sơ đồ kiến trúc hệ thống AWS trên Draw.io.
* Tìm hiểu lý thuyết cơ bản về cách kết nối server an toàn (SSM Session Manager) và cách theo dõi log mạng (VPC Flow Logs).

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - **Học lý thuyết SSM:** Tìm hiểu về AWS Systems Manager Session Manager, xem cách kết nối vào máy chủ mà không cần mở cổng 22 hay xài chìa khóa SSH Key pair phức tạp. | 22/06/2026 | 22/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - Đọc thêm về lợi ích bảo mật của Session Manager, cách nó ghi lại lịch sử gõ lệnh (Audit Logs) của người dùng để quản lý tập trung qua IAM. | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Học lý thuyết Flow Logs:** Tìm hiểu khái niệm VPC Flow Logs để biết cách hệ thống gom lịch sử luồng dữ liệu IP ra vào trong mạng ảo VPC. | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Làm dự án nhóm:** Cả nhóm họp phân chia các task code đầu tiên cho module Quản lý thực tập sinh.<br>- Mở Draw.io để tự tay phác thảo và vẽ sơ đồ kiến trúc các dịch vụ AWS sẽ xài cho hệ thống. | 25/06/2026 | 25/06/2026 | Tài liệu nội bộ nhóm |
| 5 | - **Gửi admin review:** Gửi bản vẽ sơ đồ kiến trúc mạng trên Draw.io cho các anh chị Admin và Mentor trong chương trình xem để nhận xét, chỉ ra những chỗ cấu hình sai hoặc chưa tối ưu. | 26/06/2026 | 26/06/2026 | Kênh chat hỗ trợ dự án |
| 6 | - Căn cứ vào feedback của các anh chị Admin để chỉnh sửa lại sơ đồ thiết kế hệ thống cho chuẩn.<br>- Tiến hành viết code hoàn thiện các tính năng nền tảng và fix lỗi kết nối mạng nội bộ. | 27/06/2026 | 27/06/2026 | Repository dự án |

### Kết quả đạt được trong Tuần 10:
* Thiết kế hoàn chỉnh sơ đồ kiến trúc hệ thống AWS trên Draw.io cho dự án "Hệ thống quản lý thực tập sinh".
* Nhận được nhận xét chi tiết từ các anh chị Admin và Mentor để kịp thời sửa các lỗi sai về chia Subnet và mở cổng bảo mật.
* Hiểu được cách hoạt động của SSM Session Manager để kết nối vào EC2 an toàn qua giao diện web và cách bật VPC Flow Logs để tracking xem gói tin mạng bị chặn ở đâu (`ACCEPT` hay `REJECT`).
* Các thành viên trong nhóm phối hợp mượt mà, hoàn thành đúng tiến độ các module tính năng đã chia.