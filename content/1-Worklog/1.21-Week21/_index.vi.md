---
title: "Worklog Tuần 21"
date: 2026-11-23
weight: 21
chapter: false
pre: " <b> 1.21. </b> "
---

### Mục tiêu tuần 21:

### Các công việc đã làm trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
|:---:|---|:---:|:---:|---|
| 2 |  | 23/11/2026 | 23/11/2026 |  |
| 3 |  | 24/11/2026 | 24/11/2026 |  |
| 4 | - Thực hành lab **Xây dựng một kho dữ liệu phi máy chủ với Amazon Redshift**<br>&emsp;+ Tạo S3 Bucket và IAM Role.<br>&emsp;+ Cấu hình Amazon Redshift Serverless và kết nối thông qua Query Editor v2.<br>&emsp;+ Import dataset `Prices.csv` vào Redshift.<br>&emsp;+ Thực hành truy vấn SQL, thống kê giá thực phẩm và tạo View phân tích.<br>&emsp;+ Sử dụng AWS Glue Crawler để tạo Data Catalog.<br>&emsp;+ Theo dõi các chỉ số hoạt động của Redshift bằng Amazon CloudWatch.<br>&emsp;+ Tạo snapshot để khôi phục dữ liệu khi xảy ra sự cố. | 25/11/2026 | 25/11/2026 | [Opening query editor v2](https://docs.aws.amazon.com/redshift/latest/mgmt/query-editor-v2-open.html)<br>[Loading Data from Amazon S3](https://docs.aws.amazon.com/redshift/latest/mgmt/query-editor-v2-loading-data.html)<br>[Credentials and access permissions](https://docs.aws.amazon.com/redshift/latest/dg/loading-data-access-permissions.html)<br>[Snapshots and recovery points](https://docs.aws.amazon.com/redshift/latest/mgmt/serverless-snapshots-recovery-points.html)<br>[Creating a snapshot](https://docs.aws.amazon.com/redshift/latest/mgmt/serverless-snapshots.html)<br>[Amazon Redshift Serverless backups](https://docs.aws.amazon.com/aws-backup/latest/devguide/redshift-serverless-backups.html) |
| 5 | - Làm blog cho lab **Xây dựng một kho dữ liệu phi máy chủ với Amazon Redshift** | 26/11/2026 | 26/11/2026 |  |
| 6 | - Thực hành lab **Bộ nhớ đệm trong bộ nhớ với Amazon ElastiCache**<br>&emsp;+ Tạo VPC riêng cho ElastiCache, cấu hình public/private subnets, route tables và security groups.<br>&emsp;+ Triển khai EC2 client và Amazon ElastiCache Redis OSS.<br>&emsp;+ Kết nối EC2 với Redis thông qua TLS bằng Redis CLI.<br>&emsp;+ Thực hành các cấu trúc dữ liệu Redis: string, hash, list, set và sorted set.<br>&emsp;+ Sử dụng python và thư viện redis-py để kết nối Redis, thực hiện CRUD và quản lý TTL dữ liệu.<br>&emsp;+ Thực hành Redis streams và pub/sub để ghi nhận sự kiện và trao đổi thông điệp.<br>&emsp;+ Dọn dẹp các tài nguyên AWS. | 27/11/2026 | 27/11/2026 | [Managing clusters in ElastiCache](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/Clusters.html)<br>[Python and ElastiCache](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/ElastiCache-Getting-Started-Tutorials-Python.html)<br>[Creating a cluster for Valkey or Redis OSS](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/Clusters.Create.html)<br>[Role-Based Access Control (RBAC)](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/Clusters.RBAC.html)<br>[Creating a node-based ElastiCache cluster for Redis OSS](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/SubnetGroups.designing-cluster-pre.redis.html)<br>[redis-py - Python Client for Redis](https://redis.readthedocs.io/en/stable/) |

### Kết quả đạt được tuần 21:

&emsp;◉ Thứ 4:
<br>&emsp;&emsp;○ Nắm được quy trình xây dựng Data Warehouse trên Amazon Redshift.
<br>&emsp;&emsp;○ Biết phân tích dữ liệu bằng SQL trên Query Editor v2.
<br>&emsp;&emsp;○ Biết cách sử dụng Glue Data Catalog và CloudWatch để quản lý, theo dõi dữ liệu.
<br>&emsp;&emsp;○ Biết cách sao lưu và khôi phục dữ liệu bằng Redshift Snapshot.

&emsp;◉ Thứ 6:
<br>&emsp;&emsp;○ Biết cách triển khai và kết nối Amazon ElastiCache trong môi trường VPC riêng.
<br>&emsp;&emsp;○ Nắm được cách sử dụng Redis CLI và Python để thao tác dữ liệu.
<br>&emsp;&emsp;○ Hiểu ứng dụng của Redis trong caching, quản lý dữ liệu và truyền tải sự kiện.