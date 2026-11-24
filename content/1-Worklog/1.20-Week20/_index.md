---
title: "Week 20 Worklog"
date: 2026-11-16
weight: 20
chapter: false
pre: " <b> 1.20. </b> "
---

### Week 20 Objectives:

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 16/11/2026 | 16/11/2026 |  |
| 3 |  | 17/11/2026 | 17/11/2026 |  |
| 4 | - Practice the **Web Application Firewall AWS WAF** lab<br>&emsp;+ Create an S3 Bucket and upload a test HTML website.<br>&emsp;+ Configure a CloudFront Distribution and OAC to protect S3 from public access.<br>&emsp;+ Configure AWS WAF and explore AWS Managed Rules.<br>&emsp;+ Add the SQL Database Rule Set to detect and block suspicious SQL Injection requests.<br>&emsp;+ Test normal and suspicious requests and monitor Allow and Block metrics in AWS WAF.<br>&emsp;+ Learn how to monitor security activities through the WAF Dashboard. | 18/11/2026 | 18/11/2026 | [Get started with AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/getting-started.html) |
| 5 | - Practice the **System Management with AWS Systems Manager** lab<br>&emsp;+ Create a VPC, Subnets and two Windows EC2 Instances.<br>&emsp;+ Create an IAM Role and attach it to both EC2 Instances.<br>&emsp;+ Use AWS Systems Manager Fleet Manager.<br>&emsp;+ Create patch policy in Patch Manager.<br>&emsp;+ Use Run Command and PowerShell to execute the `net user` command.<br>&emsp;+ Clean up AWS resources. | 19/11/2026 | 19/11/2026 | [Lab 000031](https://000031.awsfcaj.com) |
| 6 | - Practice the **Data Protection with AWS Backup** lab<br>&emsp;+ Create an S3 Bucket to store lab files.<br>&emsp;+ Use CloudFormation to deploy EC2, SNS and Lambda resources.<br>&emsp;+ Create an AWS Backup Plan and Backup Vault with a daily backup schedule.<br>&emsp;+ Perform EC2 backup and recovery and check Backup Job status.<br>&emsp;+ Configure SNS notifications and use Lambda to automate recovery testing.<br>&emsp;+ Clean up resources. | 20/11/2026 | 20/11/2026 | [Lab 000013](https://000013.awsfcaj.com) |

### Week 20 Achievements:

&emsp;◉ Wednesday:
<br>&emsp;&emsp;○ Successfully deployed a website through CloudFront with HTTPS and AWS WAF.
<br>&emsp;&emsp;○ Configured S3 as a private bucket and used OAC to control access.
<br>&emsp;&emsp;○ Successfully tested SQL Injection detection and blocking, with 2 requests blocked by AWS WAF.

&emsp;◉ Thursday:
<br>&emsp;&emsp;○ Successfully completed the patch scanning and installation process using Patch Manager.
<br>&emsp;&emsp;○ Successfully executed PowerShell commands on both Instances through Run Command.
<br>&emsp;&emsp;○ Understood how to manage EC2 servers, update the operating system and execute commands remotely on AWS.

&emsp;◉ Friday:
<br>&emsp;&emsp;○ Understood the backup and recovery process with AWS Backup.
<br>&emsp;&emsp;○ Understood how to integrate SNS and Lambda for automated recovery testing and notifications.