---
title: "Worklog Tuần 9"
date: 2026-08-31
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Triển khai website với GitHub Pages.
* Xây dựng các data pipeline trên AWS.
* Tập trung vào xử lý dữ liệu thời gian thực với Kinesis, Lambda và DynamoDB.
* Xây dựng Data Lake với S3 và Glue.

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 31/08/2026 | 31/08/2026 |  |
| 3 |  | 01/09/2026 | 01/09/2026 |  |
| 4 | - Thiết lập GitHub Pages để triển khai website workshop<br>&emsp;+ Tạo repository.<br>&emsp;+ Cấu hình GitHub Actions.<br>&emsp;+ Xử lý lỗi **function "try" not defined** do khác phiên bản Hugo.<br>&emsp;+ Cấu hình GitHub Pages sử dụng GitHub Actions.<br>&emsp;+ Kiểm tra và xử lý lỗi hình ảnh. | 02/09/2026 | 02/09/2026 |  |
| 5 | - Thực hành lab **Real-Time Transaction Processing Pipeline**<br>&emsp;+ Amazon S3: lưu dữ liệu đầu vào.<br>&emsp;+ Amazon EC2: producer gửi dữ liệu.<br>&emsp;+ Amazon Kinesis Data Streams: stream dữ liệu thời gian thực.<br>&emsp;+ AWS Lambda: xử lý dữ liệu.<br>&emsp;+ Amazon DynamoDB: lưu table Transactions và Customer Summary.<br>&emsp;+ IAM Roles và CloudWatch: phân quyền, giám sát và cảnh báo. | 03/09/2026 | 03/09/2026 | Lab được làm từ ChatGPT |
| 6 | - Thực hành lab **Xây dựng Data Lake với dữ liệu của riêng bạn**<br>&emsp;+ VS Code + AWS CLI thay cho Cloud9 → upload dữ liệu lên S3.<br>&emsp;+ S3 → lưu raw / cleaned / parquet.<br>&emsp;+ Glue DataBrew → profile, làm sạch và chuyển đổi dữ liệu.<br>&emsp;+ Glue ETL → CSV → Parquet - không thể sử dụng dịch vụ này. | 04/09/2026 | 04/09/2026 | [Lab 000070](https://000070.awsstudygroup.com/vi/)<br>[Cách host một trang web trên GitHub Pages miễn phí](https://youtu.be/e5AwNU3Y2es) |

### Kết quả đạt được tuần 9:

&emsp;◉ Thứ 4:
<br>&emsp;&emsp;○ Hoàn thiện quy trình build và deploy website workshop lên GitHub Pages.
<br>&emsp;&emsp;○ Xác định và xử lý các vấn đề liên quan đến phiên bản Hugo, GitHub Pages và đường dẫn hình ảnh.

&emsp;◉ Thứ 5:
<br>&emsp;&emsp;○ Xây dựng thành công pipeline xử lý giao dịch theo thời gian thực từ S3 → EC2 → Kinesis → Lambda → DynamoDB.

&emsp;◉ Thứ 6:
<br>&emsp;&emsp;○ Đã upload dữ liệu lên S3, thực hành Glue DataBrew để profile, clean và transform, tạo được cleaned CSV.
<br>&emsp;&emsp;○ Không thể thực hiện Glue ETL Job (CSV → Parquet) do thiếu quyền truy cập.