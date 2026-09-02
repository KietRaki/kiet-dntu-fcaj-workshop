---
title: "Blog 1"
date: 2026-08-30
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Building a Serverless Pipeline: Import data from S3 to DynamoDB

Hello everyone, my name is Nguyen Vu Tuan Kiet and I am currently working as a Data Analyst. After two months of my internship, I have had the opportunity to learn more about AWS services, especially services related to data storage, processing and analysis. Besides studying the theory, I also wanted to build small labs by myself to better understand how these services can be combined into a practical system.

In this blog, I will share a lab that I completed with the goal of building a simple data processing pipeline using a serverless architecture. If you are also interested in the Data field like me, you can follow this lab to understand how AWS services work together. Specifically, I used Amazon S3 to store CSV files, AWS Lambda to read and process the data, Amazon DynamoDB to store the processed data and Amazon CloudWatch to monitor logs. When a new CSV file is uploaded to S3, Lambda is automatically triggered to read the file, validate each record and write valid records to DynamoDB.

**1. Lab overview**

In data processing systems, a common workflow is to receive data from an external source, validate and process the data and then store it in a system that applications can use. In this lab, I simulated a simple scenario where product data is provided as a CSV file.

The architecture I built consists of four main components:
<br>&emsp;&#8211; Amazon S3.
<br>&emsp;&#8211; AWS Lambda.
<br>&emsp;&#8211; Amazon DynamoDB.
<br>&emsp;&#8211; Amazon CloudWatch.

S3 is used to store the input file. When a CSV file is uploaded to a specific folder in S3, S3 generates an event that triggers Lambda. Lambda then reads the CSV file, processes each row and checks conditions such as whether product_id exists, whether price is a valid number and whether stock is non-negative. Valid records are written to DynamoDB, while invalid records are skipped and warning information is written to CloudWatch Logs.

![Import from S3 to DynamoDB](/images/3-BlogsPosted/blog1/Serverless-Pipeline_Import-from-S3-to-DynamoDB.drawio.png)

**2. Preparing data in Amazon S3**

First, I created an S3 bucket to store the input data. Inside the bucket, I used the input/ folder to store the CSV files that needed to be processed. Using this prefix allowed me to control which files would trigger Lambda instead of allowing every object in the bucket to generate an event.

The sample data file has the following structure:
```
product_id,product_name,category,price,stock
P001,Laptop Dell,Electronics,1200,15
P002,Wireless Mouse,Accessories,25,100
P003,Mechanical Keyboard,Accessories,75,50
P004,Monitor 27 inch,Electronics,350,30
P005,USB-C Hub,Accessories,45,80
P006,Webcam HD,Electronics,60,40
P007,Headphones,Audio,120,25
P008,Smartphone,Electronics,800,20
P009,Desk Lamp,Home,35,60
P010,Office Chair,Home,250,10
```

I named the file `products-test.csv`.

After uploading the file to input/, S3 generates an Object Created event. This event contains important information such as the bucket name and object key of the uploaded file. Lambda can use this information to identify exactly which file needs to be read and processed.

**3. Processing Data with AWS Lambda**

The main part of the lab is Lambda. I used Python and boto3 so that Lambda could interact with S3 and DynamoDB. When Lambda receives an S3 event, it retrieves the bucket name and object key, then uses `s3.get_object()` to read the CSV file directly from S3.

After reading the file, Lambda uses `csv.DictReader` to convert each row in the CSV into a dictionary. This allows me to easily access fields such as product_id, product_name, category, price and stock to perform validation before writing the data to DynamoDB.

One issue I encountered during the lab was that DynamoDB through boto3 does not support Python float values when writing data. Initially, I used `float(row["price"])`, but Lambda returned the error `Float types are not supported`. After investigating the error, I changed the implementation to use **Decimal** from the Python decimal module. This was a useful error to encounter because it helped me understand how boto3 handles Number data types when working with DynamoDB.

**4. Validating and handling invalid data**

I did not want one invalid record to cause the entire CSV file import to fail. Therefore, I designed Lambda to validate each record individually. If **product_id** is missing, Lambda logs a warning and skips the record. Similarly, if the price cannot be converted to a **Decimal**, or the stock cannot be converted to an integer, the record is marked as **invalid**.

