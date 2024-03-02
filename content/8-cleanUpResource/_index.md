---
title: "Cleanup Resources"
date: "`r Sys.Date()`" 
weight: 8
chapter: false
pre: "<b> 8. </b>"
---
#### Cleanup Resources

We will proceed to delete resources in the following order.

### Terminate EC2 Instances.
1. Terminate EC2 instance.
    - Access the Amazon EC2 console 
    - On the left navigation pane, choose Instances
    - Select all EC2 Instances related to the lab.
    - Choose **Instance state**
    - Choose **Terminate instance**

![Create TG](/images/7/clean-up/001.png?featherlight=false&width=90pc)

2. Confirm terminate.

![Create TG](/images/7/clean-up/002.png?featherlight=false&width=90pc)

#### Delete Load Balancer

3. Delete Load balancer
    - Access the Amazon EC2 console 
    - On the left navigation pane, choose Load balancer
    - Select the Load balancer related to the lab.
    - Choose **Action**
    - Choose **Delete load balancer**

![Create TG](/images/7/clean-up/003.png?featherlight=false&width=90pc)

4. Confirm deletion

![Create TG](/images/7/clean-up/004.png?featherlight=false&width=90pc)

#### Delete Target Groups

5. Delete Target Groups
    - Access the Amazon EC2 console 
    - On the left navigation pane, choose Target Groups
    - Select the Target Groups related to the lab.
    - Choose **Action**
    - Choose **Delete**

![Create TG](/images/7/clean-up/005.png?featherlight=false&width=90pc)

6. Confirm deletion of Target Groups

![Create TG](/images/7/clean-up/006.png?featherlight=false&width=90pc)

#### Delete Database

7. Delete read replica database
   - Access the RDS console
   - On the left navigation pane, choose Database
   - Select the read replica database
   - Choose **Delete**

![Create TG](/images/7/clean-up/007.png?featherlight=false&width=90pc)

8. Confirm deletion of replica database 

![Create TG](/images/7/clean-up/008.png?featherlight=false&width=90pc)

9. Delete database
    - Select the database to be deleted
    - Choose **Delete**

![Create TG](/images/7/clean-up/009.png?featherlight=false&width=90pc)

10. Confirm deletion of the database

![Create TG](/images/7/clean-up/011.png?featherlight=false&width=90pc)

#### Delete VPC

11. Delete VPC
    
    - Access the VPC console 
    - On the left navigation pane, choose Load balancer
    - Select the VPC related to the lab.
    - Choose **Action**
    - Choose **Delete**

![Create TG](/images/7/clean-up/010.png?featherlight=false&width=90pc)

12. Confirm deletion of VPC
    
![Create TG](/images/7/clean-up/012.png?featherlight=false&width=90pc)
