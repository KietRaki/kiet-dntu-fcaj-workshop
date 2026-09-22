---
title: "Week 12 Worklog"
date: 2026-09-21
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

### Tasks completed this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|:---:|---|:---:|:---:|---|
| 2 |  | 21/09/2026 | 21/09/2026 |  |
| 3 | - Do the assigned tasks for the project<br>&emsp;+ Import database bookstoredb.sql:<br>&emsp;&emsp;++ Create a temporary EC2 instance RakiBookery-rds-import as an intermediate server.<br>&emsp;&emsp;++ Connect from Windows to EC2 via SSH.<br>&emsp;&emsp;++ Install MySQL client.<br>&emsp;&emsp;++ Upload bookstoredb.sql to EC2 and import it into RDS.<br>&emsp;+ Verified the database after import:<br>&emsp;&emsp;++ Confirm that the bookstoredb database exists.<br>&emsp;&emsp;++ Check if the data is not missing anything.<br>&emsp;&emsp;++ Test the EC2 to RDS connection through TCP port 3306.<br>&emsp;+ Prepare for Fargate connectivity:<br>&emsp;&emsp;++ Confirmed that RDS will allow the Fargate Security Group to access port 3306.<br>&emsp;&emsp;++ Could not test Fargate to RDS because the Fargate Cluster has not been created yet.<br>&emsp;&emsp;++ Will perform the test after the member responsible for ECS completes the Cluster setup. | 22/09/2026 | 22/09/2026 |  |
| 4 |  | 23/09/2026 | 23/09/2026 |  |
| 5 |  | 24/09/2026 | 24/09/2026 |  |
| 6 |  | 25/09/2026 | 25/09/2026 |  |

### Week 12 Achievements:

&emsp;◉ Tuesday:
<br>&emsp;&emsp;○ Completed the main task: deployed RDS MySQL in a private network, successfully imported bookstoredb with 7 tables and 177 records and confirmed that EC2 can connect to RDS through TCP port 3306.
<br>&emsp;&emsp;○ The initial SSH connection from Windows to EC2 timed out due to Security Group issues.
<br>&emsp;&emsp;○ Fargate to RDS connectivity could not be tested because the Fargate Cluster has not been created yet.