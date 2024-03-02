---
title: "Introduction"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: "<b> 1. </b>"
---

#### Introduction to 2-tier Architecture

The 2-tier architecture is similar to a client-server application where direct communication occurs between the client and the server. There is no intermediary between the client and the server. Due to the tight coupling, a two-tier application runs faster.

The two-tier architecture is divided into two parts:

1. Client Application (Client Tier)

2. Database (Data Tier)

![Architect](/images/1-Introduce/architecture2.png?featherlight=false&width=30pc)

On the client application side the code is written for saving the data in the SQL server database. Client sends the request to the server and it processes the request & sends it back with data. The main problem of two tier architecture is the server cannot respond to multiple requests at the same time, as a result it causes a data integrity issue.

It’s also called server-client technology.

**Advantages:**

- Easy to maintain and modification is bit easy
- Communication is faster
  
**Disadvantages:**

- In two tier architecture application performance will be degraded as soon as the number of users increases.
- Cost-ineffective

Here is a simple explanation of deploying a two-tier web application architecture on the AWS infrastructure.

![Architect](/images/1-Introduce/full-2-tier-with-53.svg?featherlight=false&width=40pc)

{{% notice info %}}
In the scope of this lab, we only use VPC, EC2, ALB, and RDS services to understand the 2-tier architecture. In reality, additional services such as S3, Route53, and CloudFront are needed.
{{% /notice %}}

Here you can see that a custom VPC is created to secure your web application, and we have distributed all resources across two availability zones (AZs) to provide redundancy for scheduled system maintenance. Therefore, each availability zone is hosting at least one instance for each service, except for services designed for redundancy (e.g., Load Balancers, etc.).

The Web tier consists of two web servers (one in each availability zone) deployed on Elastic Compute Cloud (EC2) instances. We balance external traffic to the servers using an Application Load Balancer (ALB).

The Database tier, using the Relational Database Service (RDS), provides a relational environment (MySQL, MS SQL, or Oracle) for this solution. In this design, we can also provide read replicas to alleviate the load on the primary database. To optimize costs, additional read replicas are created in each availability zone as required.