---
layout: default
title: Most Efficient Solution
nav_order: 1
permalink: /main_solution/
parent: Solutions
---

# Most Efficient Solution

The team feels that the most efficient solution is to create a website and host it using AWS cloud computing services. This would make use of various services, such as [Amazon Simple Storage Service (S3)](https://aws.amazon.com/s3/), [Amazon CloudFront](https://aws.amazon.com/cloudfront/?nc2=type_a), [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/?nc2=type_a), which provisions, [Elastic Compute Cloud (EC2)](https://aws.amazon.com/ec2/), [Amazon Relational Database Service (RDS)](https://aws.amazon.com/rds/), [Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/?nc2=type_a), [Amazon Auto Scaling](https://aws.amazon.com/ec2/autoscaling/?nc2=type_a), and [AWS CodePipeline](https://aws.amazon.com/codepipeline/?nc2=type_a).

## Hosting Static Content

For static content hosting, we are using Amazon S3 and Amazon Cloudfront.

- Amazon Simple Storage Service (S3)<br>
  By using S3, it would allow us to store our static content and host a static website. Where each page is coded in HTML and displays the same information to every visitor. We feel that using S3 has its advantages such as its enhanced security, Scalability and Migration of Data from cloud.
  S3 also works with EC2 as data in the S3 storage system is accessible to EC2 instances. EC2 allows customers to have access to the same highly scalable, efficient and reliable data storage system that Amazon also utilizes to operate its global network of websites.
- CloudFront<br>
  CloudFront's purpose was to serve the static website. We used CloudFront as its advantages are to accelerate static website content delivery and it is inexpensive.

Read the guide [here](/steps/static_content_hosting)
  
## Backend Architecture

We are using Elastic Beanstalk to provision the backend architecture.
Elastic Beanstalk is a platform as a service provided by AWS to help developers deploy their application with minimal settings on the architecture.
Our company is a small company that only needs a backend system to sell masks, it is more efficient to configure services with elastic beanstalk because it's efficient, quick, and easy, with no additional charge!
Elastic Beanstalk helps us provision several services and security configuration that would usually take quite a while to set up such as:
EC2 instance for the environment, Amazon S3, Amazon RDS, ELB, EBS, EC2 Auto Scaling, Elastic IP, and Security Groups

Read the guide [here](/steps/elastic_beanstalk)

## Deployment

AWS CodePipeline is a fully managed continuous delivery service that helps us deploy our application directly from github to elastic beanstalk.

Read the guide [here](/steps/code_pipeline)
