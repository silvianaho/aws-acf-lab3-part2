---
layout: default
title: Code Pipeline Setup
nav_order: 3
permalink: /code_pipeline/
parent: Step by Step Guide
---

# Code Pipeline Setup

1. Create CodePipeline
   * Navigate to CodePipeline on AWS Console and click on create pipeline
   ![code pipeline](../../assets/cp/1.png)
   * Give it a name!
   ![pipeline name](../../assets/cp/2.png)
   * We are using Github as a version control for our application. Hence, we are chose github as the source and connected our github account. Then, we selected the correct repository and branch.
   ![source](../../assets/cp/3.png)
   * Skip build stage because we are going to build our applications locally
   ![skip build](../../assets/cp/4.png)
   * Choose Elastic Beanstalk as the deploy provider and choose the application and environment we created earlier
   ![deploy](../../assets/cp/5.png)
   * Review and create the pipeline
   ![review and create](../../assets/cp/6.png)
   * Wait for the application to deploy for the first time
   ![deploy](../../assets/cp/7.png)

2. Deploy Application via CodePipeline
   Once you've made changes to your code, stage, commit and push to github.
   ![add commit push](../../assets/cp/9.png)
   Then, CodePipeline will automatically pick up that there are changes and deploy the application to elastic beanstalk.
   ![codepipeline deploy](../../assets/cp/10.png)

3. View Application
   There are different ways to access our server, two of them are through Elastic Beanstalk Environment Endpoint or Postman.
   ![eb endpoint](../../assets/cp/12.png)
   ![image](../../assets/cp/11.png)
   
4. Inserting Data from Postman
   ![postman](../../assets/cp/13.png)
   Result:
   ![result](../../assets/cp/15.png)