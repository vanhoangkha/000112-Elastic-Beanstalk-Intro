---
title : "Tạo IAM role cho EB service"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

1.Đi đến [AWS Management Console](https://aws.amazon.com/vi/console/).
- Tìm **IAM**.
- Chọn **IAM**.
    ![Search IAM](/images/2.preparation/2.2createservicerole/2.2.1searchiam.png?width90pc)

2. Trong giao diện **IAM**, chọn **Roles**.

3. Trong giao diện **Role**, tìm kiếm role tên là ```aws-elasticbeanstalk-ec2-role```. 

4. Nếu role đã tồn tại, bạn có thể bỏ qua bước này và đi đến [3. Create Develop environment in Elastic Beanstalk](../../3-createdevenv/).
    
{{% notice warning %}} 
Kiểm tra và đảm bảo rằng role đã được tạo với 3 policies ```AWSElasticBeanstalkWebTier```, ```AWSElasticBeanstalkWorkerTier``` and ```AWSElasticBeanstalkMulticontainerDocker```.
{{% /notice  %}}

5. Nếu role chưa tồn tại, bạn có thể tạo role mới bằng việc nhấn **Create role**.
    ![Create Role 1](/images/2.preparation/2.2createservicerole/2.2.3createrole1.png?width90pc)

6. Tại giao diện **Trusted entity type**:
    - Chọn **AWS service**.
    - Tại **Use case**, tìm kiếm và chọn **EC2** là service.
    - Chọn **EC2** là use case.
    - Sau đó nhấn **Next**.
    ![Create Role 2](/images/2.preparation/2.2createservicerole/2.2.4createrole2.png?width90pc)

7. Sau đó, tìm kiếm và thêm các policies ```AWSElasticBeanstalkWebTier```, ```AWSElasticBeanstalkWorkerTier``` và ```AWSElasticBeanstalkMulticontainerDocker```.
    ![Create Role 3](/images/2.preparation/2.2createservicerole/2.2.5createrole3.png?width90pc)

8. Nhập tên của role ```aws-elasticbeanstalk-ec2-role```.
    ![Create Role 4](/images/2.preparation/2.2createservicerole/2.2.6createrole4.png?width90pc)
9. Cuộn xuống và kiểm tra 3 policies ```AWSElasticBeanstalkWebTier```, ```AWSElasticBeanstalkWorkerTier``` và ```AWSElasticBeanstalkMulticontainerDocker``` đã được thêm. Sau đó, nhấn **Create role** để tạo role.
    ![Create Role 5](/images/2.preparation/2.2createservicerole/2.2.7createrole5.png?width90pc)