---
title: "Worklog Tuần 20"
date: 2026-11-16
weight: 20
chapter: false
pre: " <b> 1.20. </b> "
---

### Mục tiêu tuần 20:

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 16/11/2026 | 16/11/2026 |  |
| 3 |  | 17/11/2026 | 17/11/2026 |  |
| 4 | - Thực hành lab **Web Application Firewall AWS WAF**<br>&emsp;+ Tạo S3 Bucket và tải website HTML thử nghiệm lên S3.<br>&emsp;+ Cấu hình CloudFront Distribution và OAC để bảo vệ S3 khỏi truy cập công khai.<br>&emsp;+ Cấu hình AWS WAF và tìm hiểu các AWS Managed Rules.<br>&emsp;+ Thêm SQL Database Rule Set để phát hiện và chặn các request có dấu hiệu SQL Injection.<br>&emsp;+ Kiểm tra request bình thường và request độc hại, theo dõi số liệu Allow và Block trên AWS WAF.<br>&emsp;+ Tìm hiểu cách theo dõi hoạt động bảo mật thông qua WAF Dashboard. | 18/11/2026 | 18/11/2026 | [Get started with AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/getting-started.html) |
| 5 | - Thực hành lab **Quản lý hệ thống với AWS Systems Manager**<br>&emsp;+ Tạo VPC, Subnet và hai Windows EC2 Instance.<br>&emsp;+ Tạo IAM Role và gán quyền cho hai EC2 Instance.<br>&emsp;+ Sử dụng AWS Systems Manager Fleet Manager.<br>&emsp;+ Tạo patch policy trong Patch Manager.<br>&emsp;+ Sử dụng Run Command và PowerShell để thực thi lệnh `net user`.<br>&emsp;+ Dọn dẹp các tài nguyên. | 19/11/2026 | 19/11/2026 | [Lab 000031](https://000031.awsfcaj.com/vi) |
| 6 | - Thực hành lab **Bảo vệ dữ liệu với AWS Backup**<br>&emsp;+ Tạo S3 Bucket để lưu trữ các file phục vụ bài lab.<br>&emsp;+ Sử dụng CloudFormation triển khai EC2, SNS và Lambda.<br>&emsp;+ Tạo AWS Backup Plan, Backup Vault và cấu hình lịch sao lưu hằng ngày.<br>&emsp;+ Thực hiện sao lưu, khôi phục EC2 và kiểm tra trạng thái Backup Job.<br>&emsp;+ Cấu hình SNS gửi thông báo và Lambda tự động kiểm tra khả năng khôi phục.<br>&emsp;+ Dọn dẹp tài nguyên. | 20/11/2026 | 20/11/2026 | [Lab 000013](https://000013.awsfcaj.com/vi) |

### Kết quả đạt được tuần 20:

&emsp;◉ Thứ 4:
<br>&emsp;&emsp;○ Triển khai thành công website qua CloudFront với HTTPS và AWS WAF.
<br>&emsp;&emsp;○ Cấu hình S3 ở chế độ private và sử dụng OAC để kiểm soát truy cập.
<br>&emsp;&emsp;○ Kiểm thử thành công khả năng phát hiện và chặn SQL Injection, với 2 request bị AWS WAF chặn.

&emsp;◉ Thứ 5: 
<br>&emsp;&emsp;○ Thực hiện thành công quá trình kiểm tra và cài đặt bản cập nhật bằng Patch Manager.
<br>&emsp;&emsp;○ Chạy thành công lệnh PowerShell trên cả hai Instance thông qua Run Command.
<br>&emsp;&emsp;○ Hiểu cách quản lý máy chủ EC2, cập nhật hệ điều hành và thực thi lệnh từ xa trên AWS.

&emsp;◉ Thứ 6: 
<br>&emsp;&emsp;○ Hiểu quy trình sao lưu và khôi phục dữ liệu với AWS Backup.
<br>&emsp;&emsp;○ Hiểu cách kết hợp SNS và Lambda để tự động hóa kiểm tra và thông báo.