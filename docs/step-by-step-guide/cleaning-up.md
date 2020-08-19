---
layout: default
title: Cleaning Up
nav_order: 3
permalink: /cleaning_up/
parent: Step by Step Guide
---

# Cleaning Up

## Code Pipeline

1. Delete Code Pipeline
   ![Code pipeline](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e9035034-43c1-4110-8192-207ed43913f4/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T133458Z&X-Amz-Expires=86400&X-Amz-Signature=6463120169a611c9948a577c0244eeae9be1074e910dbafc379b0be1fe660c2f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

2. Confirm delete code pipeline 
   ![confirm del code pipeline](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/121f9c69-419c-4e72-8553-fd7541136cfc/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T133519Z&X-Amz-Expires=86400&X-Amz-Signature=6fd2f611cdcfa5aa425c81b1f7491a848e0a7f3fa0691aae96d1503278500237&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

3. Deleted State
   ![after delete code pipeline](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/035189f6-043a-45fe-a42d-c2fd78a48444/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T133614Z&X-Amz-Expires=86400&X-Amz-Signature=87a014b2b3ccb7a24d801b2e8b478fc4840adc61f70ac7f2373f90bb7afbc111&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

## Elastic Beanstalk

1. Delete Application
   ![delete application](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/fa76e4d2-1fb9-470e-adc9-7268dc8f5f30/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T133639Z&X-Amz-Expires=86400&X-Amz-Signature=1b63140fa0a2ff96acfe3b26c17cecb235cd5418813de6a655c2f7dbcaf356b4&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

2. Confirm delete application
   ![confirm del eb app](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/44ee8903-948b-4634-b645-4d1dd615e76d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T133700Z&X-Amz-Expires=86400&X-Amz-Signature=649a1d8531ec9500dfe49bf7ece1c5a6250a20a6c2b67a5098d032900ca86a14&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

3. Deleting in progress
   ![del eb app in progress](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c7cca2e7-f0b1-4d52-bc43-5d2aeb120325/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T133741Z&X-Amz-Expires=86400&X-Amz-Signature=2a3d04527101feab74c32d66301c48f658b3b466c26cb6ef4dd43834aff2e9fe&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   We need to wait for a while for elastic beanstalk to terminate everything, we can terminate other services such as cloudfront and S3 while waiting for the termination process to complete.

4. Deleted
   ![terminated eb app](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c8421a72-d00e-445d-96e4-17264a894d87/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T133851Z&X-Amz-Expires=86400&X-Amz-Signature=81cd2e4ecd6a35ead687fa806329c03d0cc0f36009af175461937e2ca230429c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

## Cloudfront

1. Disable Distribution
   ![disable distribution](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5ce361a4-f2d5-41ee-b356-d05f63de6981/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134003Z&X-Amz-Expires=86400&X-Amz-Signature=c9bbed73224021bd95c38eb81bbbcc10efd6d6d5957ae3c3b4184ed113c12291&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![confirm disable dist](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/395a0114-9bfa-4a8d-8bc6-36874ce56578/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134005Z&X-Amz-Expires=86400&X-Amz-Signature=c3e560489c329ba028944b566f0a12986f87f3a0c453a77f2dc459492bab1071&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   We would need to wait for around 5-15 minutes for it to disable completely before we are able to delete the distribution. Meanwhile, we can delete our S3 bucket.

2. Delete Distribution
   ![delete distribution](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4c9a952a-5bdb-47d7-95ea-cabe7de62fa5/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134113Z&X-Amz-Expires=86400&X-Amz-Signature=fdfe9d40ec794abdab86f470f34fc830e8a4e579fd314210f79bdaab2b9a899d&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![confirm delete dist](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/82e46646-da9a-4bdb-9b7e-4b15ce43ca23/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134144Z&X-Amz-Expires=86400&X-Amz-Signature=d93b7b4b835703e23b9a6dd92805abf17102fa96712a60074ac4d369d47c644c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
3. Deleted State
   ![deleted cloudfront](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a07b1b3a-67b0-4638-a2d9-c1afa4452b9f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134147Z&X-Amz-Expires=86400&X-Amz-Signature=2bb276fc7921a7a49d45a9deab796a2455aa806ecd94606b6d24b668e06b6781&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

## S3 Bucket
 
1. Empty Bucket
   ![empty bucket](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/16bd4742-fd98-4b05-ac52-65fd0ededf87/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134435Z&X-Amz-Expires=86400&X-Amz-Signature=a778f96c5f3f99593c53da17aa2a0e44e9e7bdacd819508c3817becd1cbe9a27&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   
   Enter bucket name to confirm deletion.
   ![enter name](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/fb1370e2-f054-44b4-9527-605106403dc5/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134456Z&X-Amz-Expires=86400&X-Amz-Signature=c078e326163541c174851a78d8bd27f5eadc806967f6e0ca076316fed4c407e6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

   Emptied bucket
   ![emptied bucket](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d5b508c7-5a32-4958-9d2a-a5fb35bf2871/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134655Z&X-Amz-Expires=86400&X-Amz-Signature=92149f98270a9e803a5d742380d8ad305f4f1284088b6c4e9dd29041290362ae&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
2. Delete Bucket
   ![delete bucket](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c5bcc8ea-11e4-499f-8faa-ee7ffa32bac1/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134717Z&X-Amz-Expires=86400&X-Amz-Signature=a5e44e521828ba756f6c8dd113d83bbba04b9df21ffa4356b4d934b3272a28e9&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   Enter bucket name to confirm deletion.
   ![enter bucket name](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/25ff71c5-249a-42f5-ac91-ca056584b736/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134719Z&X-Amz-Expires=86400&X-Amz-Signature=04c3dc32ad24f33b7bd467510a84d28d8ab22c13272b2632cb222418d46e2cc8&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
3. Deleted State
   ![deleted bucket](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/00df124b-a717-426e-9ca9-e0a1a07c39e5/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T134746Z&X-Amz-Expires=86400&X-Amz-Signature=1dc7893f87017d7618076bee96058deba540c84a16c8a1f82f2c4cde980b4cc0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)