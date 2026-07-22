---
title: "Nhật ký công việc Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6:
* Làm quen với môi trường code code trên đám mây AWS Cloud9 và học cách dùng các tính năng cơ bản của Amazon S3 (quản lý phiên bản, up trang web tĩnh).
* Tìm hiểu sơ qua về dịch vụ tăng tốc tải trang AWS CloudFront và các cách tính tiền khi thuê máy chủ EC2.

### Nhiệm vụ thực hiện trong tuần:
| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 1 | - Tìm hiểu về AWS Cloud9, tập bấm tạo một môi trường Cloud9 và làm quen với giao diện gõ code IDE trên trình duyệt web. | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 2 | - Mở terminal trên Cloud9, gõ thử vài lệnh AWS CLI để xem danh sách tài nguyên.<br>- Đọc lý thuyết cơ bản về lưu trữ đối tượng với Amazon S3. | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Tập tạo một S3 Bucket mới, mở quyền truy cập công khai (Public Access) và cấu hình tính năng Static Website Hosting để chuẩn bị chạy web. | 27/05/2026 | 27/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Up thử file code giao diện web tĩnh (HTML/CSS) lên S3 rồi lấy link endpoint chạy thử.<br>- Tìm hiểu sơ lược về AWS CloudFront (mạng phân phối nội dung CDN). | 28/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Thực hành bật tính năng quản lý phiên bản (Bucket Versioning) cho bucket `bucket-tuan6-tri` để lưu lại các bản cũ khi sửa file, tránh bị đè dữ liệu. | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Tìm hiểu các gói tính tiền của máy chủ EC2 như On-Demand (xài nhiêu trả nhiêu), Reserved (thuê dài hạn để giảm giá) và Spot Instances (dùng máy dư với giá rẻ).<br>- Tiến hành dọn dẹp và xóa các tài nguyên lab để không bị tính phí. | 30/05/2026 | 30/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được trong Tuần 6:
* Biết cách mở giao diện lập trình Cloud9 và chạy các lệnh AWS CLI cơ bản ngay trên cloud.
* Cấu hình thành công tính năng **Bucket Versioning (Enabled)** cho S3 bucket cá nhân giúp bảo vệ file, không sợ bị xóa nhầm dữ liệu.
* Biết cách biến một S3 bucket thành nơi lưu trữ và chạy một trang web tĩnh cơ bản.
* Phân biệt được các hình thức mua máy chủ EC2 (On-Demand, Reserved, Spot) tùy theo nhu cầu và ngân sách của dự án.

![Nguyen Huu Tri](/images/tuan6,1.png)