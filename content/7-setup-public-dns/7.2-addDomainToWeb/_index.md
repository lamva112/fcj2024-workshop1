---
title: "Install Public DNS for Web Application"
date: "`r Sys.Date()`" 
weight: 2
chapter: false
pre: "<b> 7.2 </b>"
---

#### Install Public DNS for Web Application

1. In the **Route 53** interface:
   - Select **Hosted zones**
   - Choose the **Hosted zone name** used for the website

![Create TG](/images/7/set-dns/001.png?featherlight=false&width=90pc)

2. In the selected **Hosted zone** interface:
   - Choose **Create record**

![Create TG](/images/7/set-dns/002.png?featherlight=false&width=90pc)

3. In the **Create record** interface:

- Enable **Alias**
- For **Route traffic to**:
  + Choose **Alias to Application and Classic Load Balancer**
  + Select **Asia Pacific (Singapore)**
  + Choose **MyALB**
- Press **Create record**

![Create TG](/images/7/set-dns/003.png?featherlight=false&width=90pc)

4. Complete creating the record

![Create TG](/images/7/set-dns/004.png?featherlight=false&width=90pc)

5. Open your browser and access your web application using **`http://YOUR_DOMAIN_NAME/corp.php`**

![Create TG](/images/7/set-dns/005.png?featherlight=false&width=90pc)
