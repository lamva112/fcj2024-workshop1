---
title: "Create Application Load Balancer"
date: "`r Sys.Date()`" 
weight: 6
chapter: false
pre: "<b> 6.6 </b>"
---

#### Create Application Load Balancer

1. In the EC2 dashboard:
   - Select **Load Balancers**
   - Choose **Create load balancers**

![Create TG](/images/6/create-alb/001.png?featherlight=false&width=90pc)

2. In the **Compare and select load balancer type** interface:
   - Select **Create** under **Application Load Balancer**

![Create TG](/images/6/create-alb/002.png?featherlight=false&width=90pc)

3. In the **Create Application Load Balancer** interface:
   - For **Load balancer name**, enter **`MyALB`**
   - For **Scheme**, choose **Internet-facing**
   - For **IP address typeInfo**, select **IPv4**

![Create TG](/images/6/create-alb/004.png?featherlight=false&width=90pc)

4. Continue configuring **Network mapping**:
   - For VPC, select **Web-app-vpc**
   - For **ap-southeast-1a (apse1-az2)**, choose **Public Subnet 1**
   - For **ap-southeast-1b (apse1-az1)**, choose **Public Subnet 2**

![Create TG](/images/6/create-alb/005.png?featherlight=false&width=90pc)

5. In the **Security groups** section:
   - Select **ALB-SG**

![Create TG](/images/6/create-alb/006.png?featherlight=false&width=90pc)

5. In the **Listeners and routing** section:
   - For **Default actionInfo**, select the target group **ALB-TG**

![Create TG](/images/6/create-alb/007.png?featherlight=false&width=90pc)

6. Press **Create** to complete creating the Application Load Balancer

![Create TG](/images/6/create-alb/008.png?featherlight=false&width=90pc)
