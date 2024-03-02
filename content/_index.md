---
title : "Deploy 2-tier web application"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
# Starting with 2 Tier Application

#### Overview

A 2-tier web application is a popular software architecture in which the components of the application are divided into two main tiers: the user interface tier and the service or processing logic tier. In this model, the user interface tier is responsible for displaying data and interacting with users, while the service or processing logic tier performs tasks such as processing logic, retrieving data, and interacting with databases or other systems.

When deploying a 2-tier application on AWS (Amazon Web Services), there are several important services and resources that you can use:

1. **EC2 (Elastic Compute Cloud)**: EC2 provides scalable virtual machines that you can use to deploy components of your application, including both the user interface tier and the service tier.

2. **RDS (Relational Database Service)**: RDS offers relational database services such as MySQL, PostgreSQL, SQL Server, and Oracle. You can use RDS to store data for your application.

3. **ELB (Elastic Load Balancing)**: ELB enables distributing traffic across your EC2 instances, enhancing the scalability and reliability of your application.

4. **VPC (Virtual Private Cloud)**: VPC allows you to create a virtual network environment within AWS to deploy your application, providing security and access control.

In this lab, we will explore the concept of a 2-tier web application and how to execute it in the AWS environment.

#### Content
1. [Introduction to 2-tier](1-introduce/)
2. [Prerequisite steps](2-Prerequiste/)
3. [Create EC2 server](3-CreateEc2Server/)
4. [Create RDS database](4-CreateRDS/)
5. [Install and configure web application on EC2 server](5-Installandconfigurewebapp/)
6. [Create a highly available 2-tier web application](6-makeWebSiteHighly/)
7. [Configure Public DNS with Route53](7-setup-public-dns/)
8. [Clean up resources](8-cleanUpResource/)
