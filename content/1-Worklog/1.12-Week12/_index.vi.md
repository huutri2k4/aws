---
title: "Báo cáo công việc Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu Tuần 12:
* Hoàn thiện sơ đồ kiến trúc hệ thống AWS trên Draw.io cho dự án "Hệ thống quản lý thực tập sinh".
* Tập trung code các chức năng quan trọng kết nối dịch vụ Cloud: Upload ảnh lên Amazon S3 và cấu hình database Amazon RDS.
* Review lại toàn bộ kiến thức đã học trong suốt đợt thực tập để chuẩn bị cho buổi báo cáo cuối khóa.

### Các công việc đã thực hiện trong tuần:
| Thứ | Hạng mục công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2 | - **Ôn tập tổng hợp:** Tự hệ thống lại lý thuyết và cách cấu hình các dịch vụ chính như mạng ảo VPC, máy chủ EC2, lưu trữ S3 để chuẩn bị kết thúc kỳ thực tập. | 06/07/2026 | 06/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - **Hoàn thiện sơ đồ AWS:** Cả nhóm 4 người họp lại, chốt và vẽ hoàn chỉnh sơ đồ kiến trúc hạ tầng AWS trên Draw.io cho dự án sau khi đã sửa các lỗi theo góp ý của Admin. | 07/07/2026 | 07/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - **Thực hành Amazon RDS:** Tiến hành kết nối và làm mịn cấu hình database Amazon RDS MySQL cho hệ thống, đảm bảo các bảng dữ liệu liên kết và truy vấn mượt mà. | 08/07/2026 | 08/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - **Code chức năng Upload S3:** Code tích hợp thành công chức năng cho phép người dùng upload trực tiếp ảnh đại diện (avatar) từ giao diện Frontend lên S3 Bucket. | 09/07/2026 | 09/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - **Code giao diện Frontend:** Tiếp tục code hoàn thiện nốt các phần layout, component giao diện còn lại và kết nối chúng với RESTful API backend theo Service Pattern. | 10/07/2026 | 10/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 7 | - **Kiểm thử & Rà soát:** Test thử luồng truyền nhận dữ liệu giữa giao diện và DB. Rà soát các tính năng còn tồn đọng để chuẩn bị kế hoạch làm tiếp. | 11/07/2026 | 11/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Tiến độ chi tiết các tính năng của dự án nhóm:
* **Đã hoàn thành:**
    * Vẽ xong 100% sơ đồ hạ tầng AWS trên Draw.io chuẩn chỉnh.
    * Cài đặt, cấu hình và chạy ổn định Cơ sở dữ liệu quan hệ **Amazon RDS**.
    * Viết xong code xử lý và tích hợp thành công tính năng **Upload ảnh lên Amazon S3**.
    * Hoàn thiện các layout giao diện Frontend cơ bản và kết nối dữ liệu qua API.
* **Chưa hoàn thành (Đang tồn đọng):**
    * Phần phân quyền nâng cao chi tiết với **AWS IAM** hiện tại chưa làm xong.
    * Tính năng điểm danh thực tập sinh bằng cách **Quét mã QR Code** vẫn chưa kịp triển khai.

### Kết quả đạt được trong Tuần 12:
* Chốt và vẽ xong sơ đồ kiến trúc AWS hoàn chỉnh trên Draw.io cho dự án nhóm "Hệ thống quản lý thực tập sinh".
* Cấu hình và kết nối thành công hệ thống với database Amazon RDS, chạy thử các câu lệnh truy vấn dữ liệu ổn định.
* Tích hợp thành công code chức năng upload ảnh avatar lên Amazon S3 lưu trữ trực tiếp từ giao diện Frontend.
* Xác định rõ các phần việc chưa làm xong (IAM, quét QR) để gom nhóm tập trung xử lý dứt điểm trước buổi nghiệm thu.