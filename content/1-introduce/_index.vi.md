---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

#### Giới thiệu kiến trúc 2-tier 

Kiến trúc 2-tier giống như ứng dụng client-server. Giao tiếp trực tiếp diễn ra giữa máy khách và máy chủ. Không có trung gian nào giữa máy khách và máy chủ. Do sự liên kết chặt chẽ, một ứng dụng hai tầng sẽ chạy nhanh hơn.

Kiến trúc hai tầng được chia thành hai phần:

1. Client Application (Client Tier)

2. Cơ sở dữ liệu (Data Tier)

![Architect](/images/1-Introduce/architecture2.png?featherlight=false&width=30pc)

Trên phía ứng dụng máy khách, mã được viết để lưu trữ dữ liệu trong cơ sở dữ liệu SQL Server. Máy khách gửi yêu cầu đến máy chủ và máy chủ xử lý yêu cầu đó và gửi nó trở lại với dữ liệu. Vấn đề chính của kiến trúc hai tầng là máy chủ không thể đáp ứng đồng thời nhiều yêu cầu, dẫn đến vấn đề về tính toàn vẹn dữ liệu.

Nó cũng được gọi là công nghệ máy chủ-máy khách.

Ưu điểm:
- Dễ bảo trì và việc sửa đổi dễ dàng hơn một chút
- Giao tiếp nhanh hơn

Nhược điểm:
- Trong kiến trúc hai tầng, hiệu suất ứng dụng sẽ bị suy giảm ngay khi số lượng người dùng tăng lên.
- Không hiệu quả về chi phí


Dưới đây là một giải thích đơn giản về việc triển khai ứng dụng web theo kiến trúc hai tầng trên cơ sở hạ tầng AWS.

![Architect](/images/1-Introduce/full-2-tier-with-53.svg?featherlight=false&width=40pc)

{{% notice info %}}
Trong phạm vi bài lab này chúng ta chỉ sử dụng các dịch vụ VPC, EC2, ALB và RDS để hiểu về 2 tier. Trong thực tế cần thêm các dịch vụ như S3, Route53,Cloudfront. 
{{% /notice %}}

Ở đây bạn có thể thấy rằng một VPC tùy chỉnh được tạo ra để ứng dụng Web của bạn sẽ được bảo mật, chúng ta đã phân tán tất cả các tài nguyên qua hai khu vực khả dụng (AZ) để cung cấp tính dự phòng cho việc bảo trì hệ thống theo lịch trình. Do đó, mỗi khu vực khả dụng đều đang lưu trữ ít nhất một instance cho mỗi dịch vụ, trừ các dịch vụ được thiết kế để dự phòng (ví dụ: Bộ cân bằng Tải,v.v.).

Tầng Web bao gồm hai máy chủ web (một trong mỗi khu vực khả dụng) được triển khai trên các thể hiện Elastic Compute Cloud (EC2). Chúng ta cân bằng lưu lượng bên ngoài đến các máy chủ bằng cách sử dụng Bộ cân bằng Tải  (ALB). 

Tầng Cơ sở dữ liệu, Dịch vụ Cơ sở dữ liệu Quan hệ (RDS), cung cấp môi trường quan hệ (MySQL, MS SQL hoặc Oracle) cho giải pháp này. Trong thiết kế này, chúng ta cũng có thể cung cấp các bản sao đọc để giảm nhu cầu trên cơ sở dữ liệu chính. Để tối ưu hóa chi phí, với các bản sao đọc bổ sung được tạo ra trong mỗi khu vực khả dụng như được yêu cầu.