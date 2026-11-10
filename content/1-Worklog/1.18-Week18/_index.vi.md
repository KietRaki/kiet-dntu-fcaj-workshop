---
title: "Worklog Tuần 18"
date: 2026-11-02
weight: 18
chapter: false
pre: " <b> 1.18. </b> "
---

### Mục tiêu tuần 18:

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 02/11/2026 | 02/11/2026 |  |
| 3 | - Thực hiện sửa lỗi và kiểm tra chức năng thanh toán PayPal cho dự án RakiBookery<br>&emsp;+ Kiểm tra cấu hình PayPal Sandbox trên AWS ECS và phát hiện lỗi biến môi trường.<br>&emsp;+ Kiểm tra IAM Role, bổ sung quyền truy cập Parameter Store và Secrets Manager.<br>&emsp;+ Tạo Task Definition revision mới và cập nhật thông tin cấu hình PayPal Sandbox.<br>&emsp;+ Kiểm tra giao diện thanh toán PayPal và Debit or Credit Card.<br>&emsp;+ Thử nghiệm thanh toán bằng PayPal Balance và thẻ Visa. | 03/11/2026 | 03/11/2026 |  |
| 4 | - Thực hành lab **NoSQL Database Essentials with Amazon DynamoDB**<br>&emsp;+ Tìm hiểu cách tạo và quản lý bảng DynamoDB bằng AWS Management Console và AWS CloudShell.<br>&emsp;+ Thực hành thêm, đọc, cập nhật, xóa và truy vấn dữ liệu bằng AWS CLI.<br>&emsp;+ Tìm hiểu và tạo Global Secondary Index để hỗ trợ truy vấn dữ liệu.<br>&emsp;+ Cấu hình Python, AWS CLI và thư viện Boto3 để kết nối với DynamoDB.<br>&emsp;+ Sử dụng Python và Boto3 để thực hiện CRUD, tải dữ liệu mẫu và quét dữ liệu trong bảng. | 04/11/2026 | 04/11/2026 | [Làm việc với Amazon DynamoDB](https://000060.awsfcaj.com/vi/) |
| 5 |  | 05/11/2026 | 05/11/2026 |  |
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