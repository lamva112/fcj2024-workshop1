---
title: "Create RDS Database instance"
date: "`r Sys.Date()`" 
weight: 2
chapter: false
pre: "<b>4.2</b> "
---

#### Create a DB Instance on AWS

1. In the **RDS** interface:

   - Select **Databases**
   - Click **Create database**

![Create VPC](/images/4/db-instance/001.png?featherlight=false&width=90pc)

2. In the **Create database** interface:
   - For **Choose a database creation method**, select **Standard create**
   - For **Engine options**, choose **MySQL**

![Create VPC](/images/4/db-instance/002.png?featherlight=false&width=90pc)

3. Choose **Templates** for this DB instance as **Free tier**

![Create VPC](/images/4/db-instance/003.png?featherlight=false&width=90pc)

4. To set up your main password, follow these steps:
   - For **DB instance identifierInfo**, enter **```webapp-db```**
   - Open **Credential Settings**
   - Keep the **Master username** as **admin**
   - Enter **Master password** and **Confirm master password**

{{% notice warning %}}
You cannot view the main user's password. If you don't record it, you may need to change it later. If you need to change the main user's password after the DB Instance is ready, you can modify the DB Instance to do this. For more information on modifying a DB Instance, see **Modifying an Amazon RDS DB Instance.**
{{% /notice %}}

![Create VPC](/images/4/db-instance/004.png?featherlight=false&width=90pc)

5. In the **Connectivity** section:

   - For **Compute resource**, select **Don’t connect to an EC2 compute resource**. We will set up the connection to EC2 in the next section.
   - For **Virtual private cloud (VPC)**, choose **web-app-vpc**
   - For **DB subnet group**, select **webapp-db-subnet-group**
   - For **Public access**, choose **No**

![Create VPC](/images/4/db-instance/005.png?featherlight=false&width=90pc)

6. For **VPC security group (firewall)**:

   - Choose **Create new**
   - For **New VPC security group name**, enter **webapp-db-security-group**

![Create VPC](/images/4/db-instance/006.png?featherlight=false&width=90pc)

7. Open **Additional configuration** and enter **```corp```** for **Initial database name**

![Create VPC](/images/4/db-instance/007.png?featherlight=false&width=90pc)

8. Select **Create** and the DB instance will start initializing

![Create VPC](/images/4/db-instance/008.png?featherlight=false&width=90pc)

9. Wait for about 5 minutes for the **status** to change to **available**

![Create VPC](/images/4/db-instance/009.png?featherlight=false&width=90pc)
