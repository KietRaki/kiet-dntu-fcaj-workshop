---
title: "Event 3"
date: 2026-10-31
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Summary Report: “FCAJ - Community Day 31/10”

{{< img src="images/4-EventParticipated/event3/GroupPhoto_Event3.jpg" alt="Group Photo of Event 3" >}}

## Event Objectives

FCAJ - Community Day 31/10 was organized to provide students, developers and individuals interested in cloud computing with opportunities to learn from experienced professionals and exchange practical knowledge about AWS technologies.

The event aimed to introduce effective AWS learning paths, explore the application of Artificial Intelligence (AI) in software development, understand Serverless architecture and learn how to build asynchronous systems. It also encouraged participants to explore Open-Source contributions, keep up with emerging technologies and gain practical experience for their future careers in the Cloud Computing industry.

## Speakers

1\. Tran Minh Tuan: Backend Developer and FPT University student. Presented "A Guide to Learning AWS and Getting Started with AWS for Beginners".

2\. Henry Duc Bui: Head of Engineering at Cloud Tinker. Presented "Learnings from Building Software Factory", focusing on applying AI Agents throughout the software development lifecycle.

3\. Phuc Khang (Khang Duong): Member of First Cloud Journey. Presented "3 Months of Internship at First Cloud Journey", sharing practical experience in building applications using AWS Serverless architecture.

4\. Thinh Nguyen: DevOps / Cloud Engineer at Style Solution. Presented "AWS Lambda Web Function: Rethinking Serverless Web Architecture", introducing improvements in building web applications with Lambda.

5\. Luong Cam Dao: Member of First Cloud Journey. Presented "Building Asynchronous Systems with Amazon SQS", focusing on message queue architecture and implementation.

6\. Hung Tran: Senior Cloud Engineer at NAP and Top 25 AWS CDK Contributor. Presented "Start and Maintain Consistency with Open-Source Code Contribution", sharing practical experience and strategies for contributing to Open-Source projects.

## Key Highlights

### Learning AWS and Building a Learning Roadmap for Beginners

Tran Minh Tuan introduced three learning platforms: AWS Study Group, AWS Skill Builder and AWS Builder Center. AWS Skill Builder provides theoretical courses and structured learning paths, AWS Study Group offers hands-on labs, while AWS Builder Center helps learners connect with the community and share technical knowledge. He recommended a learning process that includes studying theory, practicing through labs, documenting knowledge and building personal projects. He also emphasized the importance of cleaning up AWS resources after completing labs to avoid unexpected costs.

### Applying AI Agents to the Software Development Lifecycle

Henry Duc Bui shared practical experience in building a Software Factory by integrating AI Agents into the entire Software Development Lifecycle (SDLC). A team of only 5-6 members successfully processed and merged nearly 3,000 Merge Requests in one month, achieving three times the previous month's productivity. Key practices included involving AI in feature discussions, using Divergent Prompting to explore different solutions and automating code reviews and testing. This presentation demonstrated how AI can significantly improve development productivity and automate technical tasks.

### Building Real-World Applications with AWS Serverless Architecture

Phuc Khang introduced a real-time multiplayer turn-based card game developed during his internship at First Cloud Journey. The system used AWS Lambda for backend logic, DynamoDB for data storage, SQS and EventBridge for asynchronous event management and Cognito with API Gateway/WebSocket for user authentication and real-time communication. He also discussed practical mistakes, including excessive requests caused by using SQS for countdown management, insufficient IAM permissions management and missing Lambda version control. These experiences emphasized the importance of security and Infrastructure as Code (IaC) using AWS CDK and CloudFormation.

### Introducing AWS Lambda Web Function and Modern Serverless Architecture

Thinh Nguyen discussed the limitations of traditional AWS Lambda, including Cold Starts, API Gateway dependency and execution-time-based billing. He then introduced Lambda Web Function, which supports Docker container packaging, handles up to 128 concurrent requests per instance and integrates directly with CloudFront through Origin Access Control (OAC). According to the presentation, CPU processing-time-based billing can reduce costs by approximately 40-70%. He also demonstrated a practical MBTI quiz application to illustrate this architecture.

### Building Asynchronous Systems with Amazon SQS

Luong Cam Dao explained the differences between synchronous and asynchronous processing. Instead of making users wait for an AI service to complete a request, Amazon SQS can act as an intermediate message queue. The API service sends jobs to the queue and immediately returns a Pending status, while the AI service processes those jobs independently. He introduced Standard Queue and FIFO Queue, along with important mechanisms such as Visibility Timeout, Heartbeat, Long Polling and Dead Letter Queue (DLQ). The presentation also demonstrated how Amazon SNS and SQS can work together using the Fan-out pattern to distribute messages to multiple queues.

### Open-Source Contribution and Maintaining Consistency

Hung Tran shared his experience contributing to Open-Source projects, particularly AWS CDK, Terraform and Pulumi. He encouraged beginners to start with issues labeled Good First Issue or Ready to Implement, create smaller Pull Requests and remain patient throughout the review process. He recommended spending approximately 15-30 minutes every day contributing to Open-Source projects. He also emphasized developing a proactive mindset by identifying and fixing issues directly in the source code instead of waiting for service providers to introduce new features or provide official support.