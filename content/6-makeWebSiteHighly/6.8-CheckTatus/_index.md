---
title: "Check Target Health and Access Web Application"
date: "`r Sys.Date()`" 
weight: 8
chapter: false
pre: "<b> 6.8 </b>"
---

#### Check Target Health

1. In the EC2 dashboard:
   - Select **Target Groups**
   - Choose **ALB-TG**

![Create TG](/images/6/review/001.png?featherlight=false&width=90pc)

2. In **Target group: ALB-TG**:
   - Select **Targets**

{{% notice info %}}
Based on the target group, we can see that both EC2 instances are functioning properly.
{{% /notice %}}
![Create TG](/images/6/review/002.png?featherlight=false&width=90pc)

#### Access the Web Application

3. In the EC2 dashboard:
   - Select **Load Balancers**
   - Choose **MyALB**

![Create TG](/images/6/review/003.png?featherlight=false&width=90pc)

4. For **Load balancer: MyALB**:
   - Copy the **DNS name** and open it in the browser

![Create TG](/images/6/review/004.png?featherlight=false&width=90pc)
![Create TG](/images/6/review/005.png?featherlight=false&width=90pc)

5. Access the web page with the path **DNS name/corp.php**

![Create TG](/images/6/review/006.png?featherlight=false&width=90pc)
