---
title : "Tạo môi trường phát triển trong Elastic Beanstalk"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---

1. Tải xuống source code [**nodejs.zip**](/images/nodejs.zip)
2. Đi đến [AWS Management Console](https://aws.amazon.com/vi/console/)
3. Tìm kiếm từ khóa ```Elastic Beanstalk``` và chọn.
![SearchBeanStalk](/images/3.createdevenv/3.1selectbeanstalk.png?width=80pc)

4. Nhấn **Create Application**.
![CreateApplication](/images/3.createdevenv/3.2createapplication.png?width=80pc)

5. Trong mục **Configure environment**.
- Chọn **Web server environment**
- Trong phần **Application name**, nhập tên ứng dụng của bạn. Ví dụ: ```FCJ-My-First-App```.
- Trong phần **Environment name**, nhập ```FCJ-My-First-App-env-DEV``` cho môi trường phát triển.
![InputApplicationName](/images/3.createdevenv/3.3inputapplicationname.png?width=80pc)

- Trong phần **Platform**, chọn **NodeJS**
- Trong phần **Application code**, chọn **Upload your code**. 
- Trong phần **Version lable** , nhập ```V1-Green_DEV```
- Sau đó chọn **Local file** và nhấn **Choose file** để tải lên source code của bạn từ máy tính cá nhân.
    ![Choose Platform](/images/3.createdevenv/3.4chooseplatform.png?width=80pc)

- Trong phần **Presets**, chọn **Single instance (free tier eligible)**. Sau đó nhấn **Next**.
    ![Choose Presets](/images/3.createdevenv/3.5choosepreset.png?width=80pc)

6. Trong giao diện **Configure service access**:
    - Tại **Service role**, chọn **Use an existing role**.
    - Tại **Existing service roles**, chọn role **aws-elasticbeanstalk-service-role**.
    - Tại **EC2 key pair**, chọn **FCJ-KeyPair**.
    - Tại **EC2 instance profile**, chọn role **aws-elasticbeanstalk-ec2-role**.
    - Sau đó nhấn **Skip to review** để đi đến bước tiếp theo.
    ![Choose Presets](/images/3.createdevenv/3.6chooserole.png?width=80pc)

7. Cuộn xuống và nhấn **Submit** để tạo ứng dụng và môi trường của nó.
    ![Choose Presets](/images/3.createdevenv/3.7submit.png?width=80pc)

8. Kiểm tra kết quả, môi trường đang được tạo.
    ![Choose Presets](/images/3.createdevenv/3.8creating.png?width=80pc)
{{% notice info %}}
Quá trình này có thể mất đến 5 phút để hoàn thành.
{{% /notice  %}}

9. Kiểm tra kết quả sau khi môi trường được tạo thành công.
    ![Choose Presets](/images/3.createdevenv/3.9created.png?width=80pc)

10. Nhấn **Domain** của môi trường để thấy kết quả ứng dụng của bạn.
    ![Domain](/images/3.createdevenv/3.10domain.png?width=80pc)
    ![Domain](/images/3.createdevenv/3.11result.png?width=80pc)

{{% notice note %}}
Lưu ý rằng nền của môi trường phát triển hiện tại là **Xanh lá**.
{{% /notice  %}}

11. Chuyển hướng đến [EC2 Dashboard](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Home:).
12. Nhấn **Instance**. Bạn sẽ thấy máy chủ tên **FCJ-My-First-App-env-DEV** vừa được tạo bởi Elastic Beanstalk.
    ![EC2 Dashboard](/images/3.createdevenv/3.12navigateec2.png?width=80pc)
13. Chọn máy chủ và sao chép **Public IP address**.
    ![Copy Public IP address](/images/3.createdevenv/3.13selectinstance.png?width=80pc)
14. SSH đến máy chủ với **Public IP address** và **FCJ-KeyPair** vừa tạo ở [2.1-Create Key Pair](../2-preparation/2.1-createkeypair/)
    ![SSH to instance](/images/3.createdevenv/3.14sshtoec2.png?width=80pc)