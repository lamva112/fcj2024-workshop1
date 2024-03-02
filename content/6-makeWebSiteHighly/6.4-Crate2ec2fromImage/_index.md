---
title: "Create 2 New EC2 Instances from AMIs"
date: "`r Sys.Date()`" 
weight: 4
chapter: false
pre: "<b>6.4</b> "
---

#### Stop Current EC2 Instance

1. Access the **AWS Management Console**

   - Find **EC2**
   - Select **EC2**

![Create AMIs](/images/3/create-ec2/001.png?featherlight=false&width=90pc)


2. In the EC2 dashboard:
   - Select **Instances**
   - Choose **Webserver**
   - Select **Instance state**
   - Choose **Stop instance**

![Create AMIs](/images/6/create-2-ec2/001.png?featherlight=false&width=90pc)


{{% notice note %}}
Currently, we are not using the Webserver anymore because all the configuration and setup for the web application have been saved in AMIs. We will use AMIs to create Webserver1 and Webserver2 in the private subnet.
{{% /notice %}}

#### Create 2 New EC2 Instances from AMIs

3. In the **Instances** interface, select **Launch instance**

![Create AMIs](/images/6/create-2-ec2/002.png?featherlight=false&width=90pc)

4. In the **Launch an instance** interface, under **Name and tags Info**, enter **```Webserver1```**

![Create AMIs](/images/6/create-2-ec2/003.png?featherlight=false&width=90pc)

5. In the **Amazon Machine Image** section:
   - Select the **My AMIs** tab and choose **Owned by me**
   - Choose **WebserverImage**

![Create AMIs](/images/6/create-2-ec2/004.png?featherlight=false&width=90pc)

6. Configure **Instance type**:
   - Choose **t2.micro (default)**
   - Select the previously created **key pair**

![Create AMIs](/images/6/create-2-ec2/005.png?featherlight=false&width=90pc)

7. Configure **Network**:
   - **VPC**, select **web-app-vpc**
   - **Subnet**, choose **Private Subnet 3**
   - **Auto-assign public IP**, select **disable**
   - **Firewall (Security Group)**, choose **Select existing security group**
   - Select **Private server -SG**
   - Click **Launch instance**

![Create AMIs](/images/6/create-2-ec2/006.png?featherlight=false&width=90pc)

7. Similarly, create **```Webserver2```** with the following **network** configuration:

![Create AMIs](/images/6/create-2-ec2/007.png?featherlight=false&width=90pc)

8. Complete the creation of 2 new EC2 instances

![Create AMIs](/images/6/create-2-ec2/008.png?featherlight=false&width=90pc)