For example, I created another CSV file with the following data:
```
product_id,product_name,category,price,stock
P011,Tablet,Electronics,500,35
P012,Gaming Mouse,Accessories,55,70
P013,USB Microphone,Audio,90,25
P014,Invalid Product,Electronics,ABC,20
,Missing ID,Electronics,100,10
P015,Negative Price,Electronics,-50,20
```

I named the file `products-test-2.csv`.

Lambda processes each row individually. P011, P012 and P013 are valid records, so they are written to DynamoDB. P014 has `price = ABC`, so it is skipped. The record without a product_id is also skipped. P015 has a negative price, so it is not inserted into DynamoDB either.

One change I made after testing was to use `batch_writer()` during the file processing. This allows valid records to be added to a batch for writing to DynamoDB, while invalid records are skipped using **continue**. CloudWatch Logs also records information about the total number of records, valid records and invalid records.

**5. Storing data in Amazon DynamoDB**

After validation is completed for each record, Lambda uses DynamoDB `batch_writer()` to write the data. I created a table named **products** and used **product_id** as the Partition Key.

An item in DynamoDB looks like this:
```
{
    "product_id": "P011",
    "product_name": "Tablet",
    "category": "Electronics",
    "price": 500,
    "stock": 35
}
```

Using `batch_writer()` makes the code more suitable for cases where many records need to be imported. In this small lab, the amount of data is not large, but this approach helped me become familiar with processing multiple records instead of sending a separate request for each record.

After Lambda runs successfully, I can go to **DynamoDB → Tables → Select the created table → Explore table items** to check the data. With the test file above, only valid products appear in the table.

**6. Monitoring Lambda with CloudWatch**

During the lab, **Amazon CloudWatch Logs** was one of the tools I used most often to check whether Lambda was working correctly. I added logs such as the bucket name, object key, number of records and the status of each record to make the processing flow easier to monitor.

For example, when a record is invalid, the log may display:

```[WARNING] Invalid price or stock. Skipping record: {...}```

For a valid record:

```[INFO] Successfully processed: P011```

At the end of the processing, Lambda records a summary:
```
========== Processing Summary ==========
[INFO] Total records: 8
[INFO] Valid records: 4
[INFO] Invalid records: 4
========================================
```

Having clear logs makes it easier for me to identify problems when the pipeline does not work as expected.

**7. What I learned**

Through this lab, I gained a better understanding of how to build an event-driven serverless pipeline on AWS. Previously, I mainly approached AWS services at a conceptual level, but after connecting S3, Lambda and DynamoDB myself, I could clearly see how data moves through each component of the system.

I also gained more experience with IAM because I needed to grant Lambda permissions such as `s3:GetObject` and permission to write data to DynamoDB. I found this part particularly important because Lambda can run normally but still be unable to process data if its Execution Role does not have the required permissions.

In addition, handling invalid data helped me realize that a data pipeline needs validation and error handling from the beginning. Instead of allowing one incorrect row to cause the entire Lambda execution to fail, I can identify the invalid record, log the error and continue processing the remaining records.

**8. Issues I encountered during the lab**

During the lab, I encountered several practical issues.

The first was an **AccessDenied** error when Lambda tried to read a file from S3. The cause was that the Lambda Execution Role did not have the `s3:GetObject` permission. After checking CloudWatch Logs and the IAM Role, I added the required permission for the appropriate S3 bucket and the `input/*` prefix.

Next, I encountered the following error:
```
TypeError: Float types are not supported.
Use Decimal types instead.
```

This error occurred when I converted price to a Python float before writing it to DynamoDB. I replaced **float(**) with **Decimal()** and imported **InvalidOperation** so that I could also handle invalid values such as ABC.

Finally, I encountered an issue when processing invalid records. Initially, if a record caused an exception, Lambda could stop before writing the remaining valid records. After restructuring the code and handling exceptions inside the loop, Lambda could skip invalid records and continue processing the following records.

**9. Conclusion**

For me, this lab was also a small step in my internship journey at Amazon Web Services Vietnam. Instead of studying each service separately, I want to continue building labs with more complete architectures so that I can better understand how AWS services work together to solve practical problems. From the current pipeline, I can further develop the system by adding components such as Amazon EventBridge, Amazon SNS, Step Functions, or CloudWatch Alarms to build a system with better monitoring and error handling capabilities.