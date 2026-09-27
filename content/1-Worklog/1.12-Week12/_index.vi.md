---
title: "Worklog Tuần 12"
date: 2026-09-21
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Hoàn thành các nhiệm vụ được giao trong tuần này.
* Chụp lại ảnh minh chứng và làm báo cáo một phần của dự án.

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 21/09/2026 | 21/09/2026 |  |
| 3 | - Làm công việc được giao cho dự án - RDS MySQL Provisioning<br>&emsp;+ Tạo DB Subnet Group.<br>&emsp;+ Tạo Security Group cho RDS.<br>&emsp;+ Tạo RDS instance (MySQL).<br>&emsp;+ Import bookstoredb.sql.<br>&emsp;+ Kiểm tra kết nối. | 22/09/2026 | 22/09/2026 |  |
| 4 |  | 23/09/2026 | 23/09/2026 |  |
| 5 | - Chụp lại ảnh minh chứng của quá trình làm RDS MySQL Provisioning do đánh mất ảnh<br>- Làm nội dung báo cáo RDS MySQL Provisioning<br>&emsp;+ Tạo DB Subnet Group.<br>&emsp;+ Tạo Security Group cho RDS.<br>&emsp;+ Tạo RDS instance.<br>&emsp;+ Kiểm tra RDS private. | 24/09/2026 | 24/09/2026 |  |
| 6 | - Làm công việc được giao cho dự án - S3 Buckets<br>&emsp;+ Tạo và cấu hình 3 bucket: S3 Static Web, S3 Media, S3 Logs.<br>&emsp;+ Cấu hình Encryption, Block Public Access và Versioning cho Media.<br>- Làm nội dung báo cáo RDS MySQL Provisioning<br>&emsp;+ Import database vào RDS. | 25/09/2026 | 25/09/2026 |  |

### Kết quả đạt được tuần 12:

&emsp;◉ Thứ 3:
<br>&emsp;&emsp;○ Hoàn thành RDS MySQL Provisioning: RDS MySQL được triển khai trong private network, database bookstoredb được import thành công với 7 bảng và 177 records, đồng thời xác nhận EC2 có thể kết nối tới RDS qua TCP port 3306.
<br>&emsp;&emsp;○ Kết nối SSH từ Windows đến EC2 ban đầu bị timeout do vấn đề Security Group.
<br>&emsp;&emsp;○ Chưa thể kiểm tra Fargate kết nối tới RDS vì Fargate Cluster chưa được tạo.

&emsp;◉ Thứ 5:
<br>&emsp;&emsp;○ Đã có ảnh minh chứng và 60% nội dung báo cáo workshop về các nhiệm vụ của RDS MySQL Provisioning.

&emsp;◉ Thứ 6:
<br>&emsp;&emsp;○ Hoàn thành S3 Buckets: tạo ba S3 Buckets, trong đó bucket Media cấu hình thêm versioning để duy trì nhiều version của cùng một object, giúp khôi phục object khi bị ghi đè hoặc xóa ngoài ý muốn.
<br>&emsp;&emsp;○ Hoàn thành 100% nội dung báo cáo workshop về các nhiệm vụ của RDS MySQL Provisioning.