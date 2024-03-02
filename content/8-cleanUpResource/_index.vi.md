---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 8. </b> "
---
#### Dọn dẹp tài nguyên

Chúng ta sẽ tiến hành xóa các tài nguyên theo thứ tự sau

### Terminate các EC2 Instance.
1. Terminate EC2 instance.
    - Truy cập Amazon EC2 console 
    - Trên thanh điều hướng bên trái, chọn Intances
    - Chọn tất cả EC2 Instance liên quan tới bài lab.
    - Chọn **Instance state**
    - Chọn **Terminate instance**

![Create TG](/images/7/clean-up/001.png?featherlight=false&width=90pc)

2. Xác nhận terminate.
   
![Create TG](/images/7/clean-up/002.png?featherlight=false&width=90pc)

#### Xóa Load balancer

3. Xoá Load balancer
    - Truy cập Amazon EC2 console 
    - Trên thanh điều hướng bên trái, chọn Load balancer
    - Chọn Load balancer liên quan tới bài lab.
    - Chọn **Action**
    - Chọn **Delete load balancer**

![Create TG](/images/7/clean-up/003.png?featherlight=false&width=90pc)

4. Xác nhận xoá

![Create TG](/images/7/clean-up/004.png?featherlight=false&width=90pc)

#### Xóa Target Groups

5. Xóa Target Groups
    - Truy cập Amazon EC2 console 
    - Trên thanh điều hướng bên trái, chọn Target Groups
    - Chọn Target Groups liên quan tới bài lab.
    - Chọn **Action**
    - Chọn **Delete**

![Create TG](/images/7/clean-up/005.png?featherlight=false&width=90pc)

6. Xác nhận xoá Target Groups

![Create TG](/images/7/clean-up/006.png?featherlight=false&width=90pc)

#### Xóa Database

7. Xóa read replica database
   - Truy cập RDS console
   - Trên thanh điều hướng bên trái, chọn Database
   - Chọn read replica database
   - Chọn **Delete**

![Create TG](/images/7/clean-up/007.png?featherlight=false&width=90pc)

8. Xác nhận xoá replica database 

![Create TG](/images/7/clean-up/008.png?featherlight=false&width=90pc)

9. Xoá database
    - Chọn database cần xoá
    - Chọn **Delete**

![Create TG](/images/7/clean-up/009.png?featherlight=false&width=90pc)

10. Xác nhận xoá database

![Create TG](/images/7/clean-up/011.png?featherlight=false&width=90pc)

#### Xoá VPC


11. Xoá VPC
    
    - Truy cập VPC console 
    - Trên thanh điều hướng bên trái, chọn Load balancer
    - Chọn VPC liên quan tới bài lab.
    - Chọn **Action**
    - Chọn **Delete**

![Create TG](/images/7/clean-up/010.png?featherlight=false&width=90pc)

12. Xác nhận xoá VPC
    
![Create TG](/images/7/clean-up/012.png?featherlight=false&width=90pc)
