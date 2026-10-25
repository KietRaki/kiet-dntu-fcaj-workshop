---
title: "Week 16 Worklog"
date: 2026-10-19
weight: 16
chapter: false
pre: " <b> 1.16. </b> "
---

### Week 16 Objectives:

* Practice developing a small Python application with AWS lab.
* Deploying and testing Amazon RDS MySQL connectivity with ECS Fargate, including network configuration, security and error monitoring with CloudWatch.

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 19/10/2026 | 19/10/2026 |  |
| 3 |  | 20/10/2026 | 20/10/2026 |  |
| 4 | - Practice the **AWS Laptop Inventory** mini project using Python, boto3 and Amazon DynamoDB.<br>&emsp;+ Set up the Python environment, AWS CLI and boto3.<br>&emsp;+ Create the **LaptopInventory** table in DynamoDB to store laptop information.<br>&emsp;+ Build a CLI application to add, list, search, update and delete laptop records.<br>&emsp;+ Test CRUD operations, handled AWS-related errors and learn about credential management, source code security and cloud resource cleanup. | 21/10/2026 | 21/10/2026 |  |
| 5 | - Edit SQL code<br>&emsp;+ Merge the contents of **migration_add_paypal.sql** and **migration_promo_and_order.sql** into bookstoredb.sql.<br>&emsp;+ Fix the syntax error *ADD COLUMN IF NOT EXISTS*.<br>&emsp;+ Handle warnings about data types.<br>&emsp;+ Fix the Safe Update Mode error.<br>- Find a way to connect MySQL to RDS | 22/10/2026 | 22/10/2026 |  |
| 6 | - Practice the lab **Connecting MySQL Workbench to RDS**.<br>&emsp;+ Create a VPC, public and private subnets, route tables and security groups for the lab.<br>&emsp;+ Create DB Subnet Groups, configure RDS MySQL and check TCP connectivity on port 3306.<br>&emsp;+ Configure a Parameter Group and prepare Error Logs, General Logs and Slow Query Logs for CloudWatch.<br>- Reimplement the **RDS MySQL Provisioning** task for the RakiBookery project and prepare a report.<br>&emsp;+ Create a DB Subnet Group, RDS MySQL instance and security groups to control database access.<br>&emsp;+ Create an ECS Task Definition and run ECS Fargate to test the connection to RDS.<br>&emsp;+ Use CloudWatch Logs to identify, troubleshoot command configuration and MySQL authentication errors. | 23/10/2026 | 24/10/2026 |  |

### Week 16 Achievements:

&emsp;◉ Wednesday:
<br>&emsp;&emsp;○ Learned how to build a Python application that connects to AWS using boto3.
<br>&emsp;&emsp;○ Performed CRUD operations with DynamoDB and manages AWS credentials securely.

&emsp;◉ Thursday:
<br>&emsp;&emsp;○ Added PayPal to the PaymentMethod table, created an additional `promo` table.
<br>&emsp;&emsp;○ Unable to connect MySQL to RDS because the RDS configuration might be incorrect.

&emsp;◉ Friday:
<br>&emsp;&emsp;○ Completed the network, RDS and CloudWatch configuration for the lab and prepared a new RDS instance for further MySQL Workbench connectivity testing.
<br>&emsp;&emsp;○ Deployed a private RDS MySQL instance for RakiBookery, configured ECS Fargate and successfully verified database connectivity.
<br>&emsp;&emsp;○ Improved practical skills in AWS networking, Security Group access control and database connectivity troubleshooting.