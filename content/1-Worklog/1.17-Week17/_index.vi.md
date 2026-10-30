---
title: "Worklog Tuần 17"
date: 2026-10-26
weight: 17
chapter: false
pre: " <b> 1.17. </b> "
---

### Mục tiêu tuần 17:

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 26/10/2026 | 26/10/2026 |  |
| 3 |  | 27/10/2026 | 27/10/2026 |  |
| 4 | - Kiểm tra tài nguyên AWS trước khi thực hiện kết nối PHP web với RDS<br>&emsp;+ Kiểm tra ECS Task Definition: Tạo revision mới cho RakiBookery-task.<br>&emsp;+ Cập nhật ECS Service: Tạo revision mới hơn.<br>&emsp;+ Kiểm tra trạng thái ECS: Xác nhận task đã chạy.<br>&emsp;+ Kiểm tra Target Group: Xác nhận trạng thái Healthy.<br>&emsp;+ Kiểm tra website: Truy cập website thông qua DNS name của ALB.<br>- Học khóa học **Các khái niệm lập trình hàm trong Python** trong Codefinity<br>&emsp;+ Packing và Unpacking trong Python.<br>&emsp;+ Các hàm bậc cao và Lambda.<br>&emsp;+ Phạm vi Biến, Hàm Lồng và Closure. | 28/10/2026 | 28/10/2026 |  |
| 5 |  | 29/10/2026 | 29/10/2026 |  |
| 6 | - Triển khai quá trình kết nối PHP Web với RDS cho dự án RakiBookery<br>&emsp;+ Chỉnh sửa lỗi CSS trong trang web bằng đường link CloudFront.<br>&emsp;+ Sử dụng Docker và Amazon ECR để chuẩn bị công cụ import dữ liệu SQL.<br>&emsp;+ Tạo ECS Task để import dữ liệu vào database thông qua AWS Secrets Manager.<br>&emsp;+ Sử dụng CloudWatch Logs để kiểm tra dữ liệu sau khi import.<br>&emsp;+ Cập nhật Docker image, cấu hình PHP kết nối RDS và triển khai lên ECS Fargate.<br>&emsp;+ Kiểm tra website qua CloudFront và thử các chức năng tìm kiếm, lọc và sắp xếp sản phẩm. | 30/10/2026 | 30/10/2026 |  |

### Kết quả đạt được tuần 17:

&emsp;◉ Thứ 4:
<br>&emsp;&emsp;○ Website RakiBookery đã hiển thị qua ALB, ECS task hoạt động và Target Group đạt trạng thái Healthy.
<br>&emsp;&emsp;○ Đây là bước chuẩn bị để tiếp tục kiểm tra kết nối giữa ứng dụng PHP và cơ sở dữ liệu RDS.
<br>&emsp;&emsp;○ Hoàn thành 63% khóa học **Các khái niệm lập trình hàm trong Python**.

&emsp;◉ Thứ 6:
<br>&emsp;&emsp;○ Kết nối thành công PHP Web với Amazon RDS MySQL.
<br>&emsp;&emsp;○ Hiển thị được 20 sản phẩm từ database lên website.
<br>&emsp;&emsp;○ Các chức năng tìm kiếm, lọc theo thể loại, khoảng giá và sắp xếp sản phẩm hoạt động bình thường.