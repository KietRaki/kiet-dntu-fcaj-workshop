---
title: "Week 9 Worklog"
date: 2026-08-31
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Deploying websites with GitHub Pages.
* Build AWS data pipelines.
* Focusing on real-time data processing with Kinesis, Lambda and DynamoDB.
* Build a Data Lake using S3 and Glue.

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 31/08/2026 | 31/08/2026 |  |
| 3 |  | 01/09/2026 | 01/09/2026 |  |
| 4 | - Set up GitHub Pages to deploy the workshop website<br>&emsp;+ Create a repository.<br>&emsp;+ Configure GitHub Actions.<br>&emsp;+ Resolve the **function "try" not defined** error caused by different Hugo versions.<br>&emsp;+ Configure GitHub Pages to use GitHub Actions.<br>&emsp;+ Check and address image display issues. | 02/09/2026 | 02/09/2026 |  |
| 5 | - Practice **Real-Time Transaction Processing Pipeline** lab<br>&emsp;+ Amazon S3: input data storage.<br>&emsp;+ Amazon EC2: producer send data.<br>&emsp;+ Amazon Kinesis Data Streams: real-time data streaming.<br>&emsp;+ AWS Lambda: data processing.<br>&emsp;+ Amazon DynamoDB: Transactions and Customer Summary tables.<br>&emsp;+ IAM Roles and CloudWatch: permissions, monitoring, and alarms. | 03/09/2026 | 03/09/2026 | Lab was practiced from ChatGPT |
| 6 | - Practice **Building a DataLake with your own data** lab<br>&emsp;+ VS Code + AWS CLI instead of Cloud9 → upload data to S3.<br>&emsp;+ S3 → store raw / cleaned / parquet.<br>&emsp;+ Glue DataBrew → profile, clean and transform the data.<br>&emsp;+ Glue ETL → CSV → Parquet - cannot use this service. | 04/09/2026 | 04/09/2026 | [Lab 000070](https://000070.awsstudygroup.com/)<br>[How to Host a Website on GitHub Pages Free](https://youtu.be/e5AwNU3Y2es) |

### Week 9 Achievements:

&emsp;◉ Wednesday:
<br>&emsp;&emsp;○ Completed the process of building and deploying the workshop website to GitHub Pages.
<br>&emsp;&emsp;○ Identified and addressed issues related to the Hugo version, GitHub Pages configuration and image paths.

&emsp;◉ Thursday:
<br>&emsp;&emsp;○ Successfully built a real-time transaction processing pipeline from S3 → EC2 → Kinesis → Lambda → DynamoDB.

&emsp;◉ Friday:
<br>&emsp;&emsp;○ Uploaded the data to S3, practiced Glue DataBrew to profile, clean and transform, creating a cleaned CSV.
<br>&emsp;&emsp;○ Unable to perform Glue ETL Job (CSV → Parquet) due to lack of access permissions.