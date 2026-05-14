---
title : "Update application in Develop environment"
date: 2024-01-01
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---
1. Extract file **nodejs.zip** as a folder with name is ```nodejs-V2```.
    ![Search BeanStalk](/images/5.updateapp/5.1extractfile.png?width=80pc)

2. Open **nodejs-V2** folder, edit file **index.html**.
    - At line 38, replace **73A53E** with **0000FF** and save.
    ![Search BeanStalk](/images/5.updateapp/5.2modifyindex.png?width=80pc)

3. Zip all files in folder **nodejs-V2** to **nodejs-V2.zip**.
{{% notice info %}}
 You can download this file [nodejs-V2.zip](/images/5.updateapp/nodejs-V2.zip) to skip these steps.
{{% /notice  %}}
   
    ![Search BeanStalk](/images/5.updateapp/5.3zipfile.png?width=80pc)
    
4. Go to [Environment](https://ap-southeast-1.console.aws.amazon.com/elasticbeanstalk/home?region=ap-southeast-1#/environments) of **Elastic Beanstalk**.
5. Click to Develop environment **FCJ-My-First-App-env-DEV**.
    ![Search BeanStalk](/images/5.updateapp/5.4clickenv.png?width=80pc)

6. Click **Upload and deploy**.
    ![Search BeanStalk](/images/5.updateapp/5.5uploadanddeploy.png?width=80pc)

7. At **Upload and deploy** interface.
    - Click **Choose file** button to upload source code file from your local machine.
    - Select and upload file name **nodejs-V2.zip**.
    - Input ```V2-BLUE-DEV``` at **Version label**.
    - Click **Deploy**.
    ![Deploy App](/images/5.updateapp/5.6fillinfo.png?width=80pc)
8. After few seconds, your application is uploaded successfully into Develop environment. Click to **Domain** to see the results.
    ![Deploy App](/images/5.updateapp/5.7uploadsuccessfull.png?width=80pc)
    ![Deploy App](/images/5.updateapp/5.8uploadsuccessfull.png?width=80pc)

{{% notice note %}}
 At this time, background of Develop environment is **Blue** and Production environment is **Green**.
{{% /notice  %}}