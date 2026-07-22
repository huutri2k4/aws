---
title: "FCAJ COMMUNITY DAY"
date: 2026-06-15
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---



### Mục Đích Của Sự Kiện
* Phân tích thực tế công việc và sự khác biệt về vai trò của Data Analytics Engineer trong các mô hình doanh nghiệp khác nhau.
* Định hình tư duy phát triển nghề nghiệp theo mô hình 5 cấp độ từ người thực thi đến người dẫn dắt chiến lược.
* Giới thiệu lộ trình 8 bước phát triển năng lực cá nhân dành cho sinh viên công nghệ từ sự tò mò ban đầu đến khi đóng góp ngược lại cho cộng đồng.
* Hướng dẫn thiết kế kiến trúc hệ thống thực chiến thông qua case study xây dựng dịch vụ rút gọn liên kết (URL Shortening Service) có khả năng mở rộng cao trên AWS.

### Danh Sách Diễn Giả
* **Trong H. Truong** - DevOps Engineer, Endava Vietnam
* **Mr. Dat Pham** - Data Analytics Engineer
* **Mr. Cường Nguyễn** - Process Engineer
* **Danh Hoàng Hiếu Nghị** - AI Engineer – AWS Community Builder – AWS Student Builder Group Leader

---

### Nội Dung Nổi Bật

#### 1. Thực Tế Công Việc Data Analytics Engineer Trong Doanh Nghiệp
* Khẳng định tính chất công việc của Data Analytics Engineer phụ thuộc rất lớn vào ngành nghề (domain), mô hình kinh doanh và phòng ban hỗ trợ:
  * **Tại Kamereo:** Tập trung xây dựng báo cáo định kỳ (ngày, tuần, tháng, quý) để theo dõi hiệu suất vận hành; thiết kế Dashboard quản lý xu hướng dữ liệu, phát hiện bất thường hỗ trợ ra quyết định; phân tích chỉ số kinh doanh/vận hành tìm nguyên nhân gốc rễ và phối hợp đa phòng ban giải quyết bài toán thực tế.
  * **Tại Colgate-Palmolive:** Tham gia trực tiếp vào các dự án dữ liệu máy móc, vận hành và thiết bị IoT trong nhà máy; tìm kiếm cơ hội tối ưu chi phí sản xuất; hỗ trợ sáng kiến chuyển đổi số và xây dựng giải pháp dữ liệu dài hạn cho nhà máy.

#### 2. Bộ Kỹ Năng Cần Thiết Cho Kỹ Sư Dữ Liệu
* **Tư duy phản biện (Psychology):** Khả năng phân tích thông tin một cách khách quan để đưa ra những nhận định sáng suốt.
* **Kỹ năng giao tiếp (Forum):** Truyền đạt ý tưởng và kết quả phân tích một cách rõ ràng, dễ hiểu đến mọi đối tượng.
* **Kể chuyện với dữ liệu (Auto_graph):** Biến những con số khô khan thành những câu chuyện có ý nghĩa và thúc đẩy hành động.
* **Giải quyết vấn đề (Lightbulb):** Xác định chính xác các thách thức và tìm kiếm giải pháp tối ưu dựa trên nền tảng dữ liệu.

#### 3. Tư Duy Phát Triển Nghề Nghiệp (Career Growth Matrix)
* Mô hình phát triển cá nhân tập trung vào việc nâng cao năng lực qua 5 giai đoạn cốt lõi:
  1. **Follower (Người thực thi):** Giai đoạn thực tập sinh/junior làm quen với môi trường và tích lũy kỹ năng nền tảng dựa trên hướng dẫn chi tiết của các anh chị đi trước.
  2. **Learner (Người học chủ động):** Thấu hiểu phương án giải quyết bài toán, chủ động hỏi những câu hỏi có chiều sâu dưới sự định hướng của mentor để tích lũy kinh nghiệm thực chiến.
  3. **Problem Solver (Người giải quyết vấn đề):** Cột mốc quan trọng khi không còn làm việc theo checklist yêu cầu, chủ động phân tích sâu bài toán kinh doanh khó và cam kết chất lượng đầu ra.
  4. **System Thinker (Người tư duy hệ thống):** Nhìn nhận bài toán ở bức tranh toàn cảnh lớn, hiểu mối liên kết chéo giữa các bộ phận, đoán trước rủi ro vận hành và tập trung tối ưu hóa hệ thống lâu dài thay vì sửa lỗi vặt.
  5. **Super Star (Người dẫn dắt):** Đỉnh cao nghề nghiệp, đóng vai trò xây dựng tầm nhìn, định hướng chiến lược dữ liệu toàn diện và phát triển thế hệ kế cận.

