---
title : "Tạo môi trường phát triển trong Elastic Beanstalk"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

1. Đi đến [AWS Management Console](https://aws.amazon.com/vi/console/)
- Tìm **EC2**
- Chọn **EC2**
![Find EC2](/images/2.preparation/2.1createkeypair/2.1.1selectec2.png?width90pc)
2. Trong trang giao diện của **EC2**, chọn **Key Pairs**.
3. Nhấn vào **Create Key Pair**.
![Create Key Pair](/images/2.preparation/2.1createkeypair/2.1.2createkeypair1.png?width90pc)
4. Nhập tên của key pair ```FCJ-KeyPair```.
5. Tại mục **Key pair type**, chọn **RSA**.
6. Tại mục **Private key file format**, chọn **.pem**.
7. Nhấn  **Create key pair** để tạo.
![Create Key Pair](/images/2.preparation/2.1createkeypair/2.1.3createkeypair2.png?width90pc)
{{% notice warning %}} 
Hãy đảm bảo rằng tệp key pair vừa tạo đã được tải xuống máy tính của bạn
{{% /notice  %}}
