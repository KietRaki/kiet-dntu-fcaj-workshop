---
title: "Week 12 Worklog"
date: 2026-09-21
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Complete the assigned tasks this week.
* Take proof images and prepare a report for part of the project.

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 21/09/2026 | 21/09/2026 |  |
| 3 | - Do the assigned tasks for the project - RDS MySQL Provisioning<br>&emsp;+ Create DB Subnet Group.<br>&emsp;+ Create Security Group for RDS.<br>&emsp;+ Create RDS instance (MySQL).<br>&emsp;+ Import bookstoredb.sql.<br>&emsp;+ Test the connection. | 22/09/2026 | 22/09/2026 |  |
| 4 |  | 23/09/2026 | 23/09/2026 |  |
| 5 | - Retake the proof images of the RDS MySQL Provisioning process because the original ones was lost.<br>- Create the content for the RDS MySQL Provisioning report<br>&emsp;+ Create DB Subnet Group.<br>&emsp;+ Create Security Group for RDS.<br>&emsp;+ Create RDS instance.<br>&emsp;+ Check RDS private. | 24/09/2026 | 24/09/2026 |  |
| 6 | - Do the assigned tasks for the project - S3 Buckets<br>&emsp;+ Create and configure 3 buckets: S3 Static Web, S3 Media and S3 Logs.<br>&emsp;+ Configure encryption, Block public access and Versioning for Media.<br>- Create the content for the RDS MySQL Provisioning report<br>&emsp;+ Import database to RDS. | 25/09/2026 | 25/09/2026 |  |

### Week 12 Achievements:

&emsp;◉ Tuesday:
<br>&emsp;&emsp;○ Completed RDS MySQL Provisioning: deployed RDS MySQL in a private network, successfully imported bookstoredb with 7 tables and 177 records and confirmed that EC2 can connect to RDS through TCP port 3306.
<br>&emsp;&emsp;○ The initial SSH connection from Windows to EC2 timed out due to Security Group issues.
<br>&emsp;&emsp;○ Fargate to RDS connectivity could not be tested because the Fargate Cluster has not been created yet.

&emsp;◉ Thursday:
<br>&emsp;&emsp;○ Had all the proof images and 60% of the workshop report content for the RDS MySQL Provisioning tasks.

&emsp;◉ Friday:
<br>&emsp;&emsp;○ Completed S3 Buckets: created three S3 buckets, with the "Media" bucket configured for versioning to maintain multiple versions of the same object, enabling recovery in the event of accidental overwriting or deletion.
<br>&emsp;&emsp;○ Completed 100% of the workshop report content for the RDS MySQL Provisioning tasks.