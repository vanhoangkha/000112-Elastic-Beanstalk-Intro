---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Application**: Elastic Beanstalk directly takes in our project code. So Elastic Beanstalk application is named the same as your project home directory.

**Application Environments**: Users may want their application to run on different environments like DEV, UAT, and PROD. You can create and configure different environments to run applications on different stages.

**Isolated**: All environments within a single application are isolated from each other (independent of each others’ running states). Needless to say, two different applications are also isolated.

**Scalability**: Using Auto-Scaling within Elastic Beanstalk makes the application dynamically scalable.

**Elastic Load Balancing**: All the web requests to the application are not directly relayed to application instances. They first hit the Elastic Load Balancer (ELB), which, as the name suggests, balances the load across all the application instances.

**Language support**: Elastic Beanstalk supports the applications developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.

**Pricing**: There is no extra charge for using Elastic Beanstalk. Users are only required to pay for the services and resources provisioned by Elastic Beanstalk Service.