---
title : "Create Key Pair"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---
1. Go to [AWS Management Console](https://aws.amazon.com/vi/console/).
- Find **EC2**.
- Select **EC2**.
![Find EC2](/images/2.preparation/2.1createkeypair/2.1.1selectec2.png?width90pc)
2. In **EC2** interface, select **Key Pairs**.
3. Click **Create Key Pair**.
![Create Key Pair](/images/2.preparation/2.1createkeypair/2.1.2createkeypair1.png?width90pc)
4. Input the name of key pair ```FCJ-KeyPair```.
5. At **Key pair type**, choose **RSA**.
6. At **Private key file format**, choose **.pem**.
7. Click **Create key pair** to create.
![Create Key Pair](/images/2.preparation/2.1createkeypair/2.1.3createkeypair2.png?width90pc)
{{% notice warning %}} 
Make sure that key pair file was downloaded into your local machine.
{{% /notice  %}}
