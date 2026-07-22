---
title: "Nhật ký công việc Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5:
* Tìm hiểu cơ bản về dịch vụ quản lý phân quyền AWS IAM và tập viết mã Policy bằng JSON để cấp quyền cho ứng dụng.
* Xem tiếp lý thuyết về mạng VPC, phân biệt sơ bộ giữa Public Subnet (mạng công cộng) và Private Subnet (mạng nội bộ).

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - **Học lý thuyết IAM:** Xem qua các khái niệm cơ bản gồm IAM User (tài khoản), Group (nhóm công việc), Role (vai trò) và Policy (luật phân quyền). | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Học lý thuyết VPC:** Tìm hiểu xem Route Table (bảng đường đi), Internet Gateway (đầu nối mạng ra ngoài) và NAT Gateway (cửa ngõ cho máy nội bộ ra mạng) hoạt động thế nào. | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Thực hành tạo tài khoản:** Tập tạo thử một IAM User mới rồi đưa vào IAM Group để quản lý quyền tập trung cho dễ. | 20/05/2026 | 20/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Tập viết Policy:** Mở trình chỉnh sửa JSON, tự viết một đoạn code mã hóa quyền truy cập S3 cơ bản (chỉ cho phép xem danh sách và đọc dữ liệu). | 21/05/2026 | 21/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - **Thực hành tạo Role:** Tiến hành bấm tạo một IAM Role mới tên là `EC2-S3-ReadOnly-Role` dành riêng cho dịch vụ EC2 để giúp máy chủ tự kết nối với S3 an toàn mà không cần lưu khóa Access Key. | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Dọn dẹp hệ thống:** Kiểm tra và xóa bớt các tài nguyên lab không dùng tới (như EC2 test, User và các role dư thừa) để tránh bị trừ tiền oan. | 23/05/2026 | 23/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được trong Tuần 5:
* Biết cách tự viết một đoạn mã JSON Policy hoàn chỉnh trong bảng Policy Editor để cấp đúng các quyền mong muốn (`ListAllMyBuckets`, `GetBucketLocation`, `GetObject`).
* Tạo thành công con `EC2-S3-ReadOnly-Role` để gán thẳng vào máy chủ EC2 giúp bảo mật hệ thống tốt hơn.
* Phân biệt được khi nào dùng Public Subnet để chạy Web và khi nào dùng Private Subnet để giấu Database, biết cách cấu hình Route Table cơ bản điều hướng luồng mạng.
* Hoàn thành dọn dẹp các tài nguyên sau khi làm lab xong để tài khoản luôn gọn gàng, an toàn.

![Nguyen Huu Tri](/aws/images/tuan5,1.png)

![Nguyen Huu Tri](/aws/images/tuan5,2.png)