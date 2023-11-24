---
title : "Preparation"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
### Preparation steps
- **Key Pair**: To SSH to EC2 instances which were provisioned by Elastic Beanstalk.
- **IAM service role**: Elastic Beanstalk assumes a service role to use other AWS services on your behalf. The service role already exists in your account and you then create a new environment in Elastic Beanstalk console or using Elastic Beanstalk CLI.
- **IAM instance role**: Elastic Beanstalk applies instances profile to the instances in your environment. It allows them to do the following:
    + Retrieve application versions from Amazon Simple Storage Service (Amazon S3).
    + Upload logs to Amazon S3.
    + Perform other tasks that vary depending on the environment type and platform.

### Content

2.1. [Create Key Pair](2.1-createkeypair/).

2.2. [Create IAM instance role](2.2-createinstancerole/).
