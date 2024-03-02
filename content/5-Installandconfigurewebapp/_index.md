---
title: "Install and Configure Web Application on EC2 Server"
date: "`r Sys.Date()`" 
weight: 5 
chapter: false
pre: "<b>5.</b> "
---

#### Install and Configure Web Application on EC2 Server

1. Connect to the EC2 instance via SSH using the public IP of the EC2

![Create VPC](/images/5/001.png?featherlight=false&width=90pc)

2. Install Apache web server and PHP packages

```bash
# Switch to superuser mode for administrative privileges
sudo su

# Update the system with the DNF package manager
dnf update -y

# Install Apache HTTP server (httpd), PHP, MariaDB, and related packages
dnf install -y httpd php php-mysqli mariadb105 

# Start the Apache HTTP server
systemctl start httpd

# Enable automatic startup of the Apache HTTP server on system boot
systemctl enable httpd

```
![Create VPC](/images/5/002.png?featherlight=false&width=50pc&height=30pc)

3. Configure database connection settings
   - Create the **inc** directory

```bash
# Change directory to /var/www where web content is often stored
cd /var/www

# Create a new directory named 'inc' to store include files or other resources
mkdir inc

# Change directory to the newly created 'inc' directory
cd inc

```

![Create VPC](/images/5/002.png?featherlight=false&width=50pc&height)

- Create a new file named **dbinfo.inc** (You can use vi or nano, in this example, we'll use vi). This will open a blank file.

```bash
vi dbinfo.inc
```
![Create VPC](/images/5/004.png?featherlight=false&width=50pc&height=30pc)

- Press **i** to enter insert mode

![Create VPC](/images/5/005.png?featherlight=false&width=50pc&height=30pc)

- Add the following content. Replace the values for the parameters based on your environment.

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
Be careful when replacing the values because if incorrect, we won't be able to connect to RDS, and our web application won't function.
{{% /notice %}}

- Press **esc** and type **```:wq```** to save and exit vi
- Type **```cd```** to return to the root directory

4. Install and configure the web application on EC2

   - Create the corp.php application file in the /var/www/html directory

```bash
cd  /var/www/html
```

- Use vi to create the file corp.php (follow the instructions as mentioned above)
- Add the following code to corp.php

{{% notice note %}}
You can copy the corp.php file from this GitHub repo: [https://github.com/lamva112/fcj2024-example/blob/main/corp.php](https://github.com/lamva112/fcj2024-example/blob/main/corp.php)
{{% /notice %}}

![Create VPC](/images/5/007.png?featherlight=false&width=50pc&height=30pc)

5. Open your web browser and access the URL http://PUBLICIP/corp.php

{{% notice note %}}
PUBLICIP is the public IP of the EC2 instance
{{% /notice %}}

6. Complete the web application setup

{{% notice note %}}
You can add data to the database directly from the web application
{{% /notice %}}

![Create VPC](/images/5/008.png?featherlight=false&width=50pc&height=30pc)

#### Verify data in the database.

7. Return to the root using the command **cd**

![Create VPC](/images/5/009.png?featherlight=false&width=50pc&height=30pc)

8. Install the MySQL client on the EC2 instance

```bash
# Install pip (Amazon Linux 2023 does not have pip installed by default)
dnf install -y python3-pip

# Install necessary development packages for MariaDB and Python
dnf install -y mariadb105-devel gcc python3-devel

# Use pip to install the MySQL client library
pip install mysqlclient

```
![Create VPC](/images/5/010.png?featherlight=false&width=50pc&height=30pc)

9. Connect to the database and query data

```bash
#Access MySQL
mysql -h <database endpoint> -u admin –p 

#Access the corp database
MySQL [(none)]> connect corp

#Query data
MySQL [corp]> select * from EMPLOYEES;


```
![Create VPC](/images/5/011.png?featherlight=false&width=50pc&height=30pc)

![Create VPC](/images/5/012.png?featherlight=false&width=50pc&height=30pc)

![Create VPC](/images/5/013.png?featherlight=false&width=50pc&height=30pc)

10. Add data from the website and observe if it reflects changes. Optionally, insert data directly into the database table and see if the website displays the data.

```bash
insert into EMPLOYEES values ('2','Phuc','18','Ho Chi Minh');

```

![Create VPC](/images/5/014.png?featherlight=false&width=50pc&height=30pc)

![Create VPC](/images/5/15.png?featherlight=false&width=50pc&height=30pc)