#### 4. Lộ Trình 8 Bước Phát Triển Năng Lực (The Learning Path)
* Được sơ đồ hóa rõ ràng từ: (1) Student Curiosity -> (2) First Cloud AI Journey -> (3) Workshop & Community -> (4) Hands-on Labs -> (5) School Projects -> (6) Portfolio -> (7) AWS Partner -> (8) Share Back (Giúp đỡ thế hệ xây dựng tiếp theo).

#### 5. Thiết Kế Kiến Trúc Hệ Thống: Dịch Vụ Rút Gọn URL Trên AWS
* **Luồng xử lý đơn giản (Simple Flow) và hạn chế:** Người dùng gửi Long URL qua Frontend -> API Request -> Backend xử lý -> Ghi Short Code vào Database. Kiến trúc sơ khai này bộc lộ nhiều điểm yếu: Dễ tổn thương (Vulnerability), độ trễ đọc cao (Read Latency), tồn tại điểm lỗi duy nhất (Single Point of Failure) và rất khó mở rộng (Hard to scale).
* **Kiến trúc cải tiến với Key Generation Service (KGS):**
  * Tách biệt hoàn toàn cơ chế đọc và ghi độc lập (**Separation of Concerns**) để tối ưu cho từng loại traffic.
  * Sử dụng **Amazon ECS (Container)** để chạy dịch vụ KGS giúp tạo trước các short code ngẫu nhiên (**Pre-computation over On-demand**), đẩy vào hàng đợi mà không cần tính toán trực tiếp khi có request, triệt tiêu xung đột mã trùng.
  * Tích hợp bộ lưu trữ đệm **Amazon ElastiCache (Redis)** sử dụng hàm `LPUSH key_queue` để lưu trữ các mã tạo sẵn.
  * Áp dụng **Cache-aside Pattern**: Các yêu cầu đọc (Read requests) sẽ truy vấn trực tiếp từ bộ nhớ in-memory cache trước, chỉ khi bị cache miss mới tìm xuống Database, giúp giảm thiểu tối đa áp lực cho tầng dữ liệu và giữ độ trễ ở mức thấp nhất.
  * Đẩy bảo mật và bộ đệm ra sát người dùng nhất có thể (**Defense at the Edge**) để lọc các mối đe dọa trước khi chạm vào hệ thống cốt lõi.

---

### Những Gì Học Được

#### Tư Duy Thiết Kế
* **Domain-Driven Design:** Hiểu rằng công việc của một kỹ sư dữ liệu không bao giờ tách rời ngữ cảnh kinh doanh. Thiết kế kỹ thuật phải bám sát đặc thù vận hành của từng doanh nghiệp (FMCG như Colgate khác với dịch vụ chuỗi cung ứng như Kamereo).
* **Proactive Career Mapping:** Ý thức rõ vị trí hiện tại của bản thân (đang ở mức giao thoa giữa Follower và Learner) để chủ động đặt câu hỏi có chiều sâu, tự rèn luyện tư duy Problem Solver thay vì đợi giao việc.
* **Separation of Concerns (SoC):** Tư duy bóc tách luồng Đọc và luồng Ghi riêng biệt khi thiết kế hệ thống chịu tải lớn, giúp hệ thống không bị nghẽn cổ chai tại một điểm duy nhất.

