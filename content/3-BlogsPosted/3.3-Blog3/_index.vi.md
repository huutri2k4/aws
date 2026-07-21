---
title: "Blog 3"
date: 2026-07-09
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# TRIỂN KHAI MODERN DATA PLATFORM CHỈ TRONG VÀI PHÚT VỚI MODERN DATA ARCHITECTURE ACCELERATOR (MDAA)

Chào mọi người cộng đồng AWS Study Group VN.

Trong quá trình tìm hiểu về **AWS Big Data**, mình có đọc được một bài viết khá thú vị giới thiệu về **Modern Data Architecture Accelerator (MDAA)** – một framework mã nguồn mở do AWS phát triển nhằm giúp doanh nghiệp triển khai một Modern Data Platform nhanh hơn, đơn giản hơn nhưng vẫn tuân thủ các **AWS Best Practices** về bảo mật, quản trị dữ liệu và khả năng mở rộng.

Nếu mọi người đang tìm hiểu về **Data Lake, Data Platform hay AI Platform trên AWS** thì đây là một giải pháp rất đáng để tham khảo.

### Vì sao AWS phát triển MDAA?
Một Modern Data Platform ngày nay không còn đơn giản chỉ là tạo một S3 Bucket để lưu dữ liệu. Một hệ thống hoàn chỉnh thường phải kết hợp rất nhiều dịch vụ AWS như **Amazon S3** để lưu trữ dữ liệu, **AWS Glue** để xử lý ETL và quản lý metadata, **AWS Lake Formation** để quản trị quyền truy cập, **AWS IAM** để phân quyền, **AWS KMS** để mã hóa dữ liệu, **CloudTrail** để ghi lại toàn bộ hoạt động, **CloudWatch** để giám sát hệ thống cùng nhiều thành phần khác.

Điều này khiến việc xây dựng hạ tầng trở nên khá phức tạp. Ngoài việc hiểu từng dịch vụ, đội ngũ triển khai còn phải đảm bảo tất cả đều được cấu hình đúng chuẩn về **Security, Governance và Compliance**. Theo AWS, quá trình này thường mất rất nhiều thời gian và dễ xảy ra sai sót khi cấu hình thủ công.

### MDAA hoạt động như thế nào?
Điểm nổi bật nhất của MDAA là **thay đổi cách xây dựng hạ tầng**. Thay vì phải tự viết hàng nghìn dòng Infrastructure as Code để tạo từng tài nguyên AWS, người dùng **chỉ cần khai báo những gì mình mong muốn thông qua một file YAML**.

**Ví dụ:**
* Muốn xây dựng Data Lake.
* Muốn mã hóa dữ liệu.
* Muốn quản lý quyền truy cập.
* Muốn ghi Audit Log.
* Muốn triển khai Data Quality.

Sau đó, MDAA sẽ **tự động chuyển các khai báo này thành kiến trúc AWS hoàn chỉnh** bằng **AWS CDK và CloudFormation**. Theo số liệu AWS công bố, trong một ví dụ triển khai Data Lake có quản trị dữ liệu, lượng mã hạ tầng có thể **giảm từ khoảng 1.800 dòng CloudFormation xuống còn khoảng 45 dòng YAML**, giúp đơn giản hóa đáng kể quá trình triển khai.

### MDAA được xây dựng theo kiến trúc Module
Một điểm khá hay trong bài viết là MDAA không phải một sản phẩm cố định mà được xây dựng theo **kiến trúc module**. AWS hiện cung cấp **hơn 40 module khác nhau**, mỗi module đảm nhiệm một chức năng riêng như lưu trữ dữ liệu, ETL, quản trị dữ liệu, Machine Learning hay Generative AI.

Các module có thể **kết hợp với nhau giống như những khối LEGO**. Khi doanh nghiệp cần mở rộng hệ thống, chỉ cần bổ sung thêm module thay vì phải thiết kế lại toàn bộ kiến trúc. Để các module có thể giao tiếp với nhau, MDAA sử dụng **AWS Systems Manager Parameter Store** để chia sẻ thông tin cấu hình giữa các thành phần thay vì phải khai báo thủ công ARN hoặc ID của từng tài nguyên.

