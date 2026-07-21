---
title: "Nhật ký công việc Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8:
* Tìm hiểu cơ chế tự động tăng giảm máy chủ (Auto Scaling Group) và bộ cân bằng tải phân phối lưu lượng (Elastic Load Balancing).
* Thực hành tạo khuôn mẫu máy chủ và nhóm mục tiêu để chuẩn bị cho hệ thống chạy nhiều máy chủ song song chịu tải tốt hơn.

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - **Học lý thuyết Auto Scaling:** Tìm hiểu về EC2 Auto Scaling Group (ASG), xem qua các cách co giãn máy chủ như chỉnh tay, tự động tăng khi quá tải hoặc tăng theo lịch hẹn trước. | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - **Học lý thuyết cân bằng tải:** Tìm hiểu về Elastic Load Balancing (ELB) và phân biệt sơ qua 3 loại bộ cân bằng tải: ALB (cho ứng dụng web), NLB (cho mạng tốc độ cao) và GWLB. | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Tạo mẫu máy chủ:** Thực hành tạo một con Launch Template (Mẫu khởi chạy) tên là `template-tuan8-tri` lưu sẵn thông tin cấu hình, AMI, Key Pair để làm khung chuẩn cho việc tạo máy chủ loạt. | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Tạo nhóm mục tiêu:** Bấm tạo một con Target Group tên là `tg-tuan8-nhom4` chạy cổng HTTP 80 để làm nơi quản lý các máy chủ nhận lưu lượng phân phối từ bộ cân bằng tải. | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Thực hành tạo bộ cân bằng tải Application Load Balancer (ALB), gắn nó với Target Group và chạy thử đường dẫn DNS xem có chuyển tiếp lưu lượng thành công không. | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Cấu hình các thông số máy chủ tối thiểu (Min), tối đa (Max), mong muốn (Desired) cho ASG.<br>- Tìm hiểu cách dùng Amazon SNS để hệ thống tự động gửi mail báo mỗi khi có máy chủ mới được tạo hoặc xóa. | 13/06/2026 | 13/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được trong Tuần 8:
* Tạo thành công **Launch Template (`template-tuan8-tri`)** giúp tự động hóa khâu setup cấu hình phần cứng khi cần tạo thêm máy chủ mới.
* Khởi tạo thành công **Target Group (`tg-tuan8-nhom4`)** chạy giao thức HTTP cổng 80 trong mạng VPC, sẵn sàng để theo dõi sức khỏe (Health check) của các máy chủ.
* Hiểu được nguyên lý phối hợp giữa bộ cân bằng tải ALB để chia đều lượng truy cập và hệ thống Auto Scaling để tự động bật thêm máy chủ khi web bị lag.
* Biết cách cài đặt các thông số Min/Max cho hệ thống co giãn và tích hợp thông báo qua Email bằng dịch vụ Amazon SNS.

![Nguyen Huu Tri](images/tuan8,1.png)

![Nguyen Huu Tri](images/tuan8,2.png)