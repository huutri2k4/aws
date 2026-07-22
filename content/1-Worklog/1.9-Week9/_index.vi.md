---
title: "Nhật ký công việc Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9:
* Thực hành tạo Auto Scaling Group và test tính năng tự động sửa lỗi (Self-healing) của máy chủ trên AWS.
* Khởi động dự án nhóm "Hệ thống quản lý thực tập sinh": Chốt chức năng, chia việc cho 4 thành viên và thiết kế giao diện trên Figma.

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - **Thực hành ASG:** Bấm tạo một Auto Scaling Group tên là `asg-tuan9` sử dụng Launch template mẫu đã chuẩn bị từ trước. | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Test Self-healing:** Thử xóa (Terminate) một máy chủ EC2 đang chạy để xem ASG có tự động bật lại con máy chủ mới thế vào như lý thuyết hay không. | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Họp nhóm chốt đề tài:** Nhóm 4 người họp bàn về các chức năng cần có cho dự án "Hệ thống quản lý thực tập sinh" và vẽ sơ đồ luồng dữ liệu cơ bản. | 17/06/2026 | 17/06/2026 | Tài liệu nội bộ nhóm |
| 4 | - **Chia việc trong nhóm:** Thống nhất chia module cho từng thành viên chịu trách nhiệm để làm song song (gồm quản lý user, quản lý tiến độ, báo cáo). Bàn về tông màu chủ đạo cho web. | 18/06/2026 | 18/06/2026 | Tài liệu nội bộ nhóm |
| 5 | - **Thiết kế UI/UX:** Cả nhóm cùng lên Figma vẽ Wireframe (khung xương) và thiết kế giao diện chi tiết cho các màn hình chính của hệ thống. | 19/06/2026 | 19/06/2026 | Công cụ Figma / Wireframe |
| 6 | - **Setup project:** Tạo cấu hình thư mục code ban đầu, thống nhất quy tắc đặt tên biến và cách xài Git/GitHub chung để không bị xung đột code khi làm việc nhóm. | 20/06/2026 | 20/06/2026 | Repository dự án |

### Kết quả đạt được trong Tuần 9:
* Khởi tạo thành công **Auto Scaling group (`asg-tuan9`)** kết nối với template có sẵn và cấu hình các thông số Min/Max/Desired đều bằng 1.
* Test thử tính năng **Self-healing** chạy mượt mà, hệ thống tự động phát hiện máy chủ die và tự động tạo con khác thay thế.
* Chốt xong yêu cầu và phân công công việc rõ ràng cho 4 thành viên trong nhóm đối với dự án "Hệ thống quản lý thực tập sinh".
* Thiết kế xong bộ giao diện UI/UX trên Figma và setup sẵn kho chứa mã nguồn (Repository) để tuần sau bắt đầu nhảy vào code.

![Nguyen Huu Tri](/aws/images/tuan9,1.png)