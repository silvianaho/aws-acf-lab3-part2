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
   ![code pipeline](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6363f3f9-0d96-41f3-999a-4a15d17d3701/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T112722Z&X-Amz-Expires=86400&X-Amz-Signature=3489c2e45d53a9ee5ef0907dd4ed6fa58961fb09902029de6e6cce967d43fcbd&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Give it a name!
   ![pipeline name](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ab9a3548-4548-4200-95aa-c15200f820a5/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T112816Z&X-Amz-Expires=86400&X-Amz-Signature=99b6c54a6aafbffb74ee96783d9fa0b5200875cb289694f439d3e3ae487a93b5&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * We are using Github as a version control for our application. Hence, we are chose github as the source and connected our github account. Then, we selected the correct repository and branch.
   ![source](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2064b117-0261-41f4-a933-1ad84c5286d8/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T112840Z&X-Amz-Expires=86400&X-Amz-Signature=2d917a1f45c81643e291b3d4c6c510edd60b39a9e34a2d0f6468d60f584124c8&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Skip build stage because we are going to build our applications locally
   ![skip build](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/49074dca-f5f9-4dd2-b32e-9789006927df/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T113020Z&X-Amz-Expires=86400&X-Amz-Signature=f31bd68a2ad8cc8a35ec684fb5fa5d458b46b31a8e2128ea4ef0aa1a1781c9ce&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Choose Elastic Beanstalk as the deploy provider and choose the application and environment we created earlier
   ![deploy](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e040ffc1-914f-4e51-aded-7e4d86d252d0/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T113103Z&X-Amz-Expires=86400&X-Amz-Signature=0fc42a1b81395b608e813dac8a31421f30929493bfc667dd5b86e00337824231&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Review and create the pipeline
   ![review and create](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/9ceb5524-6376-4af8-8a78-a3cde340f3bf/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T113149Z&X-Amz-Expires=86400&X-Amz-Signature=6b155dd6b3c17faa967b3c2130d8164eabe5411437e1f2187c39808299ea8ccd&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Wait for the application to deploy for the first time
   ![deploy](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6b067420-12fe-4f5a-9f01-afba8da373b4/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T113307Z&X-Amz-Expires=86400&X-Amz-Signature=a78d67d6b3dfd2a4e47d4353115c39c38e139ed6db2426e7a798a4c24c49e3e8&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

2. Deploy Application via CodePipeline
   Once you've made changes to your code, stage, commit and push to github.
   ![add commit push](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/3120b8f4-0210-4be5-b447-bad5ea836d0a/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T113918Z&X-Amz-Expires=86400&X-Amz-Signature=75f790f664ace37db038432b106a3e2cc6c4e4bef5d343a9b81e1e33c7a0fba7&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   Then, CodePipeline will automatically pick up that there are changes and deploy the application to elastic beanstalk.
   ![codepipeline deploy](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/79d90bf9-4ace-4b2a-ad5a-791ab9fec641/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T114034Z&X-Amz-Expires=86400&X-Amz-Signature=1ca20f6f7edfebb47cf061eea861369685bfeb6ecef181c60eb56ab83d2fa2ed&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

3. View Application
   There are different ways to access our server, two of them are through Elastic Beanstalk Environment Endpoint or Postman.
   ![eb endpoint](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/770aa555-1172-40b0-a454-779762c172d8/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T114414Z&X-Amz-Expires=86400&X-Amz-Signature=e5eb7e926ac0a55b691083f88608877aee8cc4f601d0019dd278098a69141a51&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![image](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/dd660e79-9750-4a99-8ba2-2a6acdda97a8/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T114117Z&X-Amz-Expires=86400&X-Amz-Signature=42dd534ab0ef86aee579712dab824ead35d031dc621c3715f549447fea46643c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   
4. Inserting Data from Postman
   ![postman](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/11066443-cdea-4d32-9fa9-6b3b83a46fa9/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T114619Z&X-Amz-Expires=86400&X-Amz-Signature=bbf64148618bd144a3a3a9bbb9ea10b3aa0ac63177cc5388d3501084b2885d9f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   Result:
   ![result](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/667576b0-6ded-4008-b90f-40f5d705e332/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T114809Z&X-Amz-Expires=86400&X-Amz-Signature=6d0f9eeffc4dc34c35bed85f82fd352f886e7ca0bb8168d5e8760cd6c76f0f73&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)