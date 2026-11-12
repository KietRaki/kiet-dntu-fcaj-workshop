---
title: "Worklog Tuần 18"
date: 2026-11-02
weight: 18
chapter: false
pre: " <b> 1.18. </b> "
---

### Mục tiêu tuần 18:

* Kiểm tra và sửa chức năng thanh toán PayPal cho dự án RakiBookery.
* Thực hành quản lý dữ liệu NoSQL với Amazon DynamoDB, AWS CLI và Boto3.
* Xây dựng ETL Pipeline serverless bằng AWS Glue để xử lý, chuyển đổi và truy vấn dữ liệu.

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 02/11/2026 | 02/11/2026 |  |
| 3 | - Thực hiện sửa lỗi và kiểm tra chức năng thanh toán PayPal cho dự án RakiBookery<br>&emsp;+ Kiểm tra cấu hình PayPal Sandbox trên AWS ECS và phát hiện lỗi biến môi trường.<br>&emsp;+ Kiểm tra IAM Role, bổ sung quyền truy cập Parameter Store và Secrets Manager.<br>&emsp;+ Tạo Task Definition revision mới và cập nhật thông tin cấu hình PayPal Sandbox.<br>&emsp;+ Kiểm tra giao diện thanh toán PayPal và Debit or Credit Card.<br>&emsp;+ Thử nghiệm thanh toán bằng PayPal Balance và thẻ Visa. | 03/11/2026 | 03/11/2026 |  |
| 4 | - Thực hành lab **Những điều cần thiết về CSDL NoSQL với Amazon DynamoDB**<br>&emsp;+ Tìm hiểu cách tạo và quản lý bảng DynamoDB bằng AWS Management Console và AWS CloudShell.<br>&emsp;+ Thực hành thêm, đọc, cập nhật, xóa và truy vấn dữ liệu bằng AWS CLI.<br>&emsp;+ Tìm hiểu và tạo Global Secondary Index để hỗ trợ truy vấn dữ liệu.<br>&emsp;+ Cấu hình Python, AWS CLI và thư viện Boto3 để kết nối với DynamoDB.<br>&emsp;+ Sử dụng Python và Boto3 để thực hiện CRUD, tải dữ liệu mẫu và quét dữ liệu trong bảng. | 04/11/2026 | 04/11/2026 | [Làm việc với Amazon DynamoDB](https://000060.awsfcaj.com/vi/) |
| 5 | - Thực hành lab **Xây dựng Pipeline dữ liệu ETL không máy chủ với AWS Glue**<br>&emsp;+ Tìm hiểu quy trình ETL và vai trò của AWS Glue.<br>&emsp;+ Tạo Amazon S3 Bucket để lưu trữ dữ liệu CSV đầu vào và dữ liệu Parquet đầu ra.<br>&emsp;+ Cấu hình IAM Role, sử dụng AWS Glue Crawler và Data Catalog để nhận diện cấu trúc dữ liệu.<br>&emsp;+ Xây dựng AWS Glue ETL Job bằng PySpark để làm sạch, chuyển đổi dữ liệu và tính doanh thu.<br>&emsp;+ Khắc phục lỗi Data Catalog và giới hạn chạy đồng thời của Glue Job.<br>&emsp;+ Sử dụng Amazon Athena để truy vấn dữ liệu.<br>&emsp;+ Tìm hiểu cách theo dõi Glue Job bằng Amazon CloudWatch.<br>&emsp;+ Dọn dẹp tài nguyên AWS. | 05/11/2026 | 05/11/2026 | [AWS Glue Documentation](https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html)<br>[AWS Glue IAM Permissions](https://docs.aws.amazon.com/glue/latest/dg/set-up-iam.html)<br>[Amazon Athena Documentation](https://docs.aws.amazon.com/athena/latest/ug/what-is.html)<br>[AWS Glue Pricing](https://aws.amazon.com/glue/pricing/) |
| 6 |  | 06/11/2026 | 06/11/2026 |  |

### Kết quả đạt được tuần 18:

&emsp;◉ Thứ 3:
<br>&emsp;&emsp;○ Cấu hình PayPal Sandbox trên ECS và truy cập được giao diện thanh toán.
<br>&emsp;&emsp;○ Hiển thị thành công hai nút thanh toán PayPal và Debit or Credit Card.
<br>&emsp;&emsp;○ Phát hiện lỗi lưu đơn hàng sau thanh toán và một số lựa chọn PayPal bị trùng, cần tiếp tục xử lý.

&emsp;◉ Thứ 4:
<br>&emsp;&emsp;○ Hiểu cách tạo và quản lý dữ liệu trên Amazon DynamoDB.
<br>&emsp;&emsp;○ Biết sử dụng AWS CLI và Boto3 để thao tác với database.
<br>&emsp;&emsp;○ Thực hành được các chức năng CRUD, Query, Scan và Global Secondary Index.

&emsp;◉ Thứ 5:
<br>&emsp;&emsp;○ Xây dựng thành công ETL Pipeline chuyển đổi dữ liệu CSV sang Parquet.
<br>&emsp;&emsp;○ Chạy thành công AWS Glue ETL Job và tạo bảng dữ liệu đã xử lý.
<br>&emsp;&emsp;○ Hiểu rõ hơn cách kết hợp Amazon S3, AWS Glue, Athena và CloudWatch trong xử lý dữ liệu.