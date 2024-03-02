---
title: "Create Internet Gateway"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: "<b> 3.3 </b>"
---

#### Create Internet Gateway

1. In the **VPC** interface:

   - Select **Internet Gateways**
   - Choose **Create internet gateway**
  
![Create VPC](/images/2/internet-gateway/001.png?featherlight=false&width=90pc)

2. Perform configuration

   - **Name tag**, enter **`Internet Gateway`**
   - Select **Create internet gateway**

![Create VPC](/images/2/internet-gateway/002.png?featherlight=false&width=90pc)

3. Complete creating **Internet Gateway**

![Create VPC](/images/2/internet-gateway/003.png?featherlight=false&width=90pc)

4. Perform **Attach VPC**

   - Select **Actions**
   - Choose **Attach to VPC**
   - Select **ASG**, VPC ID will be automatically filled in.
   - Choose **Attach internet gateway**

![Create VPC](/images/2/internet-gateway/004.png?featherlight=false&width=90pc)

5. When attached successfully, the **State** of the internet gateway will change to **Attached**

![Create VPC](/images/2/internet-gateway/005.png?featherlight=false&width=90pc)
