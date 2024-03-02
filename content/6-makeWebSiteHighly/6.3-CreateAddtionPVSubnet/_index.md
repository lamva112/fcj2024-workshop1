---
title: "Create 2 Additional Private Subnets"
date: "`r Sys.Date()`" 
weight: 3
chapter: false
pre: "<b>6.3</b> "
---

#### Create 2 Additional Private Subnets for EC2 

1. Access the **AWS Management Console**

   - Find **VPC**
   - Select **VPC**
  
![Create VPC](/images/2/000.png?featherlight=false&width=90pc)

2. In the VPC dashboard:
   - Select **Subnet**
   - Choose **Create Subnet**

![Create VPC](/images/6/add-2-subnet/001.png?featherlight=false&width=90pc)

3. In the **Create Subnet** interface:
   - VPC, select **web-app-vpc**

![Create VPC](/images/6/add-2-subnet/002.png?featherlight=false&width=90pc)

4. In the **Subnet settings** section:
   - **Subnet name**, enter **```Private subnet 3```**
   - **Availability Zone**, select **ap-southeast-1a**
   - **IPv4 subnet CIDR block**, enter **```10.10.13.0/24```**
   - Press **Create subnet**

![Create VPC](/images/6/add-2-subnet/003.png?featherlight=false&width=90pc)

5. Similarly, create **```Private subnet 4```** with CIDR **```10.10.14.0/24```**

![Create VPC](/images/6/add-2-subnet/004.png?featherlight=false&width=90pc)

6. Complete the creation of 2 additional private subnets

![Create VPC](/images/6/add-2-subnet/005.png?featherlight=false&width=90pc)
