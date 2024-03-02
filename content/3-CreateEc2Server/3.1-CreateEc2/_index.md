---
title: "Create EC2 Instance"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: "<b> 3.1 </b>"
---

#### Create EC2 Instance in Public Subnet

1. Access the **AWS Management Console**

   - Find **EC2**
   - Select **EC2**

![Create EC2](/images/3/create-ec2/001.png?featherlight=false&width=90pc)

2. In the **EC2** interface:

   - Select **Instances**
   - Choose **Launch instances**

![Create EC2](/images/3/create-ec2/002.png?featherlight=false&width=90pc)

3. **Name and tags** of the instance, enter **`Webserver`**

![Create EC2](/images/3/create-ec2/003.png?featherlight=false&width=90pc)

4. Select **AMI**

   - Choose **Quick Start**
   - Select **Amazon Linux (default)**
   - Choose the AMI **Amazon Linux 2023 AMI – Free tier eligible**

![Create EC2](/images/3/create-ec2/004.png?featherlight=false&width=90pc)

5. Choose **Instance type**
   - Select **t2.micro (default)**
   - Choose **Create key pair**

![Create EC2](/images/3/create-ec2/005.png?featherlight=false&width=90pc)

6. In the **Create key pair** interface:

   - **Key pair name**, enter **`aws-keypair`** (optional name, you can choose any).
   - **Key pair type**, select **RSA**
   - **Private key file format**, select **.pem**

![Create EC2](/images/3/create-ec2/006.png?featherlight=false&width=90pc)

7. Configure **Network**

    - **VPC**, select **ASG**
    - **Subnet**, select **Public Subnet 1**
    - **Auto-assign public IP**, select **Enable**
    - **Firewall (Security Group)**, select **Select existing security group**
    - Choose **Public server -SG**
    - Click **Launch instance**

![Create EC2](/images/3/create-ec2/007.png?featherlight=false&width=90pc)

8. Complete the instance creation

![Create EC2](/images/3/create-ec2/008.png?featherlight=false&width=90pc)

9. Wait for about 5 minutes until the **Status check** changes to **2/2 checks passed**

![Create EC2](/images/3/create-ec2/009.png?featherlight=false&width=90pc)
