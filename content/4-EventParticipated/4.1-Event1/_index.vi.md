---
title: "FCAJ COMMUNITY DAY"
date: 2026-04-17
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---



### Mục Đích Của Sự Kiện
* Chia sẻ định hướng tổng quan và lộ trình của chuỗi sự kiện nhằm giới thiệu Điện toán đám mây và Trí tuệ nhân tạo (AI) cho cộng đồng.
* Phân tích các nguyên nhân cốt lõi khiến AI thất bại và cách tư duy đúng đắn để sử dụng AI hiệu quả hơn.
* Hướng dẫn cụ thể về cách cung cấp ngữ cảnh (Context) để tối ưu hóa kết quả đầu ra của các mô hình AI.
* Đúc kết kinh nghiệm thực tế về chiến lược định giá, các mô hình kinh doanh và thách thức tài chính khi triển khai CDN và bảo mật cho ứng dụng.
* Chia sẻ hành trình từ ý tưởng đến sản phẩm thực tế, tập trung vào kỹ năng làm việc nhóm, xử lý khủng hoảng và trình bày dự án trong thời gian ngắn (Sprint).

### Danh Sách Diễn Giả
* **Team VIB** 
* **Tinh Truong** - Platform Engineer, GoTymeX
* **Nguyen Tuan Thinh** - DevOps Engineer, First Cloud AI Journey (FCAJ)
* **Duc Dao** - Solutions Architect, Cloud Kinetics
* **Vy Lam** - Senior Business Systems Analyst, VPBank

---

### Nội Dung Nổi Bật

#### 1. Phương pháp sử dụng AI hiệu quả (Today's Journey)
* Sự kiện chỉ ra rằng các mô hình AI ngày nay rất mạnh mẽ, nhưng kết quả thường thất vọng do đầu vào (input) yếu kém.
* **Nguyên nhân chính AI thất bại:** Do ngữ cảnh cung cấp không đủ hoặc sai lệch (*Wrong direction*, *Too verbose*, *Misses constraints*). Mô hình AI không thể tự suy luận mục tiêu hoàn hảo hay đọc được suy nghĩ của người dùng; nó chỉ sử dụng những gì được cung cấp.
* **Ngữ cảnh (Context) đúng nghĩa:** Bao gồm mục tiêu người dùng (*Your goal*), tình huống cụ thể (*Your situation* như sinh viên, dự án deadline), các ràng buộc kỹ thuật/ngân sách (*Your constraints*), và bằng chứng liên quan (*Relevant evidence* như code, tài liệu).
* **Bài học cốt lõi:** Ngữ cảnh chuyển đổi một yêu cầu mơ hồ thành một nhiệm vụ có thể giải quyết được. Việc cung cấp ngữ cảnh tốt hơn luôn dẫn đến kết quả đầu ra chất lượng hơn (*Better context = better output*). Sai lầm phổ biến là nói cho AI những gì nó đã biết (*redundant context*); thay vào đó, hãy tập trung cung cấp những chi tiết hữu ích tiếp theo.

#### 2. Thách thức định giá và Quản lý chi phí Cloud (CDN & Security)
* Phân tích chi tiết mô hình định giá CDN và bảo mật: So sánh giữa **Pay-as-you-go** (trả theo mức sử dụng) và **Fixed-rate pricing** (giá cố định hàng tháng).
  * **Pay-as-you-go:** Tiết kiệm khi bắt đầu (bắt đầu từ $0) và có thể mở rộng linh hoạt theo mọi mức sử dụng. Tuy nhiên, thách thức lớn là khó ước tính chi phí trước, lưu lượng thay đổi bất ngờ (viral) có thể dẫn đến việc hóa đơn tăng đột biến.
  * **Fixed-rate pricing:** Cung cấp sự an tâm về chi phí ổn định hàng tháng, không lo sợ vượt quá ngân sách ngoài tầm kiểm soát.
* **Phản hồi từ khách hàng:** Rất nhiều doanh nghiệp lo ngại về rủi ro hóa đơn CDN tăng vọt đột ngột do tấn công mạng hoặc biến động traffic quá lớn (như nguy cơ hóa đơn nhảy vọt chạm mức $100K).
* **Giải pháp định giá cố định:** Kết hợp CDN + gói bảo mật tích hợp đầy đủ mọi tính năng cốt lõi (CDN CloudFront, WAF, Anti-DDoS, DNS Route 53 và Logging CloudWatch) giúp doanh nghiệp và các nhà phát triển kiểm soát rủi ro tài chính một cách tốt nhất.

#### 3. Hành trình Sáng tạo dự án dưới áp lực 36 giờ (LotusHacks)
* Chia sẻ hành trình từ con số 0 đến ý tưởng sản phẩm thực tế:
  * **Giờ 0:** Đăng ký tham gia, đầu óc còn hoàn toàn trống rỗng (*Signed up, head empty*).
  * **Ngày khai mạc:** Vẫn còn hoang mang và lạc lối (*Still lost*).
  * **Ra quyết định:** Về nhà và tập trung suy nghĩ (*Go home and think*).
  * **Nhận định:** Quan sát và khai thác từ chính những công việc hằng ngày (*Look at the daily work*).
  * **Xách định vấn đề cần giải quyết và đặt tên.**
  * **Sản phẩm UTMorpho chính thức ra đời.**
