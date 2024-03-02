---
title : "Tạo read replica database"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b> 6.7 </b> "
---

#### Tạo Read Replica database

{{% notice info %}}
Giả sử chúng ta đang tạo 1 trang web thương mại điện tử với số lượng read lên database nhiều hơn write. Do đó trong bài lab này chúng ta sẽ chọn Read Replica để tối ưu chi phí
{{% /notice %}}

1. Trong giao diện **RDS**

   - Chọn **Databases**
   - Chọn **webapp-db**

![Create TG](/images/6/create-read-replica/001.png?featherlight=false&width=90pc)

2. Trong giao diện **RDS**
- Chọn **Action**
- Trong Pop up, chọn **Create read replica**

![Create TG](/images/6/create-read-replica/002.png?featherlight=false&width=90pc)

3. Trong giao diện **Create read replica**, 
   - **Db instance identifier**, nhập **db-read-replica**
   - Với  **Connectivity**, chọn **Availability Zone** chọn ***ap-southest-1b* (như thiết kết ban đầu)
  ![Create TG](/images/6/create-read-replica/005.png?featherlight=false&width=90pc)

4. Với phần  **Availability**
   - Chọn  **Single DB instance**
![Create TG](/images/6/create-read-replica/003.png?featherlight=false&width=90pc)

5. Với phần  **Connectivity**
 - Chọn **Availability Zone** chọn **ap-southest-1b** (như thiết kết ban đầu)
![Create TG](/images/6/create-read-replica/004.png?featherlight=false&width=90pc)

6. Nhấn **Create read replica** để AWS bắt đầu tạo read replica
![Create TG](/images/6/create-read-replica/006.png?featherlight=false&width=90pc)

