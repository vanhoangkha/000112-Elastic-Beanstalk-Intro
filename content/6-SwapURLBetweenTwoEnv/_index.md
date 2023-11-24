---
title : "Swap URL of two environments"
date :  "`r Sys.Date()`" 
weight : 6 
chapter : false
pre : " <b> 6. </b> "
---
Because AWS Elastic Beanstalk performs an in-place update when you update your application versions, your application might become unavailable to users for a short period of time. To avoid this, perform a blue/green deployment. To do this, deploy the new version to a separate environment, and then swap the CNAMEs of the two environments to redirect traffic to the new version instantly.

{{% notice note %}}
 In this section, we will only focus on how to swap the URL between two environments (DEV and PROD).
{{% /notice  %}}

1. Go to [Environment](https://ap-southeast-1.console.aws.amazon.com/elasticbeanstalk/home?region=ap-southeast-1#/environments) of **Elastic Beanstalk**.
2. Select **FCJ-My-First-App-env-DEV** environment, click **Action** and choose **Swap environment domain**.
 ![Swap URL](/images/6.swapurl/6.1selectenv.png?width=80pc)
3. At **Environment**, choose **FCJ-My-First-App-env-PROD**. Then, click **Swap**.
 ![Swap URL](/images/6.swapurl/6.2swapenv.png?width=80pc)
4. After that, access to domain of **FCJ-My-First-App-env-DEV** and **FCJ-My-First-App-env-PROD** environment to see the result.
    - The background of **FCJ-My-First-App-env-DEV** environment now is **Green** and the URL is FCJ-My-First-App-env-PROD.*xxx*.ap-southeast-1.elasticbeanstalk.com.
    - The background of **FCJ-My-First-App-env-PROD** environment now is **Blue** and the URL is FCJ-My-First-App-env-DEV.*xxx*.ap-southeast-1.elasticbeanstalk.com.

So, two URLs of two environments are swapped each other.
    ![Result](/images/6.swapurl/6.3result.png?width=80pc)
    ![Result](/images/6.swapurl/6.4result.png?width=80pc)
    ![Result](/images/6.swapurl/6.5resultprod.png?width=80pc)
    ![Result](/images/6.swapurl/6.6resultdev.png?width=80pc)