---
title: "Week 10 Worklog"
date: 2026-09-07
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 07/09/2026 | 07/09/2026 |  |
| 3 |  | 08/09/2026 | 08/09/2026 |  |
| 4 | - Practice **Building Data Lake with your own data** lab - continue<br>&emsp;+ Amazon S3: store Airbnb data.<br>&emsp;+ Glue DataBrew: Clean & Transform → Parquet.<br>&emsp;+ Amazon Athena: SQL, JOIN, CTAS, VIEW, Partition.<br>&emsp;+ Replace Cloud9, Glue Crawler and Glue ETL due to access issues.<br>&emsp;+ Clean up resources. | 09/09/2026 | 09/09/2026 | [Lab 000070](https://000070.awsstudygroup.com/) |
| 5 |  | 10/09/2026 | 10/09/2026 |  |
| 6 | - Learn about Grafana<br>- Practice **Advanced Monitoring with CloudWatch and Grafana** lab<br>&emsp;+ Create VPC and subnet.<br>&emsp;+ Create Security Group.<br>&emsp;+ Create EC2 Instance.<br>&emsp;+ Create IAM User & Access Key.<br>&emsp;+ Create IAM Role.<br>&emsp;+ Assign IAM Role to EC2 instance.<br>&emsp;+ Install & monitor Grafana.<br>&emsp;+ Clean up resources.<br>- Practice **Optimize EC2 cost with Lambda** lab<br>&emsp;+ Create VPC.<br>&emsp;+ Create Security group.<br>&emsp;+ Create EC2 instance.<br>&emsp;+ Configure Slack Incoming Webhooks.<br>&emsp;+ Create tag for EC2 instance.<br>&emsp;+ Create role for Lambda.<br>&emsp;+ Create Lambda Function:<br>&emsp;&emsp;++ Function stop instance.<br>&emsp;&emsp;++ Function start instance.<br>&emsp;+ Test results.<br>&emsp;+ Clean up resources. | 11/09/2026 | 11/09/2026 | [Lab 000029](https://000029.awsstudygroup.com/)<br>[Lab000022](https://000022.awsstudygroup.com/) |

### Week 10 Achievements:

&emsp;◉ Wednesday:
<br>&emsp;&emsp;○ Completed most of the CSV → S3 → DataBrew → Parquet → Athena pipeline.
<br>&emsp;&emsp;○ Encountered an error while reading Parquet <strong>reviews</strong> and creating <strong>reviews_partition</strong> in Athena.

&emsp;◉ Friday:
<br>&emsp;&emsp;○ Completed setting up an AWS EC2 → Grafana → CloudWatch system, enabling the querying, visualization and monitoring of EC2 metrics within Grafana.
<br>&emsp;&emsp;○ Set up an automated EC2 start/stop mechanism using Lambda with Slack notifications to help optimize EC2 costs.