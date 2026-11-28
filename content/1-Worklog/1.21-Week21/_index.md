---
title: "Week 21 Worklog"
date: 2026-11-23
weight: 21
chapter: false
pre: " <b> 1.21. </b> "
---

### Week 21 Objectives:

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 23/11/2026 | 23/11/2026 |  |
| 3 |  | 24/11/2026 | 24/11/2026 |  |
| 4 | - Practice the **Building a Serverless Data Warehouse with Amazon Redshift** lab.<br>&emsp;+ Create an S3 Bucket and IAM Role.<br>&emsp;+ Configure Amazon Redshift Serverless and connect through Query Editor v2.<br>&emsp;+ Import the `Prices.csv` dataset into Redshift.<br>&emsp;+ Practice SQL queries, analyze food prices and create analytical Views.<br>&emsp;+ Use AWS Glue Crawler to create a Data Catalog.<br>&emsp;+ Monitor Redshift metrics using Amazon CloudWatch.<br>&emsp;+ Create a snapshot to restore data in case of an incident. | 25/11/2026 | 25/11/2026 | [Opening query editor v2](https://docs.aws.amazon.com/redshift/latest/mgmt/query-editor-v2-open.html)<br>[Loading Data from Amazon S3](https://docs.aws.amazon.com/redshift/latest/mgmt/query-editor-v2-loading-data.html)<br>[Credentials and access permissions](https://docs.aws.amazon.com/redshift/latest/dg/loading-data-access-permissions.html)<br>[Snapshots and recovery points](https://docs.aws.amazon.com/redshift/latest/mgmt/serverless-snapshots-recovery-points.html)<br>[Creating a snapshot](https://docs.aws.amazon.com/redshift/latest/mgmt/serverless-snapshots.html)<br>[Amazon Redshift Serverless backups](https://docs.aws.amazon.com/aws-backup/latest/devguide/redshift-serverless-backups.html) |
| 5 | - Write a blog for the **Building a Serverless Data Warehouse with Amazon Redshift** lab | 26/11/2026 | 26/11/2026 |  |
| 6 | - Practice the **In-Memory Caching with Amazon ElastiCache** lab<br>&emsp;+ Create a separate VPC for ElastiCache, configure public/private subnets, route tables and security groups.<br>&emsp;+ Deploy EC2 client and Amazon ElastiCache Redis OSS.<br>&emsp;+ Connect EC2 to Redis via TLS using Redis CLI.<br>&emsp;+ Practice Redis data structures: string, hash, list, set and sorted set.<br>&emsp;+ Use Python and the redis-py library to connect to Redis, perform CRUD operations and manage data TTL.<br>&emsp;+ Practice Redis streams, pub/sub to log events and exchange messages.<br>&emsp;+ Clean up AWS resources. | 27/11/2026 | 27/11/2026 | [Managing clusters in ElastiCache](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/Clusters.html)<br>[Python and ElastiCache](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/ElastiCache-Getting-Started-Tutorials-Python.html)<br>[Creating a cluster for Valkey or Redis OSS](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/Clusters.Create.html)<br>[Role-Based Access Control (RBAC)](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/Clusters.RBAC.html)<br>[Creating a node-based ElastiCache cluster for Redis OSS](https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/SubnetGroups.designing-cluster-pre.redis.html)<br>[redis-py - Python Client for Redis](https://redis.readthedocs.io/en/stable/) |

### Week 21 Achievements:

&emsp;◉ Wednesday:
<br>&emsp;&emsp;○ Gained practical experience in building a Data Warehouse with Amazon Redshift.
<br>&emsp;&emsp;○ Understood how to analyze data using SQL on Query Editor v2.
<br>&emsp;&emsp;○ Learned how to use Glue Data Catalog and CloudWatch for data management and monitoring.
<br>&emsp;&emsp;○ Understood the backup and recovery process using Redshift Snapshots.

&emsp;◉ Friday:
<br>&emsp;&emsp;○ Knew how to deploy and connect Amazon ElastiCache in a private VPC environment.
<br>&emsp;&emsp;○ Understood how to use Redis CLI and Python to manipulate data.
<br>&emsp;&emsp;○ Understood the application of Redis in caching, data management and event transmission.