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
   ![Create Bucket 1](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/f935e6af-64dc-45a4-a70a-94709ea9cf12/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T052857Z&X-Amz-Expires=86400&X-Amz-Signature=d89ac041018748472c67a21ebd75584cb75f8f2f0be1b131448b5a3e7b96df56&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   Fill in the bucket name with a unique and valid name, then accept the default settings.
   ![Name](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2d0c5418-e4b5-4936-b2ee-3f93b02d0214/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T055444Z&X-Amz-Expires=86400&X-Amz-Signature=18600caf00e51960a99bd9bca142ef214ab0993eca8f24e43ec6e7323937be08&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![Default Settings](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4cda48f2-20e4-482a-b2f9-29a2a6cfab90/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T055513Z&X-Amz-Expires=86400&X-Amz-Signature=f152ce797b8f2b94065c4b03679ded20bf13da3e5ea1f64896eb76979b70a12f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

2. Upload Static Content
   ![Upload Files](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6fba1e6f-33da-407f-bc31-1d91361988f1/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T055551Z&X-Amz-Expires=86400&X-Amz-Signature=924f0aeea0d88ab1f65048b213d350023cd10218dc2f6b4aa475de5e94e790a4&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![Upload Files](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4925eaae-d736-4613-8c7a-5c9bf4c4dcaf/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T055903Z&X-Amz-Expires=86400&X-Amz-Signature=7e2aa63e67f62bff7b381b76c0b21dee10fe2dadef340a291f595e226d598446&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![File Uploaded](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/346eb878-d6e2-43b7-9536-a7ed0e6d8d8c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T055915Z&X-Amz-Expires=86400&X-Amz-Signature=bff560caf4475746f1bf9698dd5d78543ed875d04751f78ffb1ac992ab5e6c56&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

3. Configure Static Website Hosting Property
   ![Static Website Hosting 1](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8d234378-6345-4b2b-8dcd-1b35f596492e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T055943Z&X-Amz-Expires=86400&X-Amz-Signature=5d1a5a7463f0e4f78fe615a62b65cb22d601c28f31480a2f53778780bad66df2&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![Static Website Hosting 2](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e2258f4c-9861-4a90-b5a2-0d4684788cb7/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T055946Z&X-Amz-Expires=86400&X-Amz-Signature=604c87503793d62c03cd4494c9df1a0d6770e52476d0e4132b8c73a4b974675a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

4. Edit block public access settings
   ![Block Public Access](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/1ffeae69-e569-475b-bd4b-cc14aa70660b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T060106Z&X-Amz-Expires=86400&X-Amz-Signature=85f9e142c39c91b53a9455d0d1b30dcc43163ab5b624080b41060baf2c92c568&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![Confirm Block Public Access](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/f0bfc35d-15f3-4cee-b533-8cd3d0f949e4/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T060137Z&X-Amz-Expires=86400&X-Amz-Signature=fd4e316b4c4416037c7d9a0e129a6051f5a88856c5d157aec16bca866e964b7d&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
5. Add bucket policy to make bucket content publicly available
   ![Bucket Policy](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/f2068586-ab05-4df4-98ed-b2e242adff1d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T060202Z&X-Amz-Expires=86400&X-Amz-Signature=0735a52b120667c4354d20881e131749c415f0075f76f2c219f2df48b5120b2d&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
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
   
   ![Endpoint](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/21323b71-2144-4d97-bf1f-dff4899105ff/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T060342Z&X-Amz-Expires=86400&X-Amz-Signature=133468546c39c168931ec6af123692b5212c54cf0d235a70a5e429003b00e85f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   
   ![Result](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a040c8f7-ac86-472f-837b-6ff3957e12f8/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T060438Z&X-Amz-Expires=86400&X-Amz-Signature=3bb145bfdc5653afb17ce90aa6dbefe16a99d60025420d6c46cdce86e34e9006&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

## Step 2: Serve static website hosted on S3 with Cloudfront

1. Navigate to Amazon Cloudfront
   ![navigate to cloudfront](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/304da671-c615-4acd-bf35-0b131b3dc4b0/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T062413Z&X-Amz-Expires=86400&X-Amz-Signature=24a8dfd622503395638952508c12f025f2ba6d1e4ace3bb36363cfeab4663edf&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
2. Create Distribution
   ![create](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/db61037a-74cb-412c-82ff-2446ca5eb74c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T062457Z&X-Amz-Expires=86400&X-Amz-Signature=0100479cae1b772f10504fa012ac89e86b73fcd63dd4f97bb017b3d94d2d6216&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![get started](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a80ec820-429f-4451-ad46-e121398a4f8b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T062500Z&X-Amz-Expires=86400&X-Amz-Signature=2a9935f363a2dcbfde47e7a05a6eef16d6dc825a20409479fa4a44b896628bdb&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   
   Copy the url of our S3 hosted website.
   ![copy url](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/75f30ac1-1c1f-485c-a648-74d6476d42e0/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T062545Z&X-Amz-Expires=86400&X-Amz-Signature=8b32a08c86f94a18f74f0fe407ca4eee12d0e1a12f06e9de54dcecea3c43a825&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

   Paste URL on the `Origin Domain Name` field and select redirect HTTP to HTTPS.
   ![domain name](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c0d82c3d-4ac8-4ef1-a4f8-d8f808d377a4/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T062627Z&X-Amz-Expires=86400&X-Amz-Signature=cb0da4b9f072b5f780dfe5624b33806c377e292cfb1dd8bb1c503448c094a298&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

   Select Price Class, type of SSL certificate, and supported HTTP versions.
   ![set price and ssl](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/779e5fdb-b3a6-4b76-83bd-4ff7086a21f5/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T062750Z&X-Amz-Expires=86400&X-Amz-Signature=037de32ecc1e70ba404cc262d74d32f3188c9e4549d506f4149e8780c7e5cf78&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

   Create Distribution
   ![Create Distribution](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/fd4fd258-8cf6-41df-a028-4933f3c67b64/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T062753Z&X-Amz-Expires=86400&X-Amz-Signature=b0cb6fc13c0d5182b1a8487e4c876fd15225b9863bccde2c1b49c7e955cbacbb&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

3. Test Endpoint
   We will be redirected to the cloudfront distributions dashboard. Wait for the state to change from `In Progress` to `Enabled`.
   ![wait for state to change](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/74c55f8b-5592-4134-b64f-2237a5fabb3c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T062935Z&X-Amz-Expires=86400&X-Amz-Signature=874d92ace03609900453f25319974186497db5d66d82584ae38c13bd725664b3&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   Once enabled, copy the cloudfront endpoint.
   ![enabled state](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/85bbed98-1de8-489d-b564-68a11aaf67c9/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T063159Z&X-Amz-Expires=86400&X-Amz-Signature=916009ef4a36d4b4d56f335cad2c58fd12146734f792c1c7ba459f1cf2d2c0e0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   Open a new tab and access the endpoint using your browser.
   ![access website](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5dca1a9a-c2ad-491f-966b-b427a85d9f9f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T063322Z&X-Amz-Expires=86400&X-Amz-Signature=8c3a3f87935ace190124f68d8efeea9ffde7c70e4acea2499f8ecb5c0284714a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)