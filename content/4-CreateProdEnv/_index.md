---
title : "Create Production environment in Elastic Beanstalk"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---

1. Go to [AWS Management Console](https://aws.amazon.com/vi/console/)

2. Search key word ```Elastic Beanstalk``` and select.
    ![Search BeanStalk](/images/4.createprodenv/4.1selectbeanstalk.png?width=80pc)

3. Click **Application** and click to application name was created.
    ![Select Application](/images/4.createprodenv/4.2selectapplication.png?width=80pc)

4. Click **Create environment** to create Production environment.
    ![Select Application](/images/4.createprodenv/4.3createenv.png?width=80pc)

5. Input the name of environment ```FCJ-My-First-App-env-PROD``` at **Environment name**.
    - Choose **NodeJS** at **Platform**.
    ![Select Application](/images/4.createprodenv/4.4selectplatform.png?width=80pc)
    - Choose **Upload your code** at **Application code**
    - Input ```V1-GREEN-PROD``` at **Version label**
    - Choose **Local file** and click **Choose file** button to upload your code.
    - Select the **nodejs.zip** file that you had downloaded.
    - Choose **High availability** at **Presets**.
    - Then click **Next** to go to next step. 
    ![Select Application](/images/4.createprodenv/4.5uploadfile.png?width=80pc)
6. In **Configure service access** interface:
    - At **Service role**, choose **Use an existing role**.
    - At **Existing service roles**, select role **aws-elasticbeanstalk-service-role**.
    - At **EC2 key pair**, select **FCJ-KeyPair**.
    - At **EC2 instance profile**, select role **aws-elasticbeanstalk-ec2-role**.
    - Then click **Skip to review** to go to next step.
    ![Choose Presets](/images/4.createprodenv/4.6chooserole.png?width=80pc)
7. Scroll down and click **Submit** to create environment.
    ![Choose Presets](/images/4.createprodenv/4.7submit.png?width=80pc)

8. Check the result, the environment is creating.
    ![Choose Presets](/images/4.createprodenv/4.8creating.png?width=80pc)
{{% notice info %}}
This process will take you about 5 minutes to finish.
{{% /notice  %}}
9. See the result after the environment is created successfully.
    ![Choose Presets](/images/4.createprodenv/4.9created.png?width=80pc)

10. Click to **Domain** of environment to see the result.
    ![Choose Presets](/images/4.createprodenv/4.10domain.png?width=80pc)
    ![Choose Presets](/images/4.createprodenv/4.11result.png?width=80pc)
{{% notice note %}}
Remember that the background of your application now is **Green**.
{{% /notice  %}}

11. Navigate to [EC2 Dashboard](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Home:).
12. Click to **Instance**. You will see the instance name **FCJ-My-First-App-env-PROD** had been provisioned by Elastic Beanstalk.
    ![Choose Presets](/images/4.createprodenv/4.12ec2dashboard.png?width=80pc)
    ![Choose Presets](/images/4.createprodenv/4.13prodec2.png?width=80pc)

13. Click to **Auto Scaling Groups**, you will see two ASGs are created. 
    - The ASG with Max = 4, belongs to **FCJ-My-First-App-env-PROD** environment.
    - The ASG with Max = 1, belongs to **FCJ-My-First-App-env-DEV** environment.
    ![Choose Presets](/images/4.createprodenv/4.14asg.png?width=80pc)

14. Click to **Load Balancers**, you will see an ALB is created.
    - Select ALB.
    - Click **Listeners and rules** tab.
    - Click to the target group below.
    ![Choose Presets](/images/4.createprodenv/4.15alb.png?width=80pc)

15. In **Target Group** interface, at **Registered targets** you can see the instance that belongs to **FCJ-My-First-App-env-PROD** environment.
    ![Choose Presets](/images/4.createprodenv/4.16targetgroup.png?width=80pc)
{{% notice tip %}}
An ASG and ALB was created in Production environment since you selected **High availability** at **Presets** when configuring the Elastic Beanstalk.
{{% /notice  %}}