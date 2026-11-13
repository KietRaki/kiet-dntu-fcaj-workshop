---
title: "Week 19 Worklog"
date: 2026-11-09
weight: 19
chapter: false
pre: " <b> 1.19. </b> "
---

### Week 19 Objectives:

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 | - Work on fixing and redeploying the PayPal payment function for the RakiBookery project<br>&emsp;+ Check the source code and find the cause of the error displaying two identical PayPal methods.<br>&emsp;+ Fix the SQL syntax error in the `Order.php` file and update the order saving process in the `PayPalController.php`.<br>&emsp;+ Adjust `checkout.php` to display only one PayPal method.<br>&emsp;+ Use Docker to build the image and push it to Amazon ECR.<br>&emsp;+ Create a new ECS Task Definition revision and update the ECS Service to deploy the modified version. | 09/11/2026 | 09/11/2026 |  |
| 3 |  | 10/11/2026 | 10/11/2026 |  |
| 4 | - Practice the **Real-Time Data Streaming and Analytics Pipeline on AWS** lab<br>&emsp;+ Create Amazon Kinesis Data Streams to receive real-time order data.<br>&emsp;+ Create an AWS Lambda function to process JSON data, calculate total_amount and add the processed_at timestamp.<br>&emsp;+ Configure Amazon Data Firehose to receive data from Kinesis, process it through Lambda and store it in Amazon S3.<br>&emsp;+ Use Python and Boto3 to build a program that simulates sending orders to Kinesis.<br>&emsp;+ Configure AWS Glue Crawler and Data Catalog to discover the data schema.<br>&emsp;+ Use Amazon Athena to run SQL queries and analyze revenue and best-selling products.<br>&emsp;+ Monitor data processing logs on Amazon CloudWatch. | 11/11/2026 | 11/11/2026 | [Amazon Kinesis](https://docs.aws.amazon.com/streams/latest/dev/)<br>[Amazon Data Firehose](https://docs.aws.amazon.com/firehose/latest/dev/)<br>[Transform source data in Amazon Data Firehose](https://docs.aws.amazon.com/firehose/latest/dev/data-transformation.html)<br>[AWS Lambda](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)<br>[Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)<br>[AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html)<br>[Amazon Athena](https://docs.aws.amazon.com/athena/latest/ug/what-is.html)<br>[Amazon CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html) |
| 5 |  | 12/11/2026 | 12/11/2026 |  |
| 6 |  | 13/11/2026 | 13/11/2026 |  |

### Week 19 Achievements:

&emsp;◉ Monday:
<br>&emsp;&emsp;○ Not successfully deployed due to ECS encountering a connection error with AWS Secrets Manager. Further network troubleshooting is required.

&emsp;◉ Wednesday:
<br>&emsp;&emsp;○ Successfully built a real-time order processing pipeline using Kinesis, Lambda and Firehose.
<br>&emsp;&emsp;○ Successfully sent and processed 30 orders and stored JSON data in S3.
<br>&emsp;&emsp;○ Fixed the data compression issue and successfully queried the data using Amazon Athena.
<br>&emsp;&emsp;○ Gained a better understanding of real-time data collection, processing, storage and analytics on AWS.