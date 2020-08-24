---
layout: default
title: Static Content Hosting
nav_order: 1
permalink: /static_content_hosting/
parent: Step by Step Guide
---

# Static Content Hosting

## Step 1: Host Website on S3

1. Create Bucket
   ![Create Bucket 1](../../assets/s3/1.png)
   Fill in the bucket name with a unique and valid name, then accept the default settings.
   ![Name](../../assets/s3/2.png)
   ![Default Settings](../../assets/s3/3.png)

2. Upload Static Content
   ![Upload Files](../../assets/s3/4.png)
   ![Upload Files](../../assets/s3/5.png)
   ![File Uploaded](../../assets/s3/6.png)

3. Configure Static Website Hosting Property
   ![Static Website Hosting 1](../../assets/s3/7.png)
   ![Static Website Hosting 2](../../assets/s3/8.png)

4. Edit block public access settings
   ![Block Public Access](../../assets/s3/9.png)
   ![Confirm Block Public Access](../../assets/s3/10.png)
5. Add bucket policy to make bucket content publicly available
   ![Bucket Policy](../../assets/s3/11.png)
   ```json
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Sid": "PublicReadGetObject",
         "Effect": "Allow",
         "Principal": "*",
         "Action": ["s3:GetObject"],
         "Resource": ["arn:aws:s3:::covid-no-19/*"]
       }
     ]
   }
   ```
6. Test S3 Website Endpoint
   Return to `Properties` page, click on `Static Website Hosting` and Click on the endpoint provided.
   
   ![Endpoint](../../assets/s3/12.png)
   
   ![Result](../../assets/s3/13.png)

---

## Step 2: Serve static website hosted on S3 with Cloudfront

1. Navigate to Amazon Cloudfront
   ![navigate to cloudfront](../../assets/cloudfront/1.png)
2. Create Distribution
   ![create](../../assets/cloudfront/2.png)
   ![get started](../../assets/cloudfront/3.png)
   
   Copy the url of our S3 hosted website.
   ![copy url](../../assets/cloudfront/4.png)

   Paste URL on the `Origin Domain Name` field and select redirect HTTP to HTTPS.
   ![domain name](../../assets/cloudfront/5.png)

   Select Price Class, type of SSL certificate, and supported HTTP versions.
   ![set price and ssl](../../assets/cloudfront/6.png)

   Create Distribution
   ![Create Distribution](../../assets/cloudfront/7.png)

3. Test Endpoint
   We will be redirected to the cloudfront distributions dashboard. Wait for the state to change from `In Progress` to `Enabled`.
   ![wait for state to change](../../assets/cloudfront/8.png)
   Once enabled, copy the cloudfront endpoint.
   ![enabled state](../../assets/cloudfront/9.png)
   Open a new tab and access the endpoint using your browser.
   ![access website](../../assets/cloudfront/10.png)