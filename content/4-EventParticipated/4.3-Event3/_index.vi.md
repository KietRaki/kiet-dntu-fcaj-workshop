---
title: "Event 3"
date: 2026-10-31
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch “FCAJ - Community Day 31/10”

{{< img src="images/4-EventParticipated/event3/GroupPhoto_Event3.jpg" alt="Group Photo of Event 3" >}}

## Mục đích của sự kiện

Sự kiện FCAJ - Community Day 31/10 được tổ chức nhằm tạo cơ hội cho sinh viên, lập trình viên và những người quan tâm đến công nghệ điện toán đám mây AWS gặp gỡ, học hỏi và trao đổi kinh nghiệm thực tế từ các chuyên gia trong ngành.

Thông qua các bài chia sẻ, sự kiện hướng đến việc cung cấp kiến thức về lộ trình học AWS, ứng dụng trí tuệ nhân tạo (AI) trong phát triển phần mềm, xây dựng kiến trúc Serverless, xử lý hệ thống bất đồng bộ và đóng góp mã nguồn mở. Đồng thời, chương trình giúp người tham dự tiếp cận những công nghệ mới, hiểu rõ hơn về yêu cầu thực tế của ngành và định hướng phát triển nghề nghiệp trong lĩnh vực Cloud Computing.

## Danh sách diễn giả

1\. Trần Minh Tuấn: Backend Developer, sinh viên Đại học FPT. Chia sẻ về chủ đề "Hướng dẫn cách học và lộ trình tiếp cận AWS cho người mới bắt đầu".

2\. Henry Đức Bùi: Head of Engineering tại Cloud Tinker. Trình bày chủ đề "Learnings from Building Software Factory", tập trung vào kinh nghiệm ứng dụng AI Agent trong quy trình phát triển phần mềm.

3\. Phúc Khang (Khang Duong): Thành viên First Cloud Journey. Chia sẻ về chủ đề "3 tháng thực tập tại First Cloud Journey", giới thiệu kinh nghiệm xây dựng sản phẩm thực tế bằng kiến trúc Serverless trên AWS.

4\. Thịnh Nguyễn: DevOps / Cloud Engineer tại Style Solution. Trình bày chủ đề "AWS Lambda Web Function: Rethinking Serverless Web Architecture", giới thiệu những cải tiến của Lambda Web Function trong việc xây dựng ứng dụng web.

5\. Lương Cẩm Đào: Thành viên First Cloud Journey. Chia sẻ chủ đề "Xây dựng hệ thống bất đồng bộ trên Amazon SQS", tập trung vào cách thiết kế và triển khai hệ thống xử lý hàng đợi tin nhắn.

6\. Hưng Trần: Senior Cloud Engineer tại NAP, Top 25 AWS CDK Contributor. Trình bày chủ đề "Start and Maintain Consistency with Open-Source Code Contribution", chia sẻ kinh nghiệm và phương pháp đóng góp cho các dự án mã nguồn mở.

## Nội dung nổi bật

### Hướng dẫn cách học và lộ trình tiếp cận AWS cho người mới bắt đầu

Diễn giả Trần Minh Tuấn giới thiệu ba nền tảng hỗ trợ học tập gồm AWS Study Group, AWS Skill Builder và AWS Builder Center. Trong đó, AWS Skill Builder cung cấp kiến thức lý thuyết và các lộ trình học tập, AWS Study Group hỗ trợ thực hành thông qua các bài lab, còn AWS Builder Center giúp kết nối cộng đồng và chia sẻ kiến thức. Diễn giả cũng đề xuất lộ trình học từ lý thuyết, thực hành, ghi chép kiến thức đến tự xây dựng dự án nhỏ. Ngoài ra, người học cần chú ý quản lý tài nguyên AWS và thực hiện Clean up sau mỗi bài lab để tránh phát sinh chi phí không cần thiết.

### Ứng dụng AI Agent trong quy trình phát triển phần mềm

