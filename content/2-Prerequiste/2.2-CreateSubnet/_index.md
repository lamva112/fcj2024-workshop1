---
title: "Create Subnet"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: "<b> 2.2 </b>"
---

## Create Subnet

1. In the **VPC** Interface:
   - Select **Subnets**
   - Select **Create subnet**
   
   ![Create VPC](/images/2/006.png?featherlight=false&width=90pc)

2. In the **Create subnet** Interface:
   - Select **ASG** VPC
   
   ![Create VPC](/images/2/007.png?featherlight=false&width=90pc)

3. Perform **subnet settings**

   - **Subnet name**, enter **`Public Subnet 1`**
   - Choose AZ **ap-southeast-1a**
   - **IPv4 CIDR block**, enter **`10.10.0.0/24`** as described in the architecture 
   - Select **Create subnet**
  
![Create VPC](/images/2/subnet/002.png?featherlight=false&width=80pc)

4. Complete creating **subnet**

![Create VPC](/images/2/subnet/004.png?featherlight=false&width=80pc)

5. Perform the following steps to create additional subnets:

   - **Public subnet 2** with **CIDR** of **10.10.1.0/24** in **Availability Zone ap-southeast-1b**.

![Create VPC](/images/2/subnet/005.png?featherlight=false&width=80pc)

   - **Private subnet 1** with **CIDR** of **10.10.11.0/24** in **Availability Zone ap-southeast-1a**.

![Create VPC](/images/2/subnet/006.png?featherlight=false&width=80pc)

   - **Private subnet 2** with **CIDR** of **10.10.12.0/24** in **Availability Zone ap-southeast-1b**.

![Create VPC](/images/2/subnet/007.png?featherlight=false&width=80pc)

{{% notice tip %}}
You may notice there are 2 columns, **Availability Zone** and **Availability Zone ID**. To avoid uneven EC2 resource utilization (we tend to use AZ a for primary and AZ b for standby, for example), AWS randomly assigns **Availability Zone to Availability Zone ID**. We can understand that Availability Zone is a form of an alias, while the Availability Zone ID is the identifier. For example, in the image above, Availability Zone ap-southeast-1a is assigned Availability Zone ID apse1-az2. In another AWS account, Availability Zone ap-southeast-1a may have Availability Zone ID apse1-az1.
{{% /notice %}}

![Create VPC](/images/2/subnet/008.png?featherlight=false&width=80pc)

#### Allow automatic assignment of public IP addresses to 2 public subnets.

{{% notice tip %}}
Another noteworthy point is that the subnets are essentially the same, through route table configuration and public IP address assignment, which we have just divided into Public and Private Subnets.
{{% /notice %}}

6. In the **VPC** interface:

   - Select **Subnets**
   - Choose **Public Subnet 1**
   - Select **Actions**
   - Choose **Edit subnet settings**

![Create VPC](/images/2/subnet/009.png?featherlight=false&width=80pc)

8. Repeat the same process for **Public subnet 2**.

![Create VPC](/images/2/subnet/010.png?featherlight=false&width=80pc)

![Create VPC](/images/2/subnet/011.png?featherlight=false&width=80pc)
