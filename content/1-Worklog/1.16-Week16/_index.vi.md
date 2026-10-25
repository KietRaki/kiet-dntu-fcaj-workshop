---
title: "Worklog Tuần 16"
date: 2026-10-19
weight: 16
chapter: false
pre: " <b> 1.16. </b> "
---

### Mục tiêu tuần 16:

* Thực hành lab phát triển ứng dụng Python nhỏ với AWS.
* Triển khai và kiểm tra kết nối Amazon RDS MySQL với ECS Fargate, cấu hình mạng, bảo mật và giám sát lỗi bằng CloudWatch.

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 19/10/2026 | 19/10/2026 |  |
| 3 |  | 20/10/2026 | 20/10/2026 |  |
| 4 | - Thực hiện một dự án nhỏ về **AWS Laptop Inventory** bằng Python, boto3 và Amazon DynamoDB<br>&emsp;+ Chuẩn bị môi trường Python, AWS CLI và cài đặt boto3.<br>&emsp;+ Tạo bảng **LaptopInventory** trên DynamoDB để lưu trữ thông tin laptop.<br>&emsp;+ Xây dựng ứng dụng CLI hỗ trợ thêm, xem, tìm kiếm, cập nhật và xóa dữ liệu laptop.<br>&emsp;+ Kiểm thử các chức năng CRUD, xử lý lỗi AWS và tìm hiểu cách quản lý thông tin xác thực, bảo mật mã nguồn và tài nguyên cloud. | 21/10/2026 | 21/10/2026 |  |
| 5 | - Chỉnh sửa code SQL<br>&emsp;+ Gộp nội dung **migration_add_paypal.sql** và **migration_promo_and_order.sql** vào bookstoredb.sql.<br>&emsp;+ Sửa lỗi cú pháp *ADD COLUMN IF NOT EXISTS*.<br>&emsp;+ Xử lý các warning về kiểu dữ liệu.<br>&emsp;+ Khắc phục lỗi Safe Update Mode.<br>- Tìm cách kết nối MySQL tới RDS | 22/10/2026 | 22/10/2026 |  |
| 6 | - Thực hành lab **Kết nối MySQL Workbench với RDS**<br>&emsp;+ Tạo VPC, Public Subnet, Private Subnet, Route Table và Security Group phục vụ lab.<br>&emsp;+ Tạo DB Subnet Group, cấu hình RDS MySQL và kiểm tra kết nối qua TCP port 3306.<br>&emsp;+ Cấu hình Parameter Group và xuất Error Log, General Log, Slow Query Log sang CloudWatch.<br>- Triển khai lại task **RDS MySQL Provisioning** cho dự án RakiBookery và làm báo cáo<br>&emsp;+ Tạo DB Subnet Group, RDS MySQL instance và Security Group để kiểm soát kết nối.<br>&emsp;+ Tạo ECS Task Definition và chạy ECS Fargate để kiểm tra kết nối đến RDS.<br>&emsp;+ Sử dụng CloudWatch Logs để phát hiện và xử lý lỗi cấu hình lệnh và xác thực MySQL. | 23/10/2026 | 24/10/2026 |  |

### Kết quả đạt được tuần 16:

&emsp;◉ Thứ 4:
<br>&emsp;&emsp;○ Nắm được cách xây dựng ứng dụng Python kết nối AWS bằng boto3.
<br>&emsp;&emsp;○ Thao tác CRUD với DynamoDB và quản lý thông tin xác thực AWS an toàn.

&emsp;◉ Thứ 5:
<br>&emsp;&emsp;○ Đã thêm PayPal vào bảng PaymentMethod, tạo thêm một bảng `promo`.
<br>&emsp;&emsp;○ Không thể kết nối MySQL tới RDS vì có thể sai cấu hình RDS.

&emsp;◉ Thứ 6:
<br>&emsp;&emsp;○ Hoàn thành cấu hình mạng, RDS và CloudWatch cho lab; chuẩn bị RDS mới để tiếp tục kiểm thử kết nối MySQL Workbench.
<br>&emsp;&emsp;○ Triển khai RDS MySQL ở chế độ private cho dự án RakiBookery, cấu hình ECS Fargate và xác minh kết nối database thành công.
<br>&emsp;&emsp;○ Nâng cao kỹ năng cấu hình mạng AWS, kiểm soát truy cập bằng Security Group và xử lý lỗi kết nối database.