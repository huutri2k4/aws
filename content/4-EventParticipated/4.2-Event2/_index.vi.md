---
title: "Sự kiện AWS Community Day"
date: 2026-05-23
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Báo cáo Sự kiện: AWS First Cloud AI Journey Community Day

### Mục Đích Của Sự Kiện
* Chia sẻ các góc nhìn thực tế về cách tối ưu hóa ngữ cảnh (Context) để ứng dụng AI hiệu quả trong công việc và học tập.
* Đúc kết kinh nghiệm thực tiễn từ hành trình tham gia Hackathon và quy trình phát triển sản phẩm công nghệ từ ý tưởng đến thực tế dưới áp lực thời gian.
* Giới thiệu kiến trúc nền tảng và các giải pháp tối ưu chi phí, hiệu năng, bảo mật bằng dịch vụ phân phối nội dung toàn cầu Amazon CloudFront.
* Hướng dẫn ứng dụng các công cụ trợ lý thông minh và phân tích dữ liệu tự động bằng ngôn ngữ tự nhiên.
* Làm rõ các cơ chế kỹ thuật ngầm chuyên sâu về tính bất định (Non-Determinism) của LLM và kiến trúc hệ thống Multi-Agent cấp doanh nghiệp.

### Danh Sách Diễn Giả
* **Vy Lam** - Senior Business Systems Analyst, VPBank
* **Thao Nguyen** - GenAI Engineer, VIB
* **Mai Nguyen** - GenAI Engineer, VIB
* **Uyen Le** - GenAI Engineer, VIB
* **Anh Pham** - Cloud Consultant, G-AsiaPacific Vietnam
* **Thinh Nguyen** - Devops Engineer, FCAJ
* **Tinh Truong** - Platform Engineer, GoTymeX
* **Duc Dao** - Solutions Architect, Cloud Kinetics

---

### Nội Dung Nổi Bật

#### 1. Vai trò của Ngữ cảnh trong Ứng dụng AI (Context Is Everything)
* Giải mã lý do các mô hình AI thường thất bại khi thiếu hụt dữ liệu nền tảng và định nghĩa bản chất thực sự của "ngữ cảnh".
* Sự tiến hóa công nghệ từ các dòng prompt đơn lẻ dịch chuyển sang cơ chế quản lý bộ nhớ dài hạn (Khái niệm bộ não AI thứ hai - Second AI Brain).
* Định hướng tư duy và các mẹo thực tế để tận dụng ngữ cảnh tốt hơn, giúp sinh viên và lập trình viên khai thác AI tối đa trong định hướng sự nghiệp.

#### 2. Hành trình 36 giờ tại LotusHacks – Triển khai dự án UTMorpho
* Chia sẻ lý do tham gia và hành trình động não (brainstorming) từ con số 0 để định hình bài toán thực tế cho sản phẩm UTMorpho.
* Trải nghiệm lập trình dưới áp lực thời gian cực hạn (36-Hour Development Sprint), vượt qua các điểm nghẽn kỹ thuật và thất bại phát sinh để hoàn thiện bản Demo sản phẩm.

#### 3. Xây dựng hạ tầng phân phối vững chắc với Amazon CloudFront
* Ứng dụng Amazon CloudFront làm nền tảng tăng tốc chịu tải cho mọi loại cấu trúc Workload từ Edge đến Origin.
* Các chiến lược tối ưu hóa chi phí băng thông, tăng cường khả năng bảo mật hạ tầng, nâng cao tính sẵn sàng (Reliability) và hiệu năng (Performance) hệ thống.

#### 4. Trợ lý AI thông minh tích hợp (Amazon Quick)
* **Quick Chat Agent & Quick Sight:** Xây dựng các bot trợ lý khám phá dữ liệu, phân tích chuyên sâu và tự động tạo dashboard báo cáo từ dữ liệu thô hoàn toàn bằng ngôn ngữ tự nhiên.
* **Quick Flows & Quick Spaces:** Thiết lập các quy trình công việc thông minh không cần code (No-code) và kiến tạo không gian cộng tác nhóm để chuyển hóa tri thức cá nhân thành tài sản chung của tập thể.

#### 5. Tính bất định của các thiết lập LLM "Định tính"
* Phân tích sâu cơ chế hoạt động ngầm của LLM khi chọn token tiếp theo trong chuỗi văn bản.
* Đập tan lầm tưởng kỹ thuật: Bác bỏ giả định cho rằng cấu hình `Temperature=0` sẽ đảm bảo 100% kết quả trả ra giống nhau (Determinism), chỉ ra nguyên nhân do các thuật toán tối ưu hóa hạ tầng tính toán (Inference optimizations).
* Đánh giá các tác động thực tế đến hệ thống và đưa ra các chiến lược giảm thiểu (Mitigation strategies) sai số.

#### 6. Hệ thống Multi-Agent cấp doanh nghiệp trong chấm điểm tín dụng Startup
* Giải quyết sự bất đối xứng cấu trúc giữa dữ liệu hệ thống ngân hàng truyền thống và đặc thù dữ liệu của các công nghiệp Startup.
* Phân tích bài toán khi nào nên dùng Single Agent và khi nào bắt buộc phải dịch chuyển sang mô hình Multi-Agent.
* Thiết lập sơ đồ kiến trúc cho một "Hội đồng tín dụng ảo" (Virtual Credit Committee), xây dựng các rào chắn tuân thủ (Guardrails & Compliance) cùng lộ trình tính toán ROI khi vận hành thực tế.

---

### Những Gì Học Được