* **Quy trình 6 bước trong Sprint 36 giờ của nhóm:**
  1. **Setup & Alignment:** Thiết lập môi trường và đồng bộ hướng đi của nhóm.
  2. **First slice:** Cắt nhỏ và thực hiện mảng công việc đầu tiên.
  3. **Build the core:** Tập trung xây dựng các tính năng cốt lõi.
  4. **The hard middle:** Vượt qua giai đoạn giữa đầy khó khăn và thách thức.
  5. **Integration & Polish:** Tích hợp các module và hoàn thiện tối ưu giao diện.
  6. **Submit & Pitch:** Nộp bài và thuyết trình ý tưởng trước ban giám khảo.

---

### Những Gì Học Được

#### Tư Duy Thiết Kế
* **Tư duy về Ngữ cảnh (Context-Driven Mindset):** AI không phải là bộ não tự suy nghĩ ra mọi thứ. Giá trị của một người lập trình viên là biết cách thiết kế và cung cấp ngữ cảnh chuẩn xác để định hướng AI giải quyết công việc.
* **Tư duy định giá ứng dụng (FinOps Basics):** Hiểu rõ các mô hình định giá đám mây để đảm bảo tính ổn định tài chính cho dự án. Việc kiểm soát chi phí hạ tầng (nhất là với CDN và Security) cần được tính toán từ sớm để tránh tình trạng hóa đơn tăng ngoài tầm kiểm soát.

#### Kiến Trúc Kỹ Thuật
* **Kỹ thuật Prompting Thực chiến:** Tránh nói những điều hiển nhiên với AI khiến lãng phí không gian ngữ cảnh. Hãy học cách phân tích và cung cấp các ràng buộc, cấu trúc thư mục, hoặc log lỗi cụ thể để AI thực hiện refactor (như phân trang, validation) một cách chính xác nhất.

#### Chiến Lược Triển Khai
* **Lộ trình Sprint phối hợp nhóm:** Học hỏi được quy trình chia nhỏ task và phối hợp đội nhóm nhịp nhàng để hiện thực hóa một sản phẩm công nghệ từ ý tưởng sơ khai thành bản Demo hoàn chỉnh dưới áp lực thời gian cực hạn.

---

### Ứng Dụng Vào Công Việc
* **Áp dụng vào Đề tài Hệ thống Quản lý Thực tập sinh:** Ứng dụng mô hình cung cấp ngữ cảnh rõ ràng (Mục tiêu, tình huống, ràng buộc kỹ thuật) khi viết prompt tương tác với các chatbot hỗ trợ thiết kế module dự án nhóm, tuyệt đối không lặp lại context thừa.
* **Quản trị và phân chia công việc nhóm:** Sử dụng quy trình 6 bước của mô hình Sprint để quản lý tiến độ thiết kế UI/UX trên Figma và code Frontend cho dự án nhóm, đảm bảo mọi thành viên luôn đồng bộ với nhau.

---

### Trải nghiệm trong event
Buổi hội thảo mang lại cho tôi những bài học thực tế vô giá khi cân bằng hoàn hảo giữa tư duy thiết kế, kiến trúc kỹ thuật và chiến lược kinh doanh hạ tầng đám mây.
* **Góc nhìn thực chiến từ chuyên gia:** Các diễn giả đều là những người có kinh nghiệm dày dặn tại các tổ chức lớn (VIB, VPBank, GoTymeX, Cloud Kinetics), mang đến những case-study "xương máu" về cách tối ưu hóa AI hay xử lý bài toán chi phí Cloud, hoàn toàn không lý thuyết suông.
* **Cảm hứng làm việc nhóm mạnh mẽ:** Hành trình 36 giờ tại LotusHacks là một nguồn động lực lớn, giúp một sinh viên Kỹ thuật Phần mềm như tôi hiểu rõ hơn về sức mạnh của sự quyết đoán, kỹ năng làm việc nhóm và cách hoàn thiện sản phẩm nhanh chóng dưới áp lực lớn.

### Bài học rút ra
* Mô hình AI ngày nay rất mạnh, rào cản nằm ở cách chúng ta sử dụng và cung cấp dữ liệu đầu vào. Hãy đầu tư thời gian xây dựng một ngữ cảnh chuẩn chỉnh.
* Quản lý chi phí hạ tầng đám mây (Cloud cost optimization) là một kỹ năng bắt buộc phải có khi triển khai ứng dụng thực tế để bảo vệ hệ thống trước các rủi ro tài chính đột xuất.
* Khi chạy dự án ngắn hạn, không cần cố gắng làm những điều quá vĩ mô; hãy tập trung giải quyết dứt khoát một bài toán cụ thể, tối ưu lõi hệ thống và hoàn thiện nó một cách chỉn chu nhất.

### Một số hình ảnh sự kiện

![Nguyen Huu Tri](/aws/images/sk1.jpg)

![Nguyen Huu Tri](/aws/images/sk1,2.jpg)

![Nguyen Huu Tri](/aws/images/sk1,3.jpg)