#### Kiến Trúc Kỹ Thuật
* **Cơ chế Pre-computation:** Thay vì bắt hệ thống tính toán sinh chuỗi ngẫu nhiên "on-demand" dưới áp lực thời gian thực, việc tính toán trước (ahead-of-time) và lưu trữ vào Queue mang lại độ tin cậy tuyệt đối.
* **Ứng dụng In-Memory Caching:** Nắm vững cấu trúc dữ liệu Queue trong Redis (`LPUSH`) và mô hình Cache-aside để giải quyết triệt để bài toán Read Latency trong hệ thống phân tán.
* **Kiến trúc Edge Security:** Hiểu rõ tầm quan trọng của việc chặn đứng các truy vấn độc hại ngay tại vùng biên, bảo vệ tài nguyên tính toán core backend (ECS).

---

### Ứng Dụng Vào Công Việc
* **Áp dụng vào Đề tài Hệ thống Quản lý Thực tập sinh:** Áp dụng tư duy bóc tách xử lý (SoC) vào các module báo cáo dữ liệu của dự án nhóm, tránh viết các câu lệnh Query trực tiếp đè nặng lên DB chính.
* **Tối ưu hóa Code Comments & Workflow:** Triển khai các tiêu chuẩn dọn dẹp cấu trúc thư mục dạng modular giống như cách bố trí container trên Amazon ECS, tuân thủ viết comment không dấu chống lỗi hệ thống.
* **Xây dựng Portfolio cá nhân:** Bắt đầu hiện thực hóa bước số 6 trong lộ trình phát triển năng lực bằng cách đóng gói các dự án môn học tại HUTECH và mã nguồn trên GitLab thành một hồ sơ năng lực sạch sẽ, sẵn sàng kết nối với mạng lưới đối tác.

---

### Trải nghiệm trong event
Buổi Workshop mang lại cho tôi những bài học vô giá khi cân bằng hoàn hảo giữa định hướng tư duy sự nghiệp và kiến thức chuyên môn kỹ thuật sâu sắc. 
* **Góc nhìn thực tế từ doanh nghiệp:** Bài chia sẻ của các anh diễn giả giúp tôi dẹp bỏ cái nhìn mơ mộng về ngành Data/DevOps để thấy được các bài toán "sương máu" như tối ưu chi phí sản xuất tại Colgate hay xử lý lỗi vận hành tại Kamereo.
* **Kiến trúc trực quan, dễ hiểu:** Thay vì giải thích lý thuyết suông, các diễn giả đã tháo gỡ một hệ thống URL Shortener quen thuộc thành một mô hình chuẩn Enterprise sử dụng Amazon ECS và ElastiCache, chỉ rõ từng trade-off kỹ thuật.
* **Truyền cảm hứng mạnh mẽ:** Lộ trình phát triển 5 cấp độ tư duy thúc đẩy tôi phải thay đổi cách làm việc nhóm hiện tại, không chỉ dừng lại ở việc làm xong task được giao (Follower) mà phải hướng tới việc tối ưu luồng hệ thống tổng thể (System Thinker).

### Bài học rút ra
* Kỹ năng kể chuyện bằng dữ liệu (Data Storytelling) và tư duy phản biện mới là thứ phân tách một kỹ sư giỏi với một người chỉ biết viết code thông thường.
* Để hệ thống đạt được tính mở rộng (Scalability), hãy ưu tiên tính toán trước (Pre-computation) bất cứ khi nào có thể và tận dụng tối đa sức mạnh của bộ nhớ đệm (Caching).
* Hãy đi từng bước vững chắc theo lộ trình học tập, tích lũy từ những bài Lab nhỏ nhất trước khi kỳ vọng giải quyết được các bài toán lớn của thế giới thực.

### Một số hình ảnh sự kiện

![Nguyen Huu Tri](/aws/images/sk3,1.jpg)

![Nguyen Huu Tri](/aws/images/sk3,2.jpg)

![Nguyen Huu Tri](/aws/images/sk3,3.jpg)

![Nguyen Huu Tri](/aws/images/sk3,4.jpg)

![Nguyen Huu Tri](/aws/images/sk3,5.jpg)