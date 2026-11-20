---
title: "Worklog Tuần 19"
date: 2026-11-09
weight: 19
chapter: false
pre: " <b> 1.19. </b> "
---

### Mục tiêu tuần 19:

* Hoàn thiện và triển khai các chức năng thanh toán PayPal cho dự án RakiBookery.
* Thực hành xây dựng hệ thống xử lý và phân tích dữ liệu thời gian thực bằng Kinesis, Lambda, Firehose, S3 và Athena.
* Làm quen với Amazon QuickSight, xây dựng Dashboard và phân tích dữ liệu kinh doanh.

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 | - Thực hiện sửa lỗi hiển thị hai phương thức thanh toán PayPal giống nhau của dự án RakiBookery<br>&emsp;+ Kiểm tra mã nguồn và tìm nguyên nhân lỗi hiển thị hai phương thức PayPal trùng nhau.<br>&emsp;+ Sửa lỗi cú pháp SQL trong file `Order.php` và cập nhật xử lý lưu đơn hàng trong `PayPalController.php`.<br>&emsp;+ Điều chỉnh `checkout.php` để chỉ hiển thị một phương thức PayPal.<br>&emsp;+ Sử dụng Docker để build image và push lên Amazon ECR.<br>&emsp;+ Tạo ECS Task Definition revision mới và cập nhật ECS Service để triển khai phiên bản đã sửa. | 09/11/2026 | 09/11/2026 |  |
| 3 |  | 10/11/2026 | 10/11/2026 |  |
| 4 | - Thực hành lab **Real-Time Data Streaming và Analytics Pipeline trên AWS**<br>&emsp;+ Tạo Amazon Kinesis Data Streams để tiếp nhận dữ liệu đơn hàng theo thời gian thực.<br>&emsp;+ Tạo AWS Lambda để xử lý dữ liệu JSON.<br>&emsp;+ Cấu hình Amazon Data Firehose để nhận dữ liệu từ Kinesis, xử lý thông qua Lambda và lưu vào Amazon S3.<br>&emsp;+ Sử dụng Python và Boto3 xây dựng chương trình giả lập gửi đơn hàng vào Kinesis.<br>&emsp;+ Cấu hình AWS Glue Crawler và Data Catalog để nhận diện cấu trúc dữ liệu.<br>&emsp;+ Sử dụng Amazon Athena thực hiện các truy vấn SQL để phân tích doanh thu và sản phẩm bán chạy.<br>&emsp;+ Theo dõi các log xử lý dữ liệu trên Amazon CloudWatch. | 11/11/2026 | 11/11/2026 | [Amazon Kinesis](https://docs.aws.amazon.com/streams/latest/dev/)<br>[Amazon Data Firehose](https://docs.aws.amazon.com/firehose/latest/dev/)<br>[Transform source data in Amazon Data Firehose](https://docs.aws.amazon.com/firehose/latest/dev/data-transformation.html)<br>[AWS Lambda](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)<br>[Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)<br>[AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html)<br>[Amazon Athena](https://docs.aws.amazon.com/athena/latest/ug/what-is.html)<br>[Amazon CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html) |
| 5 | - Thực hành lab **Business Intelligence with Amazon QuickSight**<br>&emsp;+ Đăng ký và cấu hình tài khoản AWS Quick tại Region Singapore.<br>&emsp;+ Tải dữ liệu `sales.csv` lên QuickSight và tạo Dataset bằng SPICE.<br>&emsp;+ Tạo 5 biểu đồ phân tích doanh thu, lợi nhuận, quốc gia, thời gian và số lượng sản phẩm theo nhóm khách hàng.<br>&emsp;+ Tổng hợp và xuất bản Dashboard với tên `Sales Performance Dashboard`.<br>&emsp;+ Kiểm tra các chức năng xem dữ liệu chi tiết, phân tích bằng AI, xuất CSV và nhúng biểu đồ vào website.<br>&emsp;+ Xóa các tài nguyên sau khi hoàn thành lab. | 12/11/2026 | 12/11/2026 | [Lab 000073](https://000073.awsfcaj.com/vi/) |
| 6 |  | 13/11/2026 | 13/11/2026 |  |

### Kết quả đạt được tuần 19:

&emsp;◉ Thứ 2:
<br>&emsp;&emsp;○ Chưa triển khai thành công do ECS gặp lỗi kết nối AWS Secrets Manager. Cần tiếp tục kiểm tra cấu hình mạng và khắc phục lỗi.

&emsp;◉ Thứ 4:
<br>&emsp;&emsp;○ Xây dựng thành công hệ thống xử lý dữ liệu đơn hàng theo thời gian thực bằng Kinesis, Lambda và Firehose.
<br>&emsp;&emsp;○ Gửi và xử lý thành công 30 đơn hàng, lưu dữ liệu JSON vào S3.
<br>&emsp;&emsp;○ Khắc phục lỗi định dạng dữ liệu và truy vấn thành công trên Amazon Athena.
<br>&emsp;&emsp;○ Hiểu rõ hơn quy trình thu thập, xử lý, lưu trữ và phân tích dữ liệu streaming trên AWS.

&emsp;◉ Thứ 5:
<br>&emsp;&emsp;○ Tạo và xuất bản thành công Dashboard gồm 5 biểu đồ phân tích kinh doanh.
<br>&emsp;&emsp;○ Thực hiện được các chức năng lọc, xem dữ liệu, xuất báo cáo và phân tích bằng AI.
<br>&emsp;&emsp;○ Biết cách xóa các tài nguyên đúng cách của Amazon QuickSight sau lab.