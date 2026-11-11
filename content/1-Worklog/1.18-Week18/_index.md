---
title: "Week 18 Worklog"
date: 2026-11-02
weight: 18
chapter: false
pre: " <b> 1.18. </b> "
---

### Week 18 Objectives:

* Check and fix the PayPal payment functionality for the RakiBookery project.
* Practice NoSQL data management using Amazon DynamoDB, AWS CLI and Boto3.
* Build a serverless ETL pipeline using AWS Glue to process, transform and query data.

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 02/11/2026 | 02/11/2026 |  |
| 3 | - Work on fixing and testing the PayPal payment function for the RakiBookery project<br>&emsp;+ Check the PayPal Sandbox configuration on AWS ECS and identified environment variable issues.<br>&emsp;+ Review the IAM Role and update permissions for Parameter Store and Secrets Manager.<br>&emsp;+ Create new Task Definition revision and update PayPal Sandbox settings.<br>&emsp;+ Test the PayPal and Debit or Credit Card payment buttons.<br>&emsp;+ Test payments using PayPal Balance and a Visa card. | 03/11/2026 | 03/11/2026 |  |
| 4 | - Practice the lab **NoSQL Database Essentials with Amazon DynamoDB**<br>&emsp;+ Learn how to create and manage DynamoDB tables using AWS Management Console and AWS CloudShell.<br>&emsp;+ Practice adding, reading, updating, deleting and querying data using AWS CLI.<br>&emsp;+ Learn how to create and use Global Secondary Indexes for data queries.<br>&emsp;+ Configure Python, AWS CLI and Boto3 to connect to DynamoDB.<br>&emsp;+ Use Python and Boto3 to perform CRUD operations, load sample data and scan table data. | 04/11/2026 | 04/11/2026 | [Work with Amazon DynamoDB](https://000060.awsfcaj.com/) |
| 5 | - Practice the **Building a Serverless ETL Data Pipeline with AWS Glue** lab<br>&emsp;+ Learn about the ETL process and the role of AWS Glue.<br>&emsp;+ Create an Amazon S3 bucket to store raw CSV data and processed Parquet data.<br>&emsp;+ Configure an IAM Role, use AWS Glue Crawler and Data Catalog to discover data schemas.<br>&emsp;+ Build an AWS Glue ETL Job using PySpark to clean, transform and calculate sales revenue.<br>&emsp;+ Troubleshoot Data Catalog errors and Glue Job concurrency limits.<br>&emsp;+ Use Amazon Athena to query and analyze data.<br>&emsp;+ Learn how to monitor Glue Jobs with Amazon CloudWatch.<br>&emsp;+ Clean up AWS resources. | 05/11/2026 | 05/11/2026 | Lab was created by ChatGPT |
| 6 |  | 06/11/2026 | 06/11/2026 |  |

### Week 18 Achievements:

&emsp;◉ Tuesday:
<br>&emsp;&emsp;○ Configured PayPal Sandbox on ECS and successfully accessed the payment interface.
<br>&emsp;&emsp;○ Successfully displayed the PayPal and Debit or Credit Card payment options.
<br>&emsp;&emsp;○ Identified an order-saving error after payment and duplicate PayPal options that still need to be fixed.

&emsp;◉ Wednesday:
<br>&emsp;&emsp;○ Understood how to create and manage data in Amazon DynamoDB.
<br>&emsp;&emsp;○ Knew how to use AWS CLI and Boto3 to interact with databases.
<br>&emsp;&emsp;○ Practiced CRUD operations, Query, Scan and Global Secondary Indexes.

&emsp;◉ Thursday:
<br>&emsp;&emsp;○ Successfully built an ETL pipeline that converts CSV data into Parquet format.
<br>&emsp;&emsp;○ Successfully executed an AWS Glue ETL Job and created a processed data table.
<br>&emsp;&emsp;○ Gained a better understanding of how Amazon S3, AWS Glue, Athena and CloudWatch work together in data processing.