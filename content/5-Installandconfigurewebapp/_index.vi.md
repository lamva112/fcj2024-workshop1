---
title : "Cài đặt và cấu hình web application trên máy chủ EC2"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

#### Cài đặt và cấu hình web application trên máy chủ EC2

1. Kết nối vào EC2 instance qua SSH bằng cách sử dụng IP public của EC2

![Create VPC](/images/5/001.png?featherlight=false&width=90pc)


2. Cài đặt  Apache web server and PHP packages

```bash
# Chuyển sang chế độ superuser
sudo su

# Cập nhật hệ thống bằng trình quản lý gói DNF
dnf update -y

# Cài đặt máy chủ Apache HTTP (httpd), PHP, MariaDB và các gói cần thiết khác
dnf install -y httpd php php-mysqli mariadb105 

# Khởi động máy chủ Apache HTTP
systemctl start httpd

# Cho phép máy chủ Apache HTTP khởi động tự động khi khởi động hệ thống
systemctl enable httpd

```
![Create VPC](/images/5/002.png?featherlight=false&width=50pc&height=30pc)


3. Cấu hình các thiết lập kết nối cơ sở dữ liệu
 -  Tạo thư mục **inc**

```bash
# Di chuyển đến thư mục /var/www
cd /var/www

# Tạo thư mục mới có tên là inc
mkdir inc

# Di chuyển đến thư mục inc vừa tạo
cd inc

```

![Create VPC](/images/5/002.png?featherlight=false&width=50pc&height=30pc)

- Tạo một file mới có tên là **dbinfo.inc** (Bạn có thể sử dụng vi hoặc nano trong ví dụ này sẽ dùng vi). Màn hìh sẽ hiện lên 1 file trống

```bash
vi dbinfo.inc
```
![Create VPC](/images/5/004.png?featherlight=false&width=50pc&height=30pc)

- nhấn **i** để bật chế độ insert

![Create VPC](/images/5/005.png?featherlight=false&width=50pc&height=30pc)

- Thêm nội dung sau đây. Thay thế các giá trị cho các tham số dựa trên môi trường của bạn.

```php

<?php
define('DB_SERVER', 'db_instance_endpoint');
define('DB_USERNAME', 'admin');
define('DB_PASSWORD', 'master password');
define('DB_DATABASE', 'corp');
?>

```

![Create VPC](/images/5/006.png?featherlight=false&width=50pc&height=30pc)


{{% notice warning %}}
Hãy thay thế các giá trị cẩn thận vì nếu sai chúng ta khổng thể kết nối với RDS và ứng dụng web của chúng ta sẽ không hoạt động
{{% /notice %}}

- Nhấn **esc** và nhập **```:wq```** để lưu và thoát khỏi **vi**
- nhập  **```cd```** để trở về root

4. Cài đặt và cấu hình ứng dụng web trên EC2
   
- Tạo tập tin ứng dụng corp.php trong thư mục /var/www/html
  
```bash
cd  /var/www/html
```
- dùng vi để tạo file corp.php (cách tạo như hướng dẫn phía trên)
- Thêm đoạn code bên dưới vào corp.php 
{{% notice note %}}
Bạn có thể copy file corp.php từ github repo này : https://github.com/lamva112/fcj2024-example/blob/main/corp.php
{{% /notice %}}

![Create VPC](/images/5/007.png?featherlight=false&width=50pc&height=30pc)

5. Mở trình duyệt của bạn và truy cập vào địa chỉ URL http://PUBLICIP/corp.php

{{% notice note %}}
PUBLICIP là public IP của EC2
{{% /notice %}}

6. Hoàn thành tạo ứng dụng web 

{{% notice note %}}
Bạn có thể thêm dữ liệu vào database trực tiếp từ ứng dụng web
{{% /notice %}}

![Create VPC](/images/5/008.png?featherlight=false&width=50pc&height=30pc)

#### Xác minh dữ liệu trong cơ sở dữ liệu.

7. Trở lại root bằng lệnh **cd**

![Create VPC](/images/5/009.png?featherlight=false&width=50pc&height=30pc)

8. Cài đặt mqsql client trong the ec2 instance


```bash
# Cài đặt pip (Amazon Linux 2023 không có pip mặc định). 
dnf install -y pip
# Cài đặt các phụ thuộc.
dnf install -y mariadb105-devel gcc python3-devel
# Cài đặt mysqlclient 
pip install mysqlclient

```
![Create VPC](/images/5/010.png?featherlight=false&width=50pc&height=30pc)

9. Kết nối đến cơ sở dữ liệu và truy vấn dữ liệu

```bash
#Truy cập vào MySQL
mysql -h <database endpoint> -u admin –p 

#Truy cập vào corp database
MySQL [(none)]> connect corp

#Truy vấn dữ liệu
MySQL [corp]> select * from EMPLOYEES;

```
![Create VPC](/images/5/011.png?featherlight=false&width=50pc&height=30pc)

![Create VPC](/images/5/012.png?featherlight=false&width=50pc&height=30pc)

![Create VPC](/images/5/013.png?featherlight=false&width=50pc&height=30pc)

10. Thêm nhiều dữ liệu từ trang web và xem xét xem có phản ánh thay đổi không. Tùy chọn chèn dữ liệu vào bảng cơ sở dữ liệu trực tiếp và xem xét xem trang web có hiển thị dữ liệu không.

```bash
insert into EMPLOYEES values ('2','Phuc','18','Ho Chi Minh');

```

![Create VPC](/images/5/014.png?featherlight=false&width=50pc&height=30pc)

![Create VPC](/images/5/15.png?featherlight=false&width=50pc&height=30pc)
