---
title: "Worklog Tuần 7"
date: 2026-08-17
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Tìm hiểu và thực hành các dịch vụ AWS về giám sát, điện toán và lưu trữ, tập trung vào CloudWatch, EC2, ECS, Lambda, S3, EBS và EFS.

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 17/08/2026 | 17/08/2026 |  |
| 3 | - Thực hành lab **Giám sát hệ thống với Amazon CloudWatch**<br>&emsp;+ Tạo CloudFormation stack.<br>&emsp;+ Làm việc với CloudWatch Metrics:<br>&emsp;&emsp;++ Xem và tìm kiếm Metrics.<br>&emsp;&emsp;++ Thực hiện các phép toán trên Metrics.<br>&emsp;&emsp;++ Tạo Dynamic Labels.<br>&emsp;+ Làm việc với CloudWatch Logs:<br>&emsp;&emsp;++ CloudWatch Logs.<br>&emsp;&emsp;++ CloudWatch Logs Insights.<br>&emsp;&emsp;++ CloudWatch Metric Filter.<br>&emsp;+ Tạo CloudWatch Alarms.<br>&emsp;+ Tạo CloudWatch Dashboards.<br>&emsp;+ Dọn dẹp tài nguyên. | 18/08/2026 | 18/08/2026 | [Lab 000008](https://000008.awsstudygroup.com/vi/) |
| 4 | - Tìm hiểu Amazon EC2 và các mô hình điện toán<br>&emsp;+ Tổng quan về EC2.<br>&emsp;+ Máy ảo, container và serverless.<br>&emsp;+ High Performance Computing (HPC).<br>&emsp;+ Edge computing và Hybrid computing.<br>&emsp;+ Quản lý chi phí và năng suất.<br>- Thực hành các dịch vụ Compute trên AWS<br>&emsp;+ Khởi chạy EC2 Instance.<br>&emsp;+ Tạo ECS Cluster và Task Definition.<br>&emsp;+ Triển khai ECS Task.<br>&emsp;+ Kiểm tra CloudWatch.<br>&emsp;+ Tạo Lambda Function.<br>&emsp;+ Xóa ECS Cluster và terminate EC2 Instance. | 19/08/2026 | 19/08/2026 | [AWS Certified Cloud Practitioner (CLF C02)](https://www.youtube.com/playlist?list=PLBfufR7vyJJ4du5ANexy0SuQ0J7KhRcjI)<br>[Compute Follow Along](https://www.youtube.com/watch?v=hLC-_TwIQk8) |
| 5 | - Tìm hiểu các dịch vụ lưu trữ trên AWS<br>&emsp;+ Các loại Storage Services.<br>&emsp;+ Tổng quan về Amazon S3.<br>&emsp;+ Các S3 Storage Classes.<br>&emsp;+ AWS Snow Family.<br>&emsp;+ Các dịch vụ Storage khác.<br>- Thực hành Amazon S3 đơn giản<br>&emsp;+ Truy cập S3 trên AWS Console.<br>&emsp;+ Tạo S3 Bucket.<br>&emsp;+ Tải file lên Bucket.<br>&emsp;+ Xem các file trong Bucket.<br>&emsp;+ Thiết lập Lifecycle Rules.<br>&emsp;+ Xóa Bucket.<br>- Xem tổng quan về EBS trong EC2.<br>- Thực hành Amazon EFS đơn giản | 20/08/2026 | 20/08/2026 | [AWS Certified Cloud Practitioner (CLF C02)](https://www.youtube.com/playlist?list=PLBfufR7vyJJ4du5ANexy0SuQ0J7KhRcjI)<br>[S3 Follow Along](https://www.youtube.com/watch?v=c3ECovVQc1Y) |
| 6 |  | 21/08/2026 | 21/08/2026 |  |

### Kết quả đạt được tuần 7:

&emsp;◉ Thứ 3:
<br>&emsp;&emsp;○ Hoàn thành các bước cơ bản để giám sát hệ thống bằng Metrics, Logs, Alarms và Dashboards trên Amazon CloudWatch.
<br>&emsp;&emsp;○ Không thể thực thi lệnh tải logger.py từ S3 trên web terminal của EC2.

&emsp;◉ Thứ 4:
<br>&emsp;&emsp;○ Hiểu các mô hình compute phổ biến trên AWS và hoàn thành thực hành cơ bản với EC2, ECS và Lambda.

&emsp;◉ Thứ 5:
<br>&emsp;&emsp;○ Hiểu các loại dịch vụ lưu trữ chính trên AWS và hoàn thành các thao tác cơ bản với S3, EBS và EFS.