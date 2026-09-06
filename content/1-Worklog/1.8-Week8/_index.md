---
title: "Week 8 Worklog"
date: 2026-08-24
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Gain a solid understanding of Data Lakes and Databases on AWS.
* Practice how to build a serverless data pipeline that transfers data from S3 to DynamoDB using Lambda.

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 24/08/2026 | 24/08/2026 |  |
| 3 | - Practice **Data Lake Fundamentals on AWS** lab<br>&emsp;+ Learn the fundamentals of Data Lakes:<br>&emsp;&emsp;++ Amazon Glue.<br>&emsp;&emsp;++ AWS Athena.<br>&emsp;&emsp;++ Amazon QuickSight.<br>&emsp;+ Prepare the environment:<br>&emsp;&emsp;++ Create an IAM role.<br>&emsp;&emsp;++ Create a policy.<br>&emsp;+ Collect and store data:<br>&emsp;&emsp;++ Create an S3 Bucket.<br>&emsp;&emsp;++ Create a Firehose stream. | 25/08/2026 | 25/08/2026 | [Lab 000035](https://000035.awsstudygroup.com/) |
| 4 | - Do the internship report<br>&emsp;+ Revise the content of Chapter 1: General introduction to the internship unit. | 26/08/2026 | 26/08/2026 |  |
| 5 | - Learn about Databases<br>&emsp;+ Database, data warehouse, key-value store and document database.<br>&emsp;+ NoSQL, relational database service (RDS) and other database services.<br>- Practice Amazon DynamoDB<br>&emsp;+ Create a table.<br>&emsp;+ Perform basic queries using the PartiQL editor.<br>- Practice Amazon RDS<br>&emsp;+ Create a database with Full Configuration.<br>&emsp;+ Connect the database to EC2.<br>&emsp;+ Create tables and insert data using Amazon Linux 2023.<br>- Learn the basics of Amazon Redshift<br>- Practice importing data from S3 into DynamoDB<br>&emsp;+ Create an S3 Bucket and uploaded a CSV file.<br>&emsp;+ Create a DynamoDB table.<br>&emsp;+ Import data from S3 into DynamoDB.<br>&emsp;+ Verify the imported data.<br>&emsp;+ Understand how S3 and DynamoDB can work together in a data workflow.<br>&emsp;+ Clean up resources after completion. | 27/08/2026 | 27/08/2026 | [AWS Certified Cloud Practitioner (CLF C02)](https://www.youtube.com/playlist?list=PLBfufR7vyJJ4du5ANexy0SuQ0J7KhRcjI) |
| 6 | - Practice **Serverless Pipeline: Import Data from S3 to DynamoDB** lab<br>&emsp;+ Prepare a CSV file and created an S3 Bucket.<br>&emsp;+ Create a folder named **input** to store the CSV file.<br>&emsp;+ Create a DynamoDB Table.<br>&emsp;+ Create a Lambda Function and configured an S3 Trigger.<br>&emsp;+ Configured IAM Permissions for Lambda:<br>&emsp;&emsp;++ **s3:GetObject**.<br>&emsp;&emsp;++ **dynamodb:PutItem** and **dynamodb:BatchWriteItem**.<br>&emsp;+ Process and validate CSV data.<br>&emsp;+ Monitor Lambda execution logs using CloudWatch. | 28/08/2026 | 28/08/2026 | Lab was practiced by ChatGPT |

### Week 8 Achievements:

&emsp;◉ Tuesday:
<br>&emsp;&emsp;○ Understood the basic Data Lake architecture on AWS and practiced the preparation, data collection and storage steps using related AWS services.
<br>&emsp;&emsp;○ Encountered an error when creating the CloudFormation Stack for sample data.
<br>&emsp;&emsp;○ Could not create a Crawler in AWS Glue to build the Data Catalog because the required permissions were not available.

&emsp;◉ Thursday:
<br>&emsp;&emsp;○ Understood the common AWS database services.
<br>&emsp;&emsp;○ Completed basic hands-on tasks with DynamoDB, RDS and Redshift, including a data import workflow from S3 to DynamoDB.

&emsp;◉ Friday:
<br>&emsp;&emsp;○ Lambda automatically processed the CSV file after it was uploaded to S3.
<br>&emsp;&emsp;○ Valid records were stored in DynamoDB, while invalid records were skipped and logged for further inspection.
<br>&emsp;&emsp;○ Lambda initially did not have permission to read data from S3
<br>&emsp;&emsp;○ DynamoDB does not directly support the float data type
<br>&emsp;&emsp;○ Some valid records were not written to DynamoDB.