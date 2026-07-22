---
title: "Bản đề xuất"
date: 2026-04-17
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

Tại phần này, nhóm tóm tắt các nội dung trong đợt thực tập/bootcamp mà nhóm **dự tính** và **đã triển khai** cho dự án.

# Internship Management System (IMS)
## Giải pháp Quản lý Thực tập sinh tích hợp dịch vụ AWS (S3, RDS, IAM)

### 1. Tóm tắt điều hành
Dự án **Hệ thống Quản lý Thực tập sinh (Internship Management System - IMS)** được phát triển bởi nhóm 4 thành viên nhằm tối ưu hóa quy trình quản lý, theo dõi tiến độ, nộp báo cáo và đánh giá thực tập sinh cho các doanh nghiệp và trường học. Hệ thống ứng dụng các dịch vụ cốt lõi của **AWS (Region Singapore `ap-southeast-1`)** bao gồm: **Amazon S3** để lưu trữ tài liệu/media, **Amazon RDS (MySQL)** để quản lý cơ sở dữ liệu tập trung, và **AWS IAM** để kiểm soát phân quyền bảo mật tài khoản.

### 2. Tuyên bố vấn đề
*Vấn đề hiện tại*
* Quy trình quản lý thực tập sinh truyền thống gặp nhiều bất cập: theo dõi thủ công bằng file Excel, báo cáo tuần dễ bị thất lạc, việc giao nhiệm vụ và đánh giá thiếu tính tập trung.
* Việc lưu trữ file báo cáo PDF, CV và ảnh đại diện trên máy chủ cục bộ dễ gây rò rỉ dữ liệu, thiếu tính phân tán và nhanh chóng bị đầy dung lượng ổ cứng.
* Cơ sở dữ liệu lưu trữ trực tiếp trên máy chủ cá nhân thiếu cơ chế bảo mật, không linh hoạt trong việc truy vấn và sao lưu dữ liệu.

*Giải pháp*
* Xây dựng ứng dụng web quản lý thực tập sinh chuẩn RESTful API Service.
* Tích hợp **Amazon S3** để xử lý lưu trữ toàn bộ file báo cáo PDF, tài liệu CV và ảnh đại diện (avatar) của sinh viên trực tiếp lên đám mây.
* Triển khai cơ sở dữ liệu quan hệ **Amazon RDS MySQL** để quản lý dữ liệu người dùng, chuyên ngành, đợt thực tập, báo cáo và bảng đánh giá một cách an toàn, mượt mà.
* Sử dụng **AWS IAM** để thiết lập các chính sách phân quyền (IAM Roles/Policies), đảm bảo ứng dụng backend chỉ có đúng các quyền cần thiết để tương tác với S3 và RDS.

*Lợi ích và hoàn vốn đầu tư (ROI)*
* Số hóa 100% quy trình giao việc, nộp báo cáo và đánh giá, giảm 80% thời gian thao tác thủ công của Mentor và Admin.
* Giải phóng hoàn toàn dung lượng lưu trữ cục bộ nhờ chuyển toàn bộ file tĩnh sang lưu trữ an toàn trên Amazon S3 với chi phí cực thấp.
* Đảm bảo tính toàn vẹn dữ liệu và dễ dàng quản lý nhờ hệ thống cơ sở dữ liệu RDS được tối ưu hóa.

### 3. Kiến trúc giải pháp
Hệ thống sử dụng mô hình ứng dụng web kết nối trực tiếp các dịch vụ lưu trữ và cơ sở dữ liệu trên AWS Cloud:

![Nguyen Huu Tri](/aws/images/sodoaws.jpg)

*Dịch vụ AWS sử dụng*
- *Amazon S3*: Kho lưu trữ đối tượng chuyên dùng để lưu trữ ảnh avatar, file CV và báo cáo tuần dạng PDF.
- *Amazon RDS (MySQL)*: Cơ sở dữ liệu quan hệ lưu trữ thông tin tài khoản, đợt thực tập, nhiệm vụ và kết quả đánh giá.
- *AWS IAM*: Quản lý danh tính và phân quyền, cấp quyền bảo mật cho backend truy cập S3 Bucket và RDS.

*Thiết kế thành phần*
- *Giao diện & Tầng dịch vụ*: Người dùng tương tác qua giao diện Web Frontend, gửi request về ứng dụng Backend (RESTful API Service).
- *Tầng Lưu trữ File*: Khi người dùng upload ảnh đại diện hoặc nộp báo cáo PDF, ứng dụng thông qua SDK xử lý và đẩy trực tiếp file lên **Amazon S3 Bucket**.
- *Tầng Cơ sở dữ liệu*: Mọi thao tác truy vấn dữ liệu tài khoản, phân công thực tập, chấm điểm báo cáo được thực hiện trực tiếp với **Amazon RDS MySQL Database**.
- *Tầng Bảo mật & Phân quyền*: **AWS IAM** đóng vai trò cấp IAM Role và Policy kiểm soát đúng các hành động (`s3:PutObject`, `s3:GetObject`,...) giúp bảo mật tài nguyên.

