---
title: "Create VPC"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: "<b> 2.1 </b>"
---

#### Create VPC

1. Access the **AWS Management Console**

   - Find **VPC**
   - Select **VPC**
  
![Create VPC](/images/2/000.png?featherlight=false&width=90pc)

2. In the **VPC** interface

   - Select **Your VPC**
   - Choose **Create VPC**
   
![Create VPC](/images/2/001.png?featherlight=false&width=90pc)

3. Proceed with creating the VPC

   - **Resource**, select **VPC only**
   - **Name tag**, enter **`web-app-vpc`**
   - **IPv4 CIDR**, enter **`10.10.0.0/16`**
  
![Create VPC](/images/2/002.png?featherlight=false&width=90pc) 

{{% notice warning %}}
For the **Tenancy** configuration, we will leave it at the default mechanism. If we switch to Dedicated, some **EC2 Instance types** may not be suitable and cannot be created in a VPC with **tenancy mode** set to **Dedicated**.
{{% /notice %}}

4. Select **Create VPC**

![Create VPC](/images/2/003.png?featherlight=false&width=90pc)

5. Complete creating **VPC**

![Create VPC](/images/2/004.png?featherlight=false&width=90pc)

6. View details of the newly created VPC. Check if **Enable DNS resolution and DNS Hostname** is not enabled yet

   - Go to **Edit VPC setting**
   - Select **DNS setting**
   - Choose and **Save**.

![Create VPC](/images/2/005.png?featherlight=false&width=90pc)
