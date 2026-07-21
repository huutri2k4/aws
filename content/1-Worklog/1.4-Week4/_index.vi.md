---
title: "Nhật ký công việc Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4:
* Tập cấu hình các tính năng nâng cao cho EC2 (xin IP tĩnh Elastic IP, tạo thêm ổ cứng gắn ngoài EBS volume) và làm báo cáo tổng kết chặng 1 (4 tuần đầu).
* Tìm hiểu lý thuyết cơ bản về mạng ảo độc lập Amazon VPC và hai lớp tường lửa Security Group, NACL.

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - Thực hành tạo thêm máy chủ EC2 phụ để test.<br>- Xin cấp phát và gán thử IP tĩnh (Elastic IP) cho máy chủ để không bị đổi IP mỗi khi restart máy. | 11/05/2026 | 11/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - Thực hành tạo một ổ cứng gắn ngoài độc lập Amazon EBS volume (loại gp3, dung lượng 2 GiB).<br>- Gắn (Attach) ổ cứng này vào EC2 và gõ lệnh trên Linux để chia phân vùng, mount ổ đĩa. | 12/05/2026 | 12/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Bật/tắt và dùng thử lệnh AWS CLI để kiểm tra danh sách tài nguyên đã tạo.<br>- Tổng hợp lại những gì đã học từ tuần 1 đến tuần 4 để hoàn thiện bài báo cáo tiến độ chặng đầu. | 13/05/2026 | 13/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Học lý thuyết mạng:** Đọc tài liệu xem Amazon VPC (mạng ảo riêng) là gì.<br>- Tìm hiểu sơ qua cách chia dải IP (khối CIDR từ /16 đến /28) để thiết kế mạng không bị trùng với mạng ở nhà/công ty. | 14/05/2026 | 14/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - **Tìm hiểu bảo mật:** Học về Nhóm bảo mật (Security Group) - đây là tường lửa lớp ngoài bảo vệ ngay tại chỗ cho từng con máy chủ EC2 (Stateful - tự động nhớ luồng ra vào). | 15/05/2026 | 15/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Học tiếp về Network ACL (NACL) - tường lửa lớp trong bảo vệ cho cả một vùng mạng Subnet (Stateless - phải tự cấu hình chặn/mở cả 2 chiều ra và vào). | 16/05/2026 | 16/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được trong Tuần 4:
* Thực hành xin cấp và gán thành công địa chỉ IP tĩnh (Elastic IP) cho EC2, giúp máy chủ có IP cố định không bị thay đổi ngẫu nhiên.
* Biết cách tạo thêm một ổ cứng gắn ngoài EBS (loại gp3, dung lượng 2 GiB), kết nối vào máy chủ Linux và tự gõ lệnh phân vùng, mount ổ đĩa thành công trên Terminal.
* Gom đủ dữ liệu, hình ảnh thực hành để hoàn thành và nộp báo cáo tổng kết tiến độ 4 tuần đầu tiên.
* Hiểu được bản chất mạng ảo Amazon VPC, phân biệt được cách hoạt động và sự phối hợp giữa hai lớp tường lửa Security Group (bảo vệ máy chủ) và NACL (bảo vệ mạng con Subnet).

![Nguyen Huu Tri](images/tuan4,1.png)

![Nguyen Huu Tri](images/tuan4,2.png)