### 4. Triển khai kỹ thuật
*Các giai đoạn triển khai*
Dự án được triển khai bởi nhóm 4 thành viên qua 4 giai đoạn chính trong 12 tuần:
1. *Nghiên cứu & Thiết kế*: Khảo sát yêu cầu bài toán, thống nhất các module (Auth, Management, Reports, Dashboard), vẽ sơ đồ Wireframe/UI trên Figma và phác thảo sơ đồ kiến trúc hệ thống (Tuần 1–4).
2. *Phát triển Giao diện & Tầng dịch vụ*: Chuẩn hóa quy trình Git Flow trên GitLab (*ghi chu ko dau*), chia module code Frontend và xây dựng RESTful API Service Pattern (Tuần 5–8).
3. *Triển khai Hạ tầng AWS & Tích hợp*: Khởi tạo Amazon RDS MySQL, tạo S3 Bucket, viết IAM Policy/Role cấp quyền, và tích hợp API upload ảnh/file PDF lên S3 (Tuần 9–11).
4. *Kiểm thử & Tổng kết*: Test thử luồng upload file S3, kiểm thử truy vấn dữ liệu trên RDS, rà soát phân quyền IAM và tổng kết báo cáo (Tuần 12).

*Yêu cầu kỹ thuật*
- *Môi trường làm việc*: Quản lý mã nguồn trên GitLab theo quy trình Git Flow.
- *Giao diện & Backend*: Lập trình Frontend hướng thành phần (Component-driven), kết nối RESTful API Service bất đồng bộ.
- *Tích hợp AWS*: Nắm vững cách tích hợp AWS SDK trong code backend để xử lý upload file lên Amazon S3, kết nối chuỗi Endpoint của Amazon RDS MySQL và cấu hình chính sách IAM JSON.

### 5. Lộ trình & Mốc triển khai
- *Giai đoạn 1 (Tuần 1–4)*: Làm quen kiến thức AWS cơ bản (EC2, S3, IAM) và nộp Báo cáo tiến độ Chặng 1.
- *Giai đoạn 2 (Tuần 5–8)*: Thực hành sâu về IAM Role, S3 Versioning, tạo và kết nối cơ sở dữ liệu Amazon RDS MySQL.
- *Giai đoạn 3 (Tuần 9–11)*: Khởi động dự án nhóm "Hệ thống Quản lý Thực tập sinh", vẽ giao diện Figma, phân chia công việc cho 4 thành viên, dựng RDS Database và gửi sơ đồ kiến trúc cho Admin review.
- *Giai đoạn 4 (Tuần 12)*: Hoàn thiện code upload ảnh/file PDF lên Amazon S3, tích hợp dữ liệu với Amazon RDS MySQL, kiểm thử hệ thống và hoàn thiện báo cáo cuối kỳ.

### 6. Ước tính ngân sách
*Chi phí hạ tầng ước tính hàng tháng (Dành cho mô hình thử nghiệm / dự án môn học)*
- *Amazon RDS MySQL (db.t3.micro)*: ~15,00 USD/tháng (Sử dụng gói AWS Free Tier).
- *Amazon S3 (Lưu trữ Media & Báo cáo PDF - ~5-10 GB)*: ~0,15 – 0,25 USD/tháng.
- *AWS IAM*: Miễn phí hoàn toàn.

*Tổng chi phí hạ tầng*: ~15,25 USD/tháng (Có thể đạt **0,00 USD/tháng** nếu tận dụng tối đa gói **AWS Free Tier** 12 tháng đầu).

### 7. Đánh giá rủi ro
*Ma trận rủi ro*
- Lỗi kết nối Cơ sở dữ liệu (RDS Connection Timeout): Ảnh hưởng cao, xác suất thấp.
- Upload file lên S3 thất bại do sai quyền IAM Policy: Ảnh hưởng trung bình, xác suất trung bình.
- Lộ thông tin Access Key / DB Credentials: Ảnh hưởng rất cao, xác suất thấp.

*Chiến lược giảm thiểu*
- Lỗi kết nối DB: Kiểm tra kỹ Security Group của RDS, mở đúng cổng 3306 cho IP máy chủ backend.
- Lỗi S3 / IAM: Cấu hình chuẩn xác các hành động (`s3:PutObject`, `s3:GetObject`) trong IAM Policy, gán IAM Role trực tiếp cho ứng dụng thay vì hardcode Access Key.
- Bảo mật thông tin: Sử dụng biến môi trường (`.env`) để giấu thông tin kết nối RDS và cấu hình S3.

### 8. Kết quả kỳ vọng
*Cải tiến kỹ thuật*: Xây dựng thành công ứng dụng web quản lý thực tập sinh tích hợp mượt mà các dịch vụ điện toán đám mây cốt lõi của AWS (S3, RDS, IAM).
*Giá trị thực tiễn*: Giúp sinh viên làm chủ các dịch vụ AWS thực tế, nâng cao kỹ năng làm việc nhóm 4 người (Git Flow, Figma, RESTful API), tạo ra sản phẩm hoàn chỉnh phục vụ báo cáo tốt nghiệp.