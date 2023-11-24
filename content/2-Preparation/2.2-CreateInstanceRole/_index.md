---
title : "Create IAM instance role"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---
1.Go to [AWS Management Console](https://aws.amazon.com/vi/console/).
- Find **IAM**.
- Select **IAM**.
    ![Search IAM](/images/2.preparation/2.2createservicerole/2.2.1searchiam.png?width90pc)

2. In **IAM** interface, select **Roles**.

3. In **Role** interface, search the role name ```aws-elasticbeanstalk-ec2-role```. 

4. If this role is existing, you can skip this step and go to [3. Create Develop environment in Elastic Beanstalk](../../3-createdevenv/).
    
{{% notice warning %}} 
Check and make sure that this role was created with 3 policies ```AWSElasticBeanstalkWebTier```, ```AWSElasticBeanstalkWorkerTier``` and ```AWSElasticBeanstalkMulticontainerDocker```.
{{% /notice  %}}

5. If the role is not existing, you can create new role by clicking **Create role**.
    ![Create Role 1](/images/2.preparation/2.2createservicerole/2.2.3createrole1.png?width90pc)

6. At **Trusted entity type** interface:
    - Choose **AWS service**.
    - At **Use case**, search and choose **EC2** as service.
    - Choose **EC2** as use case.
    - Then click **Next**.
    ![Create Role 2](/images/2.preparation/2.2createservicerole/2.2.4createrole2.png?width90pc)

7. Then, search and add policies ```AWSElasticBeanstalkWebTier```, ```AWSElasticBeanstalkWorkerTier``` and ```AWSElasticBeanstalkMulticontainerDocker```.
    ![Create Role 3](/images/2.preparation/2.2createservicerole/2.2.5createrole3.png?width90pc)

8. Input the name of role ```aws-elasticbeanstalk-ec2-role```.
    ![Create Role 4](/images/2.preparation/2.2createservicerole/2.2.6createrole4.png?width90pc)
9. Scroll down and check 3 policies ```AWSElasticBeanstalkWebTier```, ```AWSElasticBeanstalkWorkerTier``` and ```AWSElasticBeanstalkMulticontainerDocker``` were added. Then, click **Create role** to create the role.
    ![Create Role 5](/images/2.preparation/2.2createservicerole/2.2.7createrole5.png?width90pc)