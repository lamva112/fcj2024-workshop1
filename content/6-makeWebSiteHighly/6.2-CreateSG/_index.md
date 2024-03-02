---
title: "Create security group"
date: "`r Sys.Date()`" 
weight: 2
chapter: false
pre: "<b>6.2</b> "
---

#### Create security group for the new EC2 instance

As per the initial design, the EC2 instance is placed in a private subnet, so we need to ensure that the security groups applied to the EC2 instance allow connections from resources within the same VPC.

1. In the EC2 interface, select **Security Groups**
   - Choose **Create security group**

![Create VPC](/images/6/create-sg/001.png?featherlight=false&width=90pc)

2. In the **Create security group** interface under **Basic details**:
   - **Security group name**, enter **```Private server - SG```**
   - **Description**, enter **```Allow inbound HTTP traffic on port 80 inside VPC```**
   - **VPC**, select **web-app-vpc**

![Create VPC](/images/6/create-sg/002.png?featherlight=false&width=90pc)

3. Configure **Inbound rules**:

   - In **Inbound rules**, click **Add rule**.
   
   - Select **Type**: **HTTP** and **Source**: **```10.10.0.0/16```** to allow instances within the Security Group to communicate via HTTP protocol within the VPC.

![Create VPC](/images/6/create-sg/003.png?featherlight=false&width=90pc)

4. Press **Create security group** to complete the creation.

![Create VPC](/images/6/create-sg/004.png?featherlight=false&width=90pc)

#### Create security group for Application Load Balancer

5. In the EC2 interface, select **Security Groups**
   - Choose **Create security group**

![Create VPC](/images/6/create-sg/001.png?featherlight=false&width=90pc)

6. In the **Create security group** interface under **Basic details**:
   - **Security group name**, enter **```ALB-SG```**
   - **Description**, enter **```Allow inbound HTTP traffic on port 80 from the internet```**
   - **VPC**, select **web-app-vpc**

![Create VPC](/images/6/create-sg/006.png?featherlight=false&width=90pc)

7. Configure **Inbound rules**:

   - In **Inbound rules**, click **Add rule**.
   
   - Select **Type**: **HTTP** and **Source**: **Anywhere**. Allow instances within the Security Group to communicate via HTTP protocol with the outside.

![Create VPC](/images/6/create-sg/007.png?featherlight=false&width=90pc)

8. Select **Create security group** to complete the security group creation.

![Create VPC](/images/6/create-sg/008.png?featherlight=false&width=90pc)
