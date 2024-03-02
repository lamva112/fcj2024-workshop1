---
title: "Create AMIs"
date: "`r Sys.Date()`" 
weight: 1 
chapter: false
pre: "<b>6.1</b> "
---

#### Create AMIs

AMI allows us to create a backup of EC2 virtual machines, including the operating system, applications, and data. Therefore, we need to deploy AMIs with configurations similar to the EC2 instances we created earlier.

1. Access the **AWS Management Console**

   - Find **EC2**
   - Select **EC2**

![Create AMIs](/images/3/create-ec2/001.png?featherlight=false&width=90pc)


2. In the EC2 dashboard
   - Select **Instances**
   - Choose **Webserver**
   - Select **Action**

![Create EC2](/images/6/001.png?featherlight=false&width=90pc)

3. In the Action Popup:
   - Select **Image and template**
   - Choose **Create image**

![Create EC2](/images/6/002.png?featherlight=false&width=90pc)

4. In the **Create Image** interface:
   
   - **Image name**, enter **```WebserverImage```**
   - Press **Create**

![Create EC2](/images/6/003.png?featherlight=false&width=90pc)

5. Image creation successful

![Create EC2](/images/6/004.png?featherlight=false&width=90pc)
