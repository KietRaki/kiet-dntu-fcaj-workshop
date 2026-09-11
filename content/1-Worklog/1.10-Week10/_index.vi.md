---
title: "Worklog Tuần 10"
date: 2026-09-07
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 07/09/2026 | 07/09/2026 |  |
| 3 |  | 08/09/2026 | 08/09/2026 |  |
| 4 | - Thực hành lab **Xây dựng Data Lake với dữ liệu của riêng bạn** - tiếp theo<br>&emsp;+ Amazon S3: lưu dữ liệu Airbnb.<br>&emsp;+ Glue DataBrew: Clean & Transform → Parquet.<br>&emsp;+ Amazon Athena: SQL, JOIN, CTAS, VIEW, Partition.<br>&emsp;+ Thay thế Cloud9, Glue Crawler và Glue ETL do vấn đề quyền truy cập. | 09/09/2026 | 09/09/2026 | [Lab 000070](https://000070.awsstudygroup.com/vi/) |
| 5 |  | 10/09/2026 | 10/09/2026 |  |
| 6 | - Tìm hiểu về Grafana<br>- Thực hành lab **Giám sát nâng cao với CloudWatch và Grafana**<br>&emsp;+ Tạo VPC và subnet.<br>&emsp;+ Tạo Security Group.<br>&emsp;+ Tạo EC2 Instance.<br>&emsp;+ Tạo IAM User & Access Key.<br>&emsp;+ Tạo IAM Role.<br>&emsp;+ Gán IAM Role vào EC2 instance.<br>&emsp;+ Cài đặt và giám sát Grafana.<br>&emsp;+ Dọn dẹp tài nguyên. | 11/09/2026 | 11/09/2026 | [Lab 000029](https://000029.awsstudygroup.com/vi/) |

### Kết quả đạt được tuần 10:

&emsp;◉ Thứ 4:
<br>&emsp;&emsp;○ Đã hoàn thành phần lớn pipeline CSV → S3 → DataBrew → Parquet → Athena.
<br>&emsp;&emsp;○ Gặp lỗi khi đọc <strong>reviews</strong> Parquet và tạo <strong>reviews_partition</strong> trong Athena.

&emsp;◉ Thứ 6:
<br>&emsp;&emsp;○ Xây dựng được hệ thống AWS EC2 → Grafana → CloudWatch, cho phép truy vấn, trực quan hóa và theo dõi metric của EC2 trên Grafana.