---
title : "Cập nhật ứng dụng trong môi trường phát triển"
date: 2024-01-01
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

1. Giản nén tệp **nodejs.zip** như tập tin với tên là ```nodejs-V2```.
    ![Search BeanStalk](/images/5.updateapp/5.1extractfile.png?width=80pc)

2. Mở tập tin **nodejs-V2**, chỉnh sửa tệp **index.html**.
    - Tại dòng 38, thay thế **73A53E** với **0000FF** và lưu.
    ![Search BeanStalk](/images/5.updateapp/5.2modifyindex.png?width=80pc)

3. Nén tất cả các tệp trong tập tin **nodejs-V2** thành **nodejs-V2.zip**.
{{% notice info %}}
Bạn có thể tải xuống source code [nodejs-V2.zip](/images/5.updateapp/nodejs-V2.zip) để bỏ qua các bước trên.
{{% /notice  %}}
   
    ![Search BeanStalk](/images/5.updateapp/5.3zipfile.png?width=80pc)
    
4. Đi đến [Environment](https://ap-southeast-1.console.aws.amazon.com/elasticbeanstalk/home?region=ap-southeast-1#/environments) của **Elastic Beanstalk**.
5. Nhấn vào môi trường **FCJ-My-First-App-env-DEV**.
    ![Search BeanStalk](/images/5.updateapp/5.4clickenv.png?width=80pc)

6. Nhấn **Upload and deploy**.
    ![Search BeanStalk](/images/5.updateapp/5.5uploadanddeploy.png?width=80pc)

7. Tại giao diện **Upload and deploy**.
    - Nhấn nút **Choose file** để tải lên source code từ máy tính cá nhân.
    - Chọn và tải lên tệp tên **nodejs-V2.zip**.
    - Nhập ```V2-BLUE-DEV``` tại **Version label**.
    - Nhấn **Deploy**.
    ![Deploy App](/images/5.updateapp/5.6fillinfo.png?width=80pc)
8. Sau vài giây, ứng dụng của bạn đã được tải lên môi trường phát triển thành công. Nhấn **Domain** để xem kết quả.
    ![Deploy App](/images/5.updateapp/5.7uploadsuccessfull.png?width=80pc)
    ![Deploy App](/images/5.updateapp/5.8uploadsuccessfull.png?width=80pc)

{{% notice note %}}
 Tại thời điểm này, nền của môi trường phát triển là **Xanh dương** và môi trường sản phẩm là **Xanh lá**.
{{% /notice  %}}