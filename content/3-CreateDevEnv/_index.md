---
title : "Create Develop environment in Elastic Beanstalk"
date: 2024-01-01
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---
1. Download source code here [**nodejs.zip**](/images/nodejs.zip)
2. Go to [AWS Management Console](https://aws.amazon.com/vi/console/)
3. Search key word ```Elastic Beanstalk``` and select.
![SearchBeanStalk](/images/3.createdevenv/3.1selectbeanstalk.png?width=80pc)

4. Click **Create Application**.
![CreateApplication](/images/3.createdevenv/3.2createapplication.png?width=80pc)

5. In **Configure environment** stage.
- Select **Web server environment**
- In **Application name** field, input the name of your application. Ex: ```FCJ-My-First-App```.
- In **Environment name** field, input ```FCJ-My-First-App-env-DEV``` for Develop environment.
![InputApplicationName](/images/3.createdevenv/3.3inputapplicationname.png?width=80pc)

- In **Platform** field, choose **NodeJS**
- In **Application code**, choose **Upload your code**. 
- In **Version lable** , input ```V1-Green_DEV```
- Then choose **Local file** and click **Choose file** to upload source code from your local machine.
    ![Choose Platform](/images/3.createdevenv/3.4chooseplatform.png?width=80pc)

- In **Presets** field, choose **Single instance (free tier eligible)**. Then click **Next**.
    ![Choose Presets](/images/3.createdevenv/3.5choosepreset.png?width=80pc)

6. In **Configure service access** interface:
    - At **Service role**, choose **Use an existing role**.
    - At **Existing service roles**, select role **aws-elasticbeanstalk-service-role**.
    - At **EC2 key pair**, select **FCJ-KeyPair**.
    - At **EC2 instance profile**, select role **aws-elasticbeanstalk-ec2-role**.
    - Then click **Skip to review** to go to next step.
    ![Choose Presets](/images/3.createdevenv/3.6chooserole.png?width=80pc)

7. Scroll down and click **Submit** to create application and its environment.
    ![Choose Presets](/images/3.createdevenv/3.7submit.png?width=80pc)

8. Check the result, the environment is creating.
    ![Choose Presets](/images/3.createdevenv/3.8creating.png?width=80pc)
{{% notice info %}}
This process will take you about 5 minutes to finish.
{{% /notice  %}}

9. See the result after the environment is created successfully.
    ![Choose Presets](/images/3.createdevenv/3.9created.png?width=80pc)

10. Click to **Domain** of environment to see the result of your application.
    ![Domain](/images/3.createdevenv/3.10domain.png?width=80pc)
    ![Domain](/images/3.createdevenv/3.11result.png?width=80pc)

{{% notice note %}}
Remember that the background of your application now is **Green**.
{{% /notice  %}}

11. Navigate to [EC2 Dashboard](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Home:).
12. Click to **Instance**. You will see the instance name **FCJ-My-First-App-env-DEV** had been provisioned by Elastic Beanstalk.
    ![EC2 Dashboard](/images/3.createdevenv/3.12navigateec2.png?width=80pc)
13. Select the instances and copy the **Public IP address**.
    ![Copy Public IP address](/images/3.createdevenv/3.13selectinstance.png?width=80pc)
14. SSH to instance with **Public IP address** and **FCJ-KeyPair** was created at [2.1-Create Key Pair](../2-preparation/2.1-createkeypair/)
    ![SSH to instance](/images/3.createdevenv/3.14sshtoec2.png?width=80pc)