---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 7 
chapter : false
pre : " <b> 7. </b> "
---
### Xoá ứng dụng Elastic Beanstalk
1. Đi đến [Applicaiton](https://ap-southeast-1.console.aws.amazon.com/elasticbeanstalk/home?region=ap-southeast-1#/applications) của **Elastic Beanstalk**.
2. Chọn ứng dụng **FCJ-My-First-App**, nhấn **Action** và chọn **Delete application**.
    ![Delete App](/images/7.cleanup/7.1cleanupapplication.png?width=80pc)
3. Nhập tên ứng dụng ```FCJ-My-First-App``` để xóa.
    ![Delete App](/images/7.cleanup/7.2enterthename.png?width=80pc)

### Xóa Key Pair
1. Đi đến [Key Pair](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#KeyPairs:)
2. Chọn key pair **FCJ-KeyPair**, nhấn **Action** và chọn **Delete**.
3. Nhập ```Delete``` và nhấn **Delete**
    ![Delete Key Pair](/images/7.cleanup/7.3cleanupkeypair.png?width=80pc) 