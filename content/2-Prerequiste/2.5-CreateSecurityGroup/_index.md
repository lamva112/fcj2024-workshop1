---
title: "Create Security Group"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: "<b> 3.5 </b>"
---

#### Create Security Group

#### Create Security Group for servers located in the Public subnet

1. In the **VPC** interface:

   - Select **Security Group**
   - Choose **Create security group**

![Create SG](/images/2/sg-group/001.png?featherlight=false&width=90pc)

2. Perform configuration for the **Security group**

   - **Security Group name**, enter **`Public server - SG`**
   - **Description**, enter **Allow SSH and Ping for servers in public subnet.**
   - Select **web-app-vpc** VPC 

![Create SG](/images/2/sg-group/002.png?featherlight=false&width=90pc)

3. Perform configuration for **Inbound rules**

   - In **Inbound rules**, click **Add rule**.

   - Select **Type**: **SSH** and **Source**: **My IP**. Allow ping from any IP address.

   - Click **Add rule** to add a new rule.

   - Select **Type**: **HTTP** and **Source**: **Anywhere**. Allow instances within this Security Group to communicate via HTTP protocol with the outside world.

![Create SG](/images/2/sg-group/003.png?featherlight=false&width=90pc)

4. Check **Outbound rules** and choose **Create security group**

![Create SG](/images/2/sg-group/004.png?featherlight=false&width=90pc)

5. Complete creating the security group for servers located in the Public subnet

![Create SG](/images/2/sg-group/005.png?featherlight=false&width=90pc)
