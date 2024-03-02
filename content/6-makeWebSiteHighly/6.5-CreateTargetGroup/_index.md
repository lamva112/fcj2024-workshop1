---
title : "Create Target Groups"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 6.5 </b> "
---

#### Create Target Groups

In Amazon Web Services (AWS), a target group is a group of destination servers to which requests from a service are routed. Target groups are commonly used in services such as Elastic Load Balancing (ELB) or AWS Auto Scaling to route requests to appropriate destination servers.

In this lab, we will create a target group for 2 EC2 instances to route requests from a load balancer to these 2 EC2 instances. This helps distribute load and increase the availability and reliability of the application by sharing the workload between servers.

1. In the EC2 interface:
   - Select **Target Groups**
   - Click **Create target group**

![Create TG](/images/6/create-target-group/001.png?featherlight=false&width=90pc)

2. In the **Step 1** interface (**Specify group details**):
   - For **Basic configuration**, choose **target type** as **instance**

![Create TG](/images/6/create-target-group/002.png?featherlight=false&width=90pc)

3. Continue configuring the target group:
   - For **Target group name**, enter **```ALB-TG```**
   - For **Protocol : Port**, select **HTTP**
   - Choose **IP address type** as **IPv4**
   - **VPC**, select **web-app-vpc**

![Create TG](/images/6/create-target-group/003.png?featherlight=false&width=90pc)

4. Create Health checks:
   - **Health check protocol**, choose **HTTP**
   - **Health check path**, enter **```corp.php```**

![Create TG](/images/6/create-target-group/004.png?featherlight=false&width=90pc)

In AWS, health checks in a target group are used to monitor the health status of instances or targets managed by the target group. The goal of health checks is to ensure that only healthy and ready-to-serve instances or targets receive traffic from load balancers or other services. Here are some key purposes of using health checks in a target group:

- **Ensure Load Balancer routes traffic only to functioning instances**: Health checks ensure that only active and healthy EC2 instances or targets receive traffic from the Load Balancer. This helps prevent routing traffic to non-functioning or faulty instances.
  
- **Increase availability and reliability of the application**: By accepting only active and healthy instances into the target group, you ensure that your application is always available to serve requests from users without issues.

- **Automatically detect and handle failures**: If an EC2 instance or target fails to pass the health check, the load balancer or other services can automatically remove it from the traffic routing process. This helps automatically detect and handle failures without manual intervention.

5. Click **Next** to proceed to **step 2**.

6. In **Step 2** (**Register targets**):
   - Select the 2 instances **Webserver1** and **Webserver2**.
   - Choose **Include as pending below**.

![Create TG](/images/6/create-target-group/005.png?featherlight=false&width=90pc)

7. Verify that the 2 instances have been added as targets and click **Create target group**.

![Create TG](/images/6/create-target-group/006.png?featherlight=false&width=90pc)

8. Complete the creation of the target group.

![Create TG](/images/6/create-target-group/007.png?featherlight=false&width=90pc)
