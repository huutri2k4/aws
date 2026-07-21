---
title: "Blog1"
date: 2026-07-09
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Xây dựng hệ thống xác thực hai lớp (Dual-Token Authentication) cho Nakama Game Server bằng Amazon Cognito trên AWS.

### GIỚI THIỆU
Trong các trò chơi trực tuyến, hệ thống xác thực không chỉ cần đảm bảo tính bảo mật mà còn phải mang lại trải nghiệm đăng nhập liền mạch. Nakama sử dụng Session Token để quản lý phiên chơi, trong khi Amazon Cognito phát hành JWT (JSON Web Token) để xác thực danh tính người dùng. Nếu hai hệ thống này hoạt động độc lập, người chơi có thể phải xác thực nhiều lần hoặc gặp gián đoạn khi sử dụng.

Giải pháp Dual-Token Authentication kết hợp Amazon Cognito và Nakama để tách biệt việc quản lý danh tính với quản lý phiên chơi. Cognito chịu trách nhiệm xác thực người dùng, còn Nakama tạo và quản lý Session Token thông qua Go Runtime Hook, giúp hệ thống vừa an toàn vừa đảm bảo trải nghiệm mượt mà.

### Kiến trúc tổng thể
Kiến trúc sử dụng các dịch vụ chính gồm Amazon Cognito, Amazon CloudFront, Application Load Balancer (ALB), Network Load Balancer (NLB) và Nakama triển khai trên Amazon ECS Fargate.

Quy trình hoạt động như sau:
1. Người chơi đăng nhập bằng Amazon Cognito.
2. Cognito trả về JWT Access Token.
3. Client gửi JWT đến Nakama thông qua CloudFront.
4. Go Runtime Hook xác thực JWT và tạo Session Token.
5. Các yêu cầu tiếp theo sử dụng Session Token của Nakama.

Cách tiếp cận này giúp tách biệt hoàn toàn việc xác thực người dùng và quản lý phiên chơi.

### Luồng xác thực
Đầu tiên, người chơi đăng nhập bằng Amazon Cognito thông qua cơ chế USER_SRP_AUTH, giúp mật khẩu không phải gửi trực tiếp lên máy chủ. Sau khi xác thực thành công, Cognito phát hành JWT chứa các thông tin như sub, iss, exp và client_id.

Khi JWT được gửi đến Nakama, Go Runtime Hook sẽ kiểm tra chữ ký số, thời gian hết hạn, Issuer và Client ID. Nếu token hợp lệ, Nakama sẽ tạo Session Token để người chơi sử dụng trong toàn bộ quá trình chơi game.

### Vai trò của ALB và NLB
Hệ thống sử dụng đồng thời hai Load Balancer để xử lý các loại lưu lượng khác nhau.
* **Application Load Balancer (ALB):** Xử lý các HTTP API, chỉ cho phép những đường dẫn đã được cấu hình và từ chối các yêu cầu không hợp lệ bằng mã lỗi 403 Forbidden.
* **Network Load Balancer (NLB):** Xử lý kết nối WebSocket ở tầng TCP, giúp duy trì kết nối ổn định và giảm độ trễ cho các trò chơi thời gian thực.

### Bảo mật hệ thống
Amazon CloudFront là điểm truy cập HTTPS duy nhất và kết hợp với AWS WAF để lọc các yêu cầu độc hại trước khi chuyển đến hệ thống.

Bên cạnh đó, Go Runtime Hook chỉ chấp nhận JWT hợp lệ và luôn sử dụng giá trị sub trong token đã xác thực để nhận diện người chơi, giúp ngăn chặn việc giả mạo tài khoản. Các Security Group cũng được cấu hình để chỉ cho phép lưu lượng đi theo đúng tuyến từ CloudFront đến Nakama.

### Kết luận
Giải pháp Dual-Token Authentication kết hợp giữa Amazon Cognito và Nakama giúp xây dựng một hệ thống xác thực an toàn, linh hoạt và phù hợp cho các game trực tuyến hiện đại. Với sự hỗ trợ của CloudFront, ALB, NLB và Amazon ECS Fargate, hệ thống không chỉ tăng cường bảo mật mà còn đảm bảo khả năng mở rộng, hiệu suất cao và hỗ trợ tốt cho các kết nối WebSocket thời gian thực.

![Nguyen Huu Tri](images/tri.jpg)

**Nguồn tham khảo:** <https://aws.amazon.com/blogs/architecture/dual-token-authentication-for-nakama-game-servers-with-amazon-cognito-on-aws/>