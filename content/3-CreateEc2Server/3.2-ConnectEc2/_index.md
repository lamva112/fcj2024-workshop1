---
title : "Check Connection"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 3.2 </b> "
---

#### Check Connection
{{% notice note %}}
There are various ways to connect to EC2 instances, you can refer to [connecting to EC2 on Windows using PuTTY](https://000004.awsstudygroup.com/vi/4-launchlinuxinstance/4.2-connectlinuxinstance/). In this lab, we use the terminal to connect to EC2.
{{% /notice %}}

1. Open Terminal and run the following command with the correct path to the .pem key file:

![Connect EC2](/images/3/connect-ec2/001.png?featherlight=false&width=90pc)

2. Access the **EC2** page:

   - Select **Instances**
   - Choose **Webserver**
   - Click **Connect**

![Connect EC2](/images/3/connect-ec2/002.png?featherlight=false&width=90pc)

3. In the **Connect to instance** interface:

   - Select **SSH Client**
   - Copy the **Example** path

![Connect EC2](/images/3/connect-ec2/003.png?featherlight=false&width=90pc)

4. In the previously opened terminal:
   - Paste the **Example** path
   - Type **yes**

![Connect EC2](/images/3/connect-ec2/004.png?featherlight=false&width=90pc)

5. Connection successful.

![Connect EC2](/images/3/connect-ec2/005.png?featherlight=false&width=90pc)

6. To check the internet connection of the EC2 Public, execute the command:

```
ping amazon.com -c5
```

![Connect EC2](/images/3/connect-ec2/006.png?featherlight=false&width=90pc)
