---
title : "Deploy 2-tier web application"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---

# Bắt đầu với 2 Tier aplication

#### Tổng quan

2-tier web application là một kiến trúc phần mềm phổ biến trong đó các thành phần của ứng dụng được chia thành hai tầng chính: tầng giao diện người dùng và tầng dịch vụ hoặc logic xử lý. Trong mô hình này, tầng giao diện người dùng chịu trách nhiệm hiển thị dữ liệu và tương tác với người dùng, trong khi tầng dịch vụ hoặc logic xử lý thực hiện các nhiệm vụ xử lý logic, truy xuất dữ liệu và tương tác với cơ sở dữ liệu hoặc các hệ thống khác.

Khi triển khai một ứng dụng 2-tier trên AWS (Amazon Web Services), có một số dịch vụ và tài nguyên quan trọng mà bạn có thể sử dụng:

1. **EC2 (Elastic Compute Cloud)**: EC2 cung cấp các máy ảo có thể co dãn mà bạn có thể sử dụng để triển khai các thành phần của ứng dụng của mình, bao gồm cả tầng giao diện người dùng và tầng dịch vụ.

2. **RDS (Relational Database Service)**: RDS cung cấp các dịch vụ cơ sở dữ liệu quan hệ như MySQL, PostgreSQL, SQL Server, và Oracle. Bạn có thể sử dụng RDS để lưu trữ dữ liệu cho ứng dụng của mình.

3. **ELB (Elastic Load Balancing)**: ELB cho phép phân phối lưu lượng truy cập giữa các máy chủ EC2 của bạn, giúp cải thiện khả năng mở rộng và độ tin cậy của ứng dụng.

4. **VPC (Virtual Private Cloud)**: VPC cho phép bạn tạo ra một môi trường mạng ảo trong AWS để triển khai ứng dụng của mình, cung cấp bảo mật và kiểm soát truy cập.


Trong bài lab này chúng ta sẽ cùng tìm hiểu tìm 2 tier web aplication và cách thực thi nó trên môi trường AWS


#### Nội dung
1. [Giới thiệu 2-tier](1-introduce/)
2. [Các bước chuẩn bị](2-Prerequiste/)
3. [Tạo máy chủ EC2](3-CreateEc2Server/)
4. [Tạo RDS database](4-CreateRDS/)
5. [Cài đặt và cấu hình web application trên máy chủ EC2](5-Installandconfigurewebapp/)
6. [Tạo 2-tier web application có tính khả dụng cao](6-makeWebSiteHighly/)
7. [Cấu hình Public DNS với Route53](7-setup-public-dns/)
8. [Dọn dẹp tài nguyên](8-cleanUpResource/)