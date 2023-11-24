---
title : "Tạo môi trường sản phẩm trong Elastic Beanstalk"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---

1. Đi đến [AWS Management Console](https://aws.amazon.com/vi/console/)

2. Tìm kiếm từ khóa ```Elastic Beanstalk``` và chọn.
    ![Search BeanStalk](/images/4.createprodenv/4.1selectbeanstalk.png?width=80pc)

3. Nhấn **Application** và nhấn vào ứng dụng vừa được tạo.
    ![Select Application](/images/4.createprodenv/4.2selectapplication.png?width=80pc)

4. Nhấn **Create environment** để tạo môi trường sản phẩm.
    ![Select Application](/images/4.createprodenv/4.3createenv.png?width=80pc)

5. Nhập tên của môi trường ```FCJ-My-First-App-env-PROD``` tại **Environment name**.
    - Chọn **NodeJS** tại **Platform**.
    ![Select Application](/images/4.createprodenv/4.4selectplatform.png?width=80pc)
    - Chọn **Upload your code** tại **Application code**
    - Nhập ```V1-GREEN-PROD``` tại **Version label**
    - Chọn **Local file** và nhấn nút **Choose file** để tải lên source code của bạn.
    - Chọn tệp **nodejs.zip** mà bạn vừa tải xuống.
    - Nhấn **High availability** tại **Presets**.
    - Sau đó nhấn **Next** để đi đến bước tiếp theo. 
    ![Select Application](/images/4.createprodenv/4.5uploadfile.png?width=80pc)
6. Trong giao diện **Configure service access**:
    - Tại **Service role**, chọn **Use an existing role**.
    - Tại **Existing service roles**, chọn role **aws-elasticbeanstalk-service-role**.
    - Tại **EC2 key pair**, chọn **FCJ-KeyPair**.
    - Tại **EC2 instance profile**, chọn role **aws-elasticbeanstalk-ec2-role**.
    - Sau đó nhấn **Skip to review** để đi đến bước tiếp theo.
    ![Choose Presets](/images/4.createprodenv/4.6chooserole.png?width=80pc)
7. Cuộn xuống và nhấn **Submit** để tạo môi trường.
    ![Choose Presets](/images/4.createprodenv/4.7submit.png?width=80pc)

8. Kiểm tra kết quả, môi trường đang được tạo.
    ![Choose Presets](/images/4.createprodenv/4.8creating.png?width=80pc)
{{% notice info %}}
Quá trình này có thể mất đến 5 phút để hoàn thành.
{{% /notice  %}}
9. Kiểm tra kết quả sau khi môi trường được tạo thành công.
    ![Choose Presets](/images/4.createprodenv/4.9created.png?width=80pc)

10. Nhấn **Domain** của môi trường để kiểm tra kết quả.
    ![Choose Presets](/images/4.createprodenv/4.10domain.png?width=80pc)
    ![Choose Presets](/images/4.createprodenv/4.11result.png?width=80pc)
{{% notice note %}}
Lưu ý rằng nền của môi trường sản phẩm hiện tại là **Xanh lá**.
{{% /notice  %}}

11. Chuyển hướng đến [EC2 Dashboard](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Home:).
12. Nhấn **Instance**. Bạn sẽ thấy máy chủ tên **FCJ-My-First-App-env-PROD** vừa được tạo bởi Elastic Beanstalk.
    ![Choose Presets](/images/4.createprodenv/4.12ec2dashboard.png?width=80pc)
    ![Choose Presets](/images/4.createprodenv/4.13prodec2.png?width=80pc)

13. Nhấn **Auto Scaling Groups**, bạn sẽ thấy 2 ASGs được tạo. 
    - ASG với Max = 4, thuộc về môi trường **FCJ-My-First-App-env-PROD**.
    - ASG với Max = 1, thuộc về môi trường **FCJ-My-First-App-env-DEV**.
    ![Choose Presets](/images/4.createprodenv/4.14asg.png?width=80pc)

14. Nhấn **Load Balancers**, bạn sẽ thấy 1 ALB được tạo.
    - Chọn ALB.
    - Nhấn **Listeners and rules**.
    - Nhấn target group phía dưới.
    ![Choose Presets](/images/4.createprodenv/4.15alb.png?width=80pc)

15. Trong giao diện **Target Group**, tại **Registered targets** bạn có thể thấy máy chủ thuộc về môi trường **FCJ-My-First-App-env-PROD**.
    ![Choose Presets](/images/4.createprodenv/4.16targetgroup.png?width=80pc)
{{% notice tip %}}
Một ASG và ALB được tạo ra trong môi trường sản phẩm vì bạn đã chọn **High availability** tại **Presets** khi cấu hình Elastic Beanstalk.
{{% /notice  %}}