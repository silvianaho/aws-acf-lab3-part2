---
layout: default
title: Cleaning Up
nav_order: 4
permalink: /cleaning_up/
parent: Step by Step Guide
---

# Cleaning Up

## Code Pipeline

1. Delete Code Pipeline
   ![Code pipeline](../../assets/clean/1.png)

2. Confirm delete code pipeline 
   ![confirm del code pipeline](../../assets/clean/2.png)

3. Deleted State
   ![after delete code pipeline](../../assets/clean/3.png)

## Elastic Beanstalk

1. Delete Application
   ![delete application](../../assets/clean/4.png)

2. Confirm delete application
   ![confirm del eb app](../../assets/clean/5.png)

3. Deleting in progress
   ![del eb app in progress](../../assets/clean/6.png)
   We need to wait for a while for elastic beanstalk to terminate everything, we can terminate other services such as cloudfront and S3 while waiting for the termination process to complete.

4. Deleted
   ![terminated eb app](../../assets/clean/7.png)

## Cloudfront

1. Disable Distribution
   ![disable distribution](../../assets/clean/8.png)
   ![confirm disable dist](../../assets/clean/9.png)
   We would need to wait for around 5-15 minutes for it to disable completely before we are able to delete the distribution. Meanwhile, we can delete our S3 bucket.

2. Delete Distribution
   ![delete distribution](../../assets/clean/16.png)
   ![confirm delete dist](../../assets/clean/17.png)
3. Deleted State
   ![deleted cloudfront](../../assets/clean/18.png)

## S3 Bucket
 
1. Empty Bucket
   ![empty bucket](../../assets/clean/10.png)
   
   Enter bucket name to confirm deletion.
   ![enter name](../../assets/clean/11.png)

   Emptied bucket
   ![emptied bucket](../../assets/clean/12.png)
2. Delete Bucket
   ![delete bucket](../../assets/clean/13.png)
   Enter bucket name to confirm deletion.
   ![enter bucket name](../../assets/clean/14.png)
3. Deleted State
   ![deleted bucket](../../assets/clean/15.png)