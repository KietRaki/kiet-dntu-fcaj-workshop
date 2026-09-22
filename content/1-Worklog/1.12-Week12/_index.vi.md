---
title: "Worklog Tuần 12"
date: 2026-09-21
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 21/09/2026 | 21/09/2026 |  |
| 3 | - Làm công việc được giao cho dự án<br>&emsp;+ Import database bookstoredb.sql:<br>&emsp;&emsp;++ Tạo EC2 tạm thời RakiBookery-rds-import để làm máy trung gian.<br>&emsp;&emsp;++ Kết nối SSH từ Windows đến EC2.<br>&emsp;&emsp;++ Cài MySQL client.<br>&emsp;&emsp;++ Đưa file bookstoredb.sql lên EC2 và import vào RDS.<br>&emsp;+ Kiểm tra database sau khi import:<br>&emsp;&emsp;++ Xác nhận database bookstoredb tồn tại.<br>&emsp;&emsp;++ Kiểm tra dữ liệu có thiếu gì không.<br>&emsp;&emsp;++ Kiểm tra kết nối EC2 tới RDS bằng TCP port 3306.<br>&emsp;+ Chuẩn bị cho kết nối Fargate:<br>&emsp;&emsp;++ Xác định RDS sẽ cho phép Fargate Security Group truy cập port 3306.<br>&emsp;&emsp;++ Sẽ thực hiện kiểm tra sau khi thành viên phụ trách ECS hoàn thành tạo Cluster. | 22/09/2026 | 22/09/2026 |  |
| 4 |  | 23/09/2026 | 23/09/2026 |  |
| 5 |  | 24/09/2026 | 24/09/2026 |  |
| 6 |  | 25/09/2026 | 25/09/2026 |  |

### Kết quả đạt được tuần 12:

&emsp;◉ Thứ 3:
<br>&emsp;&emsp;○ Hoàn thành phần chính của task: RDS MySQL được triển khai trong private network, database bookstoredb được import thành công với 7 bảng và 177 records, đồng thời xác nhận EC2 có thể kết nối tới RDS qua TCP port 3306.
<br>&emsp;&emsp;○ Kết nối SSH từ Windows đến EC2 ban đầu bị timeout do vấn đề Security Group.
<br>&emsp;&emsp;○ Chưa thể kiểm tra Fargate kết nối tới RDS vì Fargate Cluster chưa được tạo.