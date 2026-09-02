---
title: "Worklog Tuần 8"
date: 2026-08-24
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Nắm vững kiến thức về Data Lake và Database trên AWS.
* Thực hành xây dựng data pipeline serverless từ S3 sang DynamoDB bằng Lambda.

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 24/08/2026 | 24/08/2026 |  |
| 3 | - Thực hành lab **Cơ bản về Data Lake trên AWS**<br>&emsp;+ Tìm hiểu tổng quan về Data Lake:<br>&emsp;&emsp;++ Amazon Glue.<br>&emsp;&emsp;++ AWS Athena.<br>&emsp;&emsp;++ Amazon QuickSight.<br>&emsp;+ Chuẩn bị môi trường:<br>&emsp;&emsp;++ Tạo IAM Role.<br>&emsp;&emsp;++ Tạo Policy.<br>&emsp;+ Thu thập và lưu trữ dữ liệu:<br>&emsp;&emsp;++ Tạo S3 Bucket.<br>&emsp;&emsp;++ Tạo Firehose stream. | 25/08/2026 | 25/08/2026 | [Lab 000035](https://000035.awsstudygroup.com/vi/) |
| 4 | - Làm báo cáo thực tập<br>&emsp;+ Sửa lại nội dung Chương 1: Giới thiệu chung về đơn vị thực tập.  | 26/08/2026 | 26/08/2026 |  |
| 5 | - Tìm hiểu về Database<br>&emsp;+ Database, data warehouse, key-value store và document database.<br>&emsp;+ Các dịch vụ NoSQL, cơ sở dữ liệu quan hệ và các dịch vụ database khác.<br>- Thực hành Amazon DynamoDB<br>&emsp;+ Tạo Table.<br>&emsp;+ Thực hiện truy vấn đơn giản bằng PartiQL Editor.<br>- Thực hành Amazon RDS:<br>&emsp;+ Tạo Database với Full Configuration.<br>&emsp;+ Kết nối Database với EC2.<br>&emsp;+ Tạo Table và thêm dữ liệu trên Amazon Linux 2023.<br>- Làm quen với Amazon Redshift<br>- Thực hành Import dữ liệu từ S3 vào DynamoDB<br>&emsp;+ Tạo S3 Bucket và upload file CSV.<br>&emsp;+ Tạo DynamoDB Table.<br>&emsp;+ Import dữ liệu từ S3 vào DynamoDB.<br>&emsp;+ Kiểm tra dữ liệu sau khi import.<br>&emsp;+ Hiểu cách kết hợp S3 và DynamoDB trong data workflow.<br>&emsp;+ Dọn dẹp tài nguyên sau khi hoàn thành. | 27/08/2026 | 27/08/2026 | [AWS Certified Cloud Practitioner (CLF C02)](https://www.youtube.com/playlist?list=PLBfufR7vyJJ4du5ANexy0SuQ0J7KhRcjI) |
| 6 | - Thực hành lab **Serverless Pipeline: Import dữ liệu từ S3 sang DynamoDB**<br>&emsp;+ Chuẩn bị file CSV và tạo S3 bucket.<br>&emsp;+ Tạo thư mục **input** để lưu file CSV.<br>&emsp;+ Tạo DynamoDB table.<br>&emsp;+ Tạo Lambda function và thiết lập S3 trigger.<br>&emsp;+ Cấu hình IAM Permission cho Lambda:<br>&emsp;&emsp;++ **s3:GetObject**.<br>&emsp;&emsp;++ **dynamodb:PutItem** và **dynamodb:BatchWriteItem**.<br>&emsp;+ Xử lý và xác thực dữ liệu CSV.<br>&emsp;+ Giám sát Lambda execution logs bằng CloudWatch. | 28/08/2026 | 28/08/2026 | Lab được tạo từ ChatGPT |

### Kết quả đạt được tuần 8:

&emsp;◉ Thứ 3:
<br>&emsp;&emsp;○ Hiểu kiến trúc cơ bản của Data Lake trên AWS và thực hành các bước chuẩn bị, thu thập và lưu trữ dữ liệu bằng các dịch vụ AWS liên quan.
<br>&emsp;&emsp;○ Gặp lỗi khi tạo CloudFormation stack để tạo dữ liệu mẫu.
<br>&emsp;&emsp;○ Không thể tạo Crawler trong AWS Glue để xây dựng Data Catalog do không có quyền sử dụng.

&emsp;◉ Thứ 5:
<br>&emsp;&emsp;○ Nắm được các loại database phổ biến trên AWS.
<br>&emsp;&emsp;○ Hoàn thành các thao tác cơ bản với DynamoDB, RDS, Redshift, đồng thời thực hành thành công quy trình đưa dữ liệu từ S3 vào DynamoDB.

&emsp;◉ Thứ 6:
<br>&emsp;&emsp;○ Lambda tự động xử lý file CSV ngay khi được upload lên S3.
<br>&emsp;&emsp;○ Các record hợp lệ được lưu vào DynamoDB, còn record không hợp lệ được bỏ qua và ghi log để kiểm tra.
<br>&emsp;&emsp;○ Lambda ban đầu không có quyền đọc dữ liệu từ S3.
<br>&emsp;&emsp;○ DynamoDB không hỗ trợ trực tiếp kiểu dữ liệu float.
<br>&emsp;&emsp;○ Một số record hợp lệ chưa được ghi vào DynamoDB.