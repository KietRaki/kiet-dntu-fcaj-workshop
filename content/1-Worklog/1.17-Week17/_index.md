---
title: "Week 17 Worklog"
date: 2026-10-26
weight: 17
chapter: false
pre: " <b> 1.17. </b> "
---

### Week 17 Objectives:

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 26/10/2026 | 26/10/2026 |  |
| 3 |  | 27/10/2026 | 27/10/2026 |  |
| 4 | - Check AWS resources before connecting the PHP web to RDS<br>&emsp;+ Check ECS Task Definition: Create a new revision of RakiBookery-task.<br>&emsp;+ Update ECS Service: Switched to created revision from Task Definition.<br>&emsp;+ Check ECS Status: Confirm that the task was running.<br>&emsp;+ Check Target Group: Verify the status to be Healthy.<br>&emsp;+ Test the Website: Access the website through the ALB DNS name.<br>- Learn **Functional Programming Concepts in Python** course in Codefinity<br>&emsp;+ Packing and Unpacking in Python.<br>&emsp;+ Higher-Order Functions and Lambdas.<br>&emsp;+ Variable Scope, Nested Functions and Closures. | 28/10/2026 | 28/10/2026 |  |
| 5 |  | 29/10/2026 | 29/10/2026 |  |
| 6 | - Deploy the process of connecting PHP Web with RDS for the RakiBookery project<br>&emsp;+ Fix CSS errors on the website using the CloudFront link.<br>&emsp;+ Use Docker and Amazon ECR to prepare the SQL data import process.<br>&emsp;+ Create an ECS Task to import SQL data using AWS Secrets Manager.<br>&emsp;+ Use CloudWatch Logs to verify the imported data.<br>&emsp;+ Update the Docker image, configure PHP database connectivity and deploy the application to ECS Fargate.<br>&emsp;+ Test the website through CloudFront, including product search, filtering and sorting. | 30/10/2026 | 30/10/2026 |  |

### Week 17 Achievements:

&emsp;◉ Wednesday:
<br>&emsp;&emsp;○ The RakiBookery website was accessible through the ALB, the ECS task was running and the Target Group was Healthy.
<br>&emsp;&emsp;○ These checks prepared the environment for testing the PHP application's connection to RDS.
<br>&emsp;&emsp;○ Complete 63% of **Functional Programming Concepts in Python** course.

&emsp;◉ Friday:
<br>&emsp;&emsp;○ Successfully connected the PHP website to Amazon RDS MySQL.
<br>&emsp;&emsp;○ Displayed 20 products retrieved from the database.
<br>&emsp;&emsp;○ Verified that product search, category filtering, price filtering and sorting functions worked correctly.