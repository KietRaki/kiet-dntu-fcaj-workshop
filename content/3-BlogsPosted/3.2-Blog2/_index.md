---
title: "Blog 2"
date: 2026-11-26
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# Building a Serverless Data Warehouse with Amazon Redshift

Hi everyone, about 2 months ago I posted a blog about **Building a Serverless Pipeline: Importing Data from S3 to DynamoDB**. Looking back, I felt that lab was too simple and did not focus enough on data safety and storage. So during my internship, I learned about a very interesting service called Amazon Redshift — a cloud-based data warehouse service on AWS that is fully managed for storing and analyzing large-scale data.

In this blog, I will share a lab called **Building a Data Warehouse with Amazon Redshift Serverless**. While learning about Data Analytics, I realized that data plays an important role in business operations. Data is used for analysis, decision-making and managing business activities. Therefore, storing and protecting data safely is a necessary requirement.

In reality, data can be lost for many reasons, such as accidental deletion, system errors, or processing failures. Without a proper backup plan, a business can spend a lot of time and money to recover data. Therefore, I chose this lab to learn how to build a data warehouse on AWS, while also practicing backup and recovery methods using Amazon Redshift.

## Lab walkthrough

### 1. Preparing and storing data on Amazon S3

First, I created an S3 Bucket to store the `Prices.csv` dataset. This CSV file contains 155 records and 8 columns related to food prices, including product name, product form, retail price and price per cup equivalent unit.

After creating the Bucket, I uploaded the file to the `raw/` folder and enabled the Versioning feature to keep different versions of the object. This helps protect the original data in case the file is overwritten or accidentally deleted.

### 2. Configuring IAM and Amazon Redshift Serverless

Next, I created an IAM Role with the necessary permissions so that Amazon Redshift can read data from S3. I used limited access only to the specific Bucket for this lab instead of granting broad permissions.

After that, I created a Redshift Serverless with namespace `prices-namespace` and workgroup `prices-workgroup`. This is the main component of the system, responsible for storing and processing data.

Once the configuration was complete, I attached the IAM Role to Redshift to allow the service to access the CSV file on S3.

### 3. Loading and analyzing data with Query Editor v2

I used Amazon Redshift Query Editor v2 to connect to the Data Warehouse, create the `food_analytics` schema and create the `prices` table.

After configuring the COPY command to load data from S3, I checked the result and confirmed the table had all 155 records.

Next, I practiced SQL queries to analyze the data, such as:
<br>&emsp;&#8211; Counting the number of products by category: Fresh, Canned, Frozen, Dried and Juice.
<br>&emsp;&#8211; Calculating the average, minimum and maximum retail price.
<br>&emsp;&#8211; Finding the top 10 most expensive products.
<br>&emsp;&#8211; Comparing prices across different product forms.
<br>&emsp;&#8211; Finding products with a low Cup Equivalent Price.

In addition, I created a View called `vw_price_summary` to store summary results and tried creating charts in Query Editor v2 to visualize the data.

### 4. Using AWS Glue to manage metadata

After finishing the data processing in Redshift, I continued to practice with AWS Glue.

I created a database called `prices_catalog` and a crawler called `prices_csv_crawler`, then configured the crawler to read data from the `raw/` folder in S3.

When the crawler ran successfully, AWS Glue automatically collected information about the CSV file structure and created metadata in the Data Catalog. Through this, I better understood the role of Glue in managing data metadata.

### 5. Monitoring the system with Amazon CloudWatch

For the monitoring part, I used Amazon CloudWatch to track the activity of Redshift Serverless.

I explored and selected several important metrics such as QueryDuration, QueriesCompletedPerSecond, QueriesRunning, QueriesSucceeded, ComputeCapacity, ComputeSeconds, DatabaseConnections and DataStorage.

Then, I created a dashboard called `Redshift-Prices-Monitoring` with chart groups for query performance, compute usage, database connections, storage capacity and query execution time.

I also ran some additional SQL queries to generate activity in Redshift and observed the changes in the CloudWatch metrics. Through this section, I better understood how to monitor performance and check the health of a Data Warehouse.

### 6. Performing backup and disaster recovery

This was the most important part of the lab. I backed up the data using the Manual Snapshot feature of Amazon Redshift Serverless, naming the snapshot `prices-before-disaster`.

After the snapshot was complete, I simulated a disaster by dropping the `food_analytics.prices` table using the SQL command `DROP TABLE`. When I checked again, the query could not run because the table had been deleted.

Next, I used the snapshot to restore the system. The restore process creates a new namespace, so I needed to connect Query Editor v2 to the corresponding workgroup to verify the data after recovery.

The check showed that the `prices` table was restored with all 155 records. I also checked the `vw_price_summary` View to confirm the data was fully recovered.

In addition, I practiced using AWS Backup to manage backup activities for Redshift Serverless, with similar results to Redshift. Through this, I gained more experience with managing Backup Plans and Recovery Points.

## AWS Architecture diagram

{{< img src="images/3-BlogsPosted/blog2/Building-a-Serverless-Data-Warehouse-with-Amazon-Redshift.png" alt="Building a Serverless Data Warehouse with Amazon Redshift" >}}

## Conclusion

After completing the lab, I can confirm that building a data warehouse system on AWS can bring many benefits when developing websites or applications that handle large amounts of data.

This lab gave me a more practical understanding of how AWS services work together in a data system. Through this experience, I want to continue learning about Data Analytics and not stop there. I also want to explore Data Engineering so I can apply what I have learned to real projects in the future.

I encourage anyone who is learning AWS or wants to explore Data Analytics or Engineering to try this lab. It can help you get familiar with Amazon Redshift Serverless, S3, IAM, Glue and CloudWatch through a relatively complete data processing workflow.

If you have the chance to try it, please pay attention to IAM permissions, service configuration and AWS usage costs. Make sure to check and clean up your resources after finishing to avoid unexpected charges.