---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

**Ứng dụng**: Elastic Beanstalk trực tiếp lấy mã dự án của chúng ta. Vì thế Elastic Beanstalk application được đặt tên giống với thư much chính của dự án.

**Các môi trường ứng dụng**: Người dùng muốn ứng dụng của họ được triển khai trên nhiều môi trường khác nhau như DEV, UAT, và PROD. Bạn có thể ạo và cấu hình nhiều môi trường khác nhau để triển khai ứng dụng trên các giai đoạn khác nhau.

**Cô lập**: Tất cả các môi trường bên trong một ứng dụng được cô lập với nhau (độc lập với trạng thái hoạt động của nhau). Không cần phải nói, hai ứng dụng khác nhau cũng sẽ bị cô lập với nhau.

**Khả năng co giãn**: Sử dụng Auto-Scaling trong Elastic Beanstalk làm cho ứng dụng có khả năng mở rộng linh hoạt.

**Bộ cân bằng tải đàn hổi (ELB)**: Tất cả lượng yêu cầu từ web đến ứng dụng không được chuyển trực tiếp đến các máy chủ của ứng dụng. Chúng sẽ gặp Bộ cân bằng tải đàn hồi (ELB) đầu tiên, cân bằng tải trên tất cả các máy chủ ứng dụng.

**Ngôn ngữ hổ trợ**: Elastic Beanstalk hổ trợ các ứng dụng được phát triển với Java, .NET, PHP, Node.js, Python, Ruby, Go, và Docker trên các máy chủ quen thuộc như Apache, Nginx, Passenger, và IIS.

**Chi phí**: Không có bất kỳ chi phí phát sinh nào cho việc sử dụng Elastic Beanstalk. Người dùng chỉ cần phải chi trả cho các dịch vụ và tài nguyên được tạo ra bởi Elastic Beanstalk Service.