---
title : "Tạo RDS Database instance"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

#### Tạo một DB Instance trên AWS

1. Trong giao diện **RDS**

   - Chọn **Databases**
   - Chọn **Create database**

![Create VPC](/images/4/db-instance/001.png?featherlight=false&width=90pc)

2. Trong giao diện **Create database**
   - Đối với **Choose a database creation method**, chọn **Standard create**
   - Đối với **Engine options**, chọn **MySQL**

![Create VPC](/images/4/db-instance/002.png?featherlight=false&width=90pc)

3. Chọn **Templates** cho DB instance này là **Free tier**

![Create VPC](/images/4/db-instance/003.png?featherlight=false&width=90pc)

4. Để nhập mất khẩu chính của bạn ta làm như sau
  - Với **DB instance identifierInfo** ta nhập **```webapp-db```**
  - Mở **Credential Settings**
  - Giữ nguyên **Master username** là **admin**
  - Nhập **Master password** và **Confirm master password**

{{% notice warning %}}
Bạn không thể xem lại mật khẩu người dùng chính. Nếu bạn không ghi lại nó, bạn có thể phải thay đổi nó. Nếu bạn cần thay đổi mật khẩu người dùng chính sau khi DB Instance đã sẵn sàng, bạn có thể sửa đổi DB Instance để làm điều này. Để biết thêm thông tin về việc sửa đổi một DB Instance, xem **Modifying an Amazon RDS DB Instance.**


{{% /notice %}}

![Create VPC](/images/4/db-instance/004.png?featherlight=false&width=90pc)

5. Trong phần **Connectivity** 
   
- Đối với **Compute resource** chọn **Don’t connect to an EC2 compute resource**. Chúng ta sẽ tự set up kết với EC2 trong phần tiếp theo
- Đối với **Virtual private cloud (VPC)** chọn **web-app-vpc**
- Đối với **DB subnet group** chọn **webapp-db-subnet-group**
- Đối với **Public access** chọn **No**

![Create VPC](/images/4/db-instance/005.png?featherlight=false&width=90pc)

6. Đối với **VPC security group (firewall)**

 - Chọn ***Create new*
 - **New VPC security group name**, nhập **webapp-db-security-group**

![Create VPC](/images/4/db-instance/006.png?featherlight=false&width=90pc)

7. Mở **Additional configuration** và nhập **```corp```** cho **Initial database name**

![Create VPC](/images/4/db-instance/007.png?featherlight=false&width=90pc)

8. Chọn **Create** và Db instance bắt đầu khởi tạo 

![Create VPC](/images/4/db-instance/008.png?featherlight=false&width=90pc)

9. Đợi khoảng 5 phút để **status** chuyển sang **available**

![Create VPC](/images/4/db-instance/009.png?featherlight=false&width=90pc)
