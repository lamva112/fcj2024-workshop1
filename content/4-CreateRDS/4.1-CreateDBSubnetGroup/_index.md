---
title: "Create DB Subnet Group"
date: "`r Sys.Date()`" 
weight: 1 
chapter: false
pre: "<b>4.1</b> "
---

#### Create DB Subnet Group on AWS

1. Access the **AWS Management Console**

   - Find **RDS**
   - Select **RDS**

![Create VPC](/images/4/db-subnet-group/001.png?featherlight=false&width=90pc)

2. In the **RDS** interface:

   - Select **Subnet groups**
   - Choose **Create DB Subnet group**

![Create VPC](/images/4/db-subnet-group/002.png?featherlight=false&width=90pc)

3. In the **Add subnets** interface:
     - **Name**, enter **```webapp-db-subnet-group```**
     - **Description**, enter **```DB Subnet group```**
     - Select **web-app-vpc** VPC

![Create VPC](/images/4/db-subnet-group/003.png?featherlight=false&width=90pc)

4. In the **Add subnets** interface:
   - **Availability Zones**, choose **ap-southeast-1a** and **ap-southeast-1b**
   - **Subnets**, choose **10.10.11.0/24** for **ap-southeast-1a** and **10.10.12.0/24** for **ap-southeast-1b**
   - Click **Create**

![Create VPC](/images/4/db-subnet-group/004.png?featherlight=false&width=90pc)

5. DB Subnet Group creation completed

![Create VPC](/images/4/db-subnet-group/005.png?featherlight=false&width=90pc)