### Governance được tích hợp ngay từ khi triển khai
Ở nhiều dự án thực tế, Data Governance thường chỉ được bổ sung sau khi hệ thống đã hoàn thành. AWS lựa chọn cách tiếp cận hoàn toàn khác. 

Ngay trong quá trình triển khai, MDAA đã **tích hợp sẵn các dịch vụ phục vụ quản trị dữ liệu** như **AWS Lake Formation, AWS Glue Data Catalog, AWS KMS, CloudTrail** và nhiều cơ chế bảo mật khác. Điều này giúp doanh nghiệp xây dựng được một nền tảng dữ liệu có khả năng quản trị ngay từ đầu thay vì phải chỉnh sửa kiến trúc sau này.

### Bốn mô hình triển khai được AWS xây dựng sẵn
Để phù hợp với nhiều nhu cầu khác nhau, AWS đã chuẩn bị sẵn **bốn kiến trúc tham chiếu**:
* Mô hình đầu tiên là **Basic Data Lake**, phù hợp khi doanh nghiệp muốn tập trung dữ liệu từ nhiều nguồn về một nơi lưu trữ thống nhất.
* Khi có nhu cầu phân tích hoặc xây dựng các mô hình Machine Learning, doanh nghiệp có thể mở rộng lên **Data Science Platform**.
* Nếu nhiều nhóm như Data Engineer, Data Analyst và Data Scientist cần làm việc trên cùng một môi trường thì có thể triển khai **SageMaker Unified Studio**.
* Trong trường hợp muốn xây dựng các ứng dụng Generative AI trên dữ liệu nội bộ, MDAA tiếp tục hỗ trợ mở rộng với **Amazon Bedrock và kiến trúc Retrieval-Augmented Generation (RAG)** mà không cần thiết kế lại toàn bộ nền tảng dữ liệu.

**Ví dụ thực tế:**
Bài viết cũng đưa ra một trường hợp triển khai thực tế tại một **hệ thống đại học với 17 cơ sở, quản lý khoảng 7,2 TB dữ liệu và hơn 8.000 Dashboard**. Sau khi áp dụng MDAA, **thời gian triển khai các tính năng và Dashboard mới được rút ngắn khoảng 95%**, đồng thời giúp chuẩn hóa việc quản trị dữ liệu trên toàn hệ thống và giảm đáng kể sự phụ thuộc vào các giải pháp của bên thứ ba. Đây là ví dụ cho thấy MDAA hướng tới các tổ chức có quy mô dữ liệu lớn thay vì những ứng dụng nhỏ.

### MDAA có phù hợp với mọi dự án không?
Theo nội dung bài blog, MDAA được thiết kế dành cho các tổ chức đang xây dựng **Modern Data Platform, Data Lake hoặc các hệ thống phân tích dữ liệu quy mô lớn**. Điểm mạnh của framework này không nằm ở việc tạo ra nhiều dịch vụ AWS hơn mà ở **khả năng chuẩn hóa toàn bộ kiến trúc theo AWS Best Practices**, giảm đáng kể thời gian triển khai và giúp các nhóm kỹ thuật tập trung vào dữ liệu thay vì dành phần lớn thời gian để xây dựng hạ tầng.

### Kết luận
Theo mình, MDAA là một hướng tiếp cận khá thú vị của AWS trong việc xây dựng nền tảng dữ liệu hiện đại. Thay vì để kỹ sư phải cấu hình từng dịch vụ riêng lẻ, MDAA giúp **tự động hóa gần như toàn bộ quá trình triển khai**, đồng thời **tích hợp sẵn các cơ chế quản trị dữ liệu, bảo mật và khả năng mở rộng** ngay từ đầu.

Nếu mọi người đang tìm hiểu về Data Lake, Data Platform hoặc kiến trúc dữ liệu trên AWS thì đây là một bài viết rất đáng đọc để hiểu thêm cách AWS đang chuẩn hóa việc triển khai các hệ thống dữ liệu quy mô lớn.

**Nguồn tham khảo:** <https://aws.amazon.com/blogs/big-data/deploy-modern-data-platforms-in-minutes-with-mdaa/>