#### Tư Duy Thiết Kế
* **Context-Driven Mindset:** Hiểu rõ AI chỉ là công cụ, việc cung cấp và thiết lập một "Hệ thống ngữ cảnh" (Second AI Brain) chuẩn xác mới là chìa khóa để tạo ra kết quả tối ưu.
* **Problem-First Approach:** Bài học từ Hackathon cho thấy việc định hình rõ ràng bài toán thực tế quan trọng hơn việc vội vã đâm đầu vào viết code mà không có mục tiêu cụ thể.
* **Multi-Agent Paradigm:** Tư duy phân rã các hệ thống phức tạp thành một mạng lưới nhiều Agent chuyên biệt phối hợp với nhau, thay vì bắt một Agent duy nhất xử lý mọi tác vụ lớn.

#### Kiến Trúc Kỹ Thuật
* **Hạ tầng phân phối tại vùng biên:** Cách sử dụng CloudFront làm lớp khiên chắn đầu tiên để vừa tối ưu chi phí hạ tầng, vừa tăng tốc độ phản hồi cho các ứng dụng web.
* **Bản chất Stochastic của LLM:** Hiểu sâu về cách phân tích token của mô hình ngôn ngữ lớn để chuẩn bị cho việc xử lý các hệ thống đòi hỏi tính chính xác cao, nhận diện được sự đánh đổi (trade-offs) của các hạ tầng Inference.
* **Thiết lập Guardrails:** Cách thức tích hợp các rào cản kiểm soát dữ liệu đầu vào/đầu ra để đảm bảo hệ thống AI tuân thủ các quy định bảo mật của doanh nghiệp.

#### Chiến Lược Triển Khai
* **No-code Workflow Integration:** Tận dụng tối đa các công cụ như Amazon Quick để tự động hóa quy trình phân tích nội bộ, rút ngắn thời gian xây dựng Dashboard từ hàng tuần xuống hàng phút.
* **Hành trình Sprint hiệu quả:** Kinh nghiệm quản lý năng suất, phân chia task và xử lý khủng hoảng khi chạy dự án trong thời gian ngắn dưới áp lực cao.

---

### Ứng Dụng Vào Công Việc
* **Tối ưu hóa quy trình làm việc với AI:** Ứng dụng tư duy kiến tạo Context để xây dựng các prompt và hệ thống lưu trữ tài liệu tham khảo thông minh cho bản thân khi làm bài tập lớn.
* **Triển khai hạ tầng cho dự án nhóm:** Áp dụng Amazon CloudFront vào ứng dụng Web của nhóm để tăng tốc tải trang và bảo vệ các API Backend.
* **Thử nghiệm No-code AI Tools:** Tích hợp các giải pháp dạng Quick Flows hoặc Chat Agent để thử nghiệm nhanh các ý tưởng tính năng trước khi bước vào giai đoạn code chi tiết.
* **Xây dựng hệ thống bài bản:** Khi thiết kế các module AI cho dự án, chú ý cấu hình các thông số LLM và tính toán đến sai số bất định dựa trên các chiến lược giảm thiểu đã học.

---

### Trải nghiệm trong event
Tham gia buổi **AWS First Cloud AI Journey Community Day** tại Bitexco Financial Tower là một trải nghiệm cực kỳ giá trị, mở ra cho tôi một cái nhìn toàn diện từ những kiến thức hạ tầng cốt lõi cho đến các kỹ thuật GenAI chuyên sâu nhất tại doanh nghiệp. Một số trải nghiệm nổi bật:
* **Học hỏi từ đội ngũ diễn giả chất lượng:** Được lắng nghe chia sẻ trực tiếp từ các kỹ sư GenAI, Giải pháp kiến trúc (SA), Consultant đến từ các ngân hàng lớn (VIB, VPBank) và các đối tác cao cấp của AWS. Các case-study từ chấm điểm tín dụng đến phát triển ứng dụng UTMorpho giúp tôi hiểu rõ khoảng cách giữa lý thuyết giảng đường và bài toán thực tế.
* **Tiếp cận sâu về mặt kỹ thuật:** Buổi hội thảo không dừng lại ở mức giới thiệu tính năng mà đi sâu vào bản chất toán học/hạ tầng (cách chọn token của LLM, lỗi phần cứng ngầm khi tối ưu inference). Điều này giúp ích rất lớn cho một sinh viên chuyên ngành Kỹ thuật Phần mềm như tôi để tư duy hệ thống chuẩn xác hơn.
* **Môi trường kết nối chuyên nghiệp:** Không gian tổ chức hoành tráng, tạo điều kiện thuận lợi để giao lưu, đặt câu hỏi Q&A trực tiếp với các chuyên gia và học hỏi kinh nghiệm thực chiến từ các anh chị Devops Engineer, SA đi trước.

### Bài học rút ra
* Một hệ thống AI mạnh không nằm ở việc chọn mô hình đắt tiền nhất, mà nằm ở việc thiết kế hệ thống dữ liệu ngữ cảnh (Context Layer) và kiến trúc Multi-Agent phân rã nhiệm vụ đủ tốt.
* Luôn phải tính toán đến tính bất định của LLM trong môi trường Production để có các kịch bản kiểm soát (Guardrails) phù hợp.
* Việc tối ưu hóa hạ tầng đám mây (như CloudFront) cần được thực hiện song song ngay từ giai đoạn đầu phát triển ứng dụng để bảo toàn chi phí ngân sách và trải nghiệm người dùng.

### Một số hình ảnh sự kiện

![Nguyen Huu Tri](/images/sk2,1.jpg)

![Nguyen Huu Tri](/images/sk2,2.jpg)

![Nguyen Huu Tri](/images/sk2,3.jpg)

![Nguyen Huu Tri](/images/sk2,4.jpg)