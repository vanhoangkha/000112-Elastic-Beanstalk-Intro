---
title : "Hoán đổi URL giữa hai môi trường"
date :  "`r Sys.Date()`" 
weight : 6 
chapter : false
pre : " <b> 6. </b> "
---

Bởi vì AWS Elastic Beanstalk thực hiện cập nhật tại chỗ khi bạn cập nhật phiên bản ứng dụng của bạn, ứng dụng của bạn sẽ trở nên không khả dụng đến người dùng trong một khoảng thời gian ngắn. Để tránh việc này, thực hiện triển khai blue/green. Để làm điều này, triển khai một phiên bản mới ở môi trường riêng biệt, và sau đó chuyển đổi CNAMEs của hai môi trường để điều hướng lưu lượng đến phiên bản mới ngay lập tức.

{{% notice note %}}
Trong phần này, chúng ta sẽ chỉ tập trung vào việc làm thế nào để chuyển đổi URL giữa hai môi trường (Phát triển và sản phẩm).
{{% /notice  %}}

1. Đi đến [Environment](https://ap-southeast-1.console.aws.amazon.com/elasticbeanstalk/home?region=ap-southeast-1#/environments) của **Elastic Beanstalk**.
2. Chọn môi trường **FCJ-My-First-App-env-DEV**, nhấn **Action** và chọn **Swap environment domain**.
 ![Swap URL](/images/6.swapurl/6.1selectenv.png?width=80pc)
3. Tại **Environment**, chọn **FCJ-My-First-App-env-PROD**. Sau đó, nhấn **Swap**.
 ![Swap URL](/images/6.swapurl/6.2swapenv.png?width=80pc)
4. Sau đó, truy cập tên miền của môi trường **FCJ-My-First-App-env-DEV** và **FCJ-My-First-App-env-PROD** để thấy kết quả.
    - Nền của môi trường **FCJ-My-First-App-env-DEV** hiện tại là **Xanh lá** và URL là FCJ-My-First-App-env-PROD.*xxx*.ap-southeast-1.elasticbeanstalk.com.
    - Nền của môi trường **FCJ-My-First-App-env-PROD** hiện tại là **Xanh dương** và URL là FCJ-My-First-App-env-DEV.*xxx*.ap-southeast-1.elasticbeanstalk.com.

Như vậy, hai URLs của hai môi trường đã được chuyển đổi cho nhau.
    ![Result](/images/6.swapurl/6.3result.png?width=80pc)
    ![Result](/images/6.swapurl/6.4result.png?width=80pc)
    ![Result](/images/6.swapurl/6.5resultprod.png?width=80pc)
    ![Result](/images/6.swapurl/6.6resultdev.png?width=80pc)