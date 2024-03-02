---
title: "Create Read Replica Database"
date: "`r Sys.Date()`" 
weight: 7
chapter: false
pre: "<b> 6.7 </b>"
---

#### Create Read Replica database

{{% notice info %}}
Assuming we are creating an e-commerce website with more read operations on the database than writes. Therefore, in this lab, we will choose Read Replica to optimize costs.
{{% /notice %}}

1. In the **RDS** interface:
   - Select **Databases**
   - Choose **webapp-db**

![Create TG](/images/6/create-read-replica/001.png?featherlight=false&width=90pc)

2. In the **RDS** interface:
   - Select **Action**
   - In the Pop-up, choose **Create read replica**

![Create TG](/images/6/create-read-replica/002.png?featherlight=false&width=90pc)

3. In the **Create read replica** interface:
   - For **Db instance identifier**, enter **db-read-replica**
   - For **Connectivity**, choose **Availability Zone** and select ***ap-southest-1b*** (as in the original design)
  ![Create TG](/images/6/create-read-replica/005.png?featherlight=false&width=90pc)

4. For the **Availability** section:
   - Choose **Single DB instance**
![Create TG](/images/6/create-read-replica/003.png?featherlight=false&width=90pc)

5. For the **Connectivity** section:
   - Choose **Availability Zone** and select **ap-southest-1b** (as in the original design)
![Create TG](/images/6/create-read-replica/004.png?featherlight=false&width=90pc)

6. Press **Create read replica** to let AWS start creating the read replica
![Create TG](/images/6/create-read-replica/006.png?featherlight=false&width=90pc)
