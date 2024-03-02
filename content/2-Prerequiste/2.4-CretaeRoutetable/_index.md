---
title: "Create Route Table"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: "<b> 2.4 </b>"
---

#### Create Route Table for routing out to the internet via Internet Gateway.

1. In the **VPC** interface:

   - Select **Route Tables**
   - Choose **Create route table**

![Create VPC](/images/2/route-table/002.png?featherlight=false&width=90pc)

2. Perform configuration for the **Route table**

   - **Name**, enter **`Route table-Public`**
   - **VPC**, select **ASG** VPC. The VPC ID will be automatically filled in.
   - Choose **Create route table**

![Create VPC](/images/2/route-table/001.png?featherlight=false&width=90pc)

3. Complete creating the **Route table**

![Create VPC](/images/2/route-table/003.png?featherlight=false&width=90pc)

4. Perform **Edit route**

   - Select **Actions**
   - Choose **Edit routes**

![Create VPC](/images/2/route-table/004.png?featherlight=false&width=90pc)

5. In the **Edit routes** interface:

   - Choose **Add route**
   - Enter **Destination CIDR** : **`0.0.0.0/0`** representing the Internet.
   - In the **Target** section, select **Internet Gateway**, then choose the **Internet Gateway** we created. The **Internet Gateway ID** will be automatically filled in.
   - Choose **Save changes**
  
![Create VPC](/images/2/route-table/005.png?featherlight=false&width=90pc)

6. Complete and verify the **Routes**

![Create VPC](/images/2/route-table/006.png?featherlight=false&width=90pc)

7. Ensure **Route table - Public** is selected.

   - Select **subnet associations**
   - Choose **Edit subnet associations**

![Create VPC](/images/2/route-table/007.png?featherlight=false&width=90pc)

8. In the **Edit subnet associations** step:

   - Expand the **Subnet ID** column by dragging the separator to the right.
   - Select the correct **2 public subnets** we created.

![Create VPC](/images/2/route-table/008.png?featherlight=false&width=90pc)

9. Select **Save associations**

![Create VPC](/images/2/route-table/009.png?featherlight=false&width=90pc)

10. Complete and verify the **Subnet associations**

![Create VPC](/images/2/route-table/010.png?featherlight=false&width=90pc)

#### Create Route table - Private and associate it with the private subnets.

11. In the **Route Tables** interface:

   - Choose **Create route table**

![Create VPC](/images/2/route-table/011.png?featherlight=false&width=90pc)

12. In the **Create route table** interface:

   - **Name**, enter **`Route table - Private`**
   - **VPC**, select **web-app-vpc** VPC
   - Choose **Create route table**

![Create VPC](/images/2/route-table/012.png?featherlight=false&width=90pc)

13. Complete creating the **Route table - Private**
    
![Create VPC](/images/2/route-table/013.png?featherlight=false&width=90pc)

14. In the **Route table - Private** interface:

    - Select **Subnet Associations**
    - Choose **Edit subnet associations**

![Create VPC](/images/2/route-table/014.png?featherlight=false&width=90pc)

15. In the **Edit subnet associations** interface:

     - Select 2 private subnets
     - Choose **Save associations**

![Create VPC](/images/2/route-table/015.png?featherlight=false&width=90pc)