Henry Đức Bùi chia sẻ kinh nghiệm xây dựng Software Factory bằng cách ứng dụng AI Agent vào toàn bộ quy trình phát triển phần mềm - SDLC. Đội ngũ chỉ gồm 5-6 người đã xử lý và merge gần 3.000 Merge Requests trong một tháng, tăng gấp ba lần so với tháng trước. Một số phương pháp đáng chú ý gồm đưa AI tham gia vào quá trình thảo luận tính năng, sử dụng kỹ thuật Divergent Prompting để tìm kiếm nhiều giải pháp, tự động hóa Code Review và Testing. Bài chia sẻ cho thấy AI có thể hỗ trợ đáng kể trong việc tăng năng suất lập trình và tự động hóa các công việc kỹ thuật.

### Xây dựng ứng dụng thực tế bằng kiến trúc Serverless trên AWS

Phúc Khang giới thiệu dự án game thẻ bài nhiều người chơi theo thời gian thực được xây dựng trong thời gian thực tập tại First Cloud Journey. Hệ thống sử dụng AWS Lambda để xử lý logic backend, DynamoDB để lưu trữ dữ liệu, SQS và EventBridge để quản lý các sự kiện, cùng Cognito và API Gateway/WebSocket để xác thực người dùng và duy trì kết nối. Diễn giả cũng chia sẻ những sai lầm thực tế như phát sinh lượng lớn request không cần thiết khi sử dụng SQS để đếm ngược thời gian, cấu hình IAM Role chưa tuân thủ nguyên tắc Least Privilege và thiếu quản lý phiên bản Lambda. Từ đó, diễn giả nhấn mạnh tầm quan trọng của bảo mật và Infrastructure as Code (IaC) thông qua AWS CDK và CloudFormation.

### Giới thiệu AWS Lambda Web Function và kiến trúc Serverless mới

Thịnh Nguyễn phân tích những hạn chế của AWS Lambda truyền thống như Cold Start, phụ thuộc vào API Gateway và chi phí tính theo thời gian thực thi. Sau đó, diễn giả giới thiệu Lambda Web Function với khả năng đóng gói ứng dụng bằng Docker Container, hỗ trợ xử lý đồng thời tối đa 128 requests trên một instance và kết nối trực tiếp với CloudFront thông qua Origin Access Control - OAC. Theo nội dung trình bày, cơ chế tính phí dựa trên thời gian xử lý CPU thực tế có thể giúp tiết kiệm khoảng 40-70% chi phí. Diễn giả cũng thực hiện demo ứng dụng trắc nghiệm MBTI để minh họa khả năng triển khai kiến trúc này.

### Xây dựng hệ thống xử lý bất đồng bộ bằng Amazon SQS

Lương Cẩm Đào trình bày sự khác biệt giữa xử lý đồng bộ và bất đồng bộ. Thay vì để người dùng chờ một dịch vụ AI xử lý xong yêu cầu, hệ thống có thể sử dụng Amazon SQS làm hàng đợi trung gian để lưu trữ công việc và trả về trạng thái Pending ngay lập tức. Diễn giả giới thiệu hai loại hàng đợi Standard Queue và FIFO Queue, cùng các cơ chế quan trọng như Visibility Timeout, Heartbeat, Long Polling và Dead Letter Queue - DLQ. Ngoài ra, phần demo còn giới thiệu cách kết hợp Amazon SNS và SQS theo mô hình Fan-out để phân phối một thông điệp đến nhiều hàng đợi khác nhau.

### Kinh nghiệm đóng góp và duy trì hoạt động trong cộng đồng Open Source

Hưng Trần chia sẻ kinh nghiệm tham gia đóng góp mã nguồn mở, đặc biệt là các dự án liên quan đến AWS CDK, Terraform và Pulumi. Diễn giả khuyến khích người mới bắt đầu từ những issue có nhãn Good First Issue hoặc Ready to Implement, chia nhỏ Pull Request và kiên trì theo đuổi quá trình đóng góp. Một phương pháp được đề xuất là dành khoảng 15-30 phút mỗi ngày để tham gia đóng góp. Bên cạnh đó, diễn giả nhấn mạnh tư duy chủ động tìm kiếm và sửa lỗi trong mã nguồn thay vì chờ nhà cung cấp dịch vụ cập nhật hoặc hỗ trợ tính năng mới.