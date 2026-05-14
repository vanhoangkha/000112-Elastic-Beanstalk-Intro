---
title : "Chuẩn bị"
date: 2024-01-01
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---

### Các bước chuẩn bị
- **Key Pair**: Để SSH đến máy chủ EC2 vừa được cung cấp bởi Elastic Beanstalk
- **IAM service role**: Elastic Beanstalk đảm nhận vai trò dịch vụ để sử dụng các dịch vụ khác của AWS. Service role đã tồn tại sẵn trên tài khoản của bạn và bạn có thể tạo môi trường mới trong bảng điều khiển Elastic Beanstalk hoặc sử dụng Elastic Beanstalk CLI.
- **IAM instance role**: Elastic Beanstalk áp dụng instances profile đến máy chủ trong môi trường của bạn. Nó cho phép chúng thực hiện:
    + Truy xuất các phiên bản ứng dụng từ Amazon Simple Storage Service (Amazon S3).
    + Đăng tải nhật ký lên Amazon S3.
    + Thực hiện các tác vụ khác tùy thuộc vào loại môi trường và nền tảng.

### Nội dung

2.1. [Tạo Key Pair](2.1-createkeypair/).

2.2. [Tạo IAM instance role](2.2-createinstancerole/).
