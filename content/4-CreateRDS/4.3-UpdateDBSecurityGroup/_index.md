---
title: "Update DB security group"
date: "`r Sys.Date()`" 
weight: 3
chapter: false
pre: "<b>4.3</b> "
---

#### Update DB security group to allow traffic from VPC CIDR

1. In the **Amazon RDS** interface:
   - Select **Database**
   - Open **webapp-db**

![Create VPC](/images/4/db-sg/001.png?featherlight=false&width=90pc)

2. In the **webapp-db** interface:
   - Select **Connectivity & Security** 
   - Click on the VPC Security groups link (this will open the EC2 console with the selected DB security group)

![Create VPC](/images/4/db-sg/002.png?featherlight=false&width=90pc)
![Create VPC](/images/4/db-sg/003.png?featherlight=false&width=90pc)

3. Open **webapp-db-security-group**
   - Select **Inbound rules**
   - Select **Edit inbound rules**

![Create VPC](/images/4/db-sg/004.png?featherlight=false&width=90pc)

4. In the **Edit inbound rules** interface:
   - Update source to **```10.10.0.0/16```**
   - Select **Save rules**

![Create VPC](/images/4/db-sg/006.png?featherlight=false&width=90pc)
