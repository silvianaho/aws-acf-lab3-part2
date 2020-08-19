---
layout: default
title: Elastic Beanstalk Setup
nav_order: 2
permalink: /elastic_beanstalk/
parent: Step by Step Guide
---

# Elastic Beanstalk Setup

1. Create Elastic Beanstalk Application
   * Navigate to Elastic Beanstalk on AWS Console and click on `Create Application`
   ![create app](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4f5866b5-b15e-4b45-b639-7d9240e4de8c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T082147Z&X-Amz-Expires=86400&X-Amz-Signature=7f819c36fcfbb7305e79a4d5f0bd223a0dc4981e1c7befff1113dbb9b7746ace&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

   * Name the Elastic Beanstalk application and add a tag (optional)
   ![name](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a162ab17-05ab-4ab6-a852-a95cefb21c04/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T082242Z&X-Amz-Expires=86400&X-Amz-Signature=0b06ec36afd4a83f9a0d7c28230b1f77497c7e2e82f45f1dbd8d183bebfd7cc5&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

   * Select platform version and sample application code (we are going to deploy our server from code pipeline later on). Press `Create Application` and wait for the application to deploy.
   ![platform](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7f274a56-c6fd-426f-97b1-6cea126c9f75/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T082330Z&X-Amz-Expires=86400&X-Amz-Signature=95f43f411f2e5ed63d8ff33ca9a53f1b577547caf07e01f2d81c3bb15ae06e7c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

   * This is how it looks like after a successful deployment
   ![deploy success](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/39782556-1a96-47d3-a271-0c8bcd005e97/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T082512Z&X-Amz-Expires=86400&X-Amz-Signature=ef5a0b5af030387e051f88d5084b679843e53301c0cf6acd71bea8a748d0ca95&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

2. Add Elastic Load Balancing and Auto Scaling Group to Elastic Beanstalk Environment
   * Navigate to `Configuration`, scroll down to the `Capacity` category and press the `Edit` button.
   ![capacity config](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/67215b66-2280-4170-bba2-1eb9c65d8f93/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T082548Z&X-Amz-Expires=86400&X-Amz-Signature=350997d381ba2e09fb9a7d074c2bc653c465cf1c69a94fe8572174e90274cff0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   
   * Modify the `Environment Type`, `Number of Instances`, `Instance Type`, `Availability Zones`, and `Scaling Triggers`
   ![env type, instances](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/16881739-5189-4988-a239-dbfce30e5ee6/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T082816Z&X-Amz-Expires=86400&X-Amz-Signature=831a1c1da0d87074d75abb0d58f1a9d8a413d4763fd6561f3a2d15d9b03a5a1c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![type, az](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/75cc5eed-ed49-4ddc-a1d9-834662ba33d5/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T082846Z&X-Amz-Expires=86400&X-Amz-Signature=ac25b566f50dd278774d7386c23ad3b49fda9dd5f15c7ef18083c345353e78e1&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![triggers](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/0732ee37-e305-40df-8752-81df95b0429d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T082935Z&X-Amz-Expires=86400&X-Amz-Signature=af00084c844c1f25dcb22b483336f2c6daca0267ccffe0c9a556ce19f08167bd&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Read the warning message and `Confirm`
   ![warn confirm](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ae6961d4-4cd7-48f3-9992-0e009d1d8b3f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T083059Z&X-Amz-Expires=86400&X-Amz-Signature=98154451e2e836aedb8d76870958d434b616c191e61dd42eeab2bf2a951ce4a0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

   * Wait for the application to deploy again.

3. Add an Amazon RDS Database to Elastic Beanstalk Environment
   * After a successful deployment, navigate to `configuration`, scroll down to `Database` category, and `Edit`
   ![edit database](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/db3f44a1-5c6c-4b31-b241-e955951fbb46/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T083412Z&X-Amz-Expires=86400&X-Amz-Signature=cd99d6d774a0d7e8fbcdb99c28e89c2bf2e03efdf5c509b9dbece79c53fe1a5b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Modify database configurations as needed. In our case, since our website is relatively small, we are using a `MySQL` database engine with `db.t2.micro` instance class and 5GB storage.
   ![engine](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/808b22b6-884c-4319-8143-f1c14f44bee5/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T083517Z&X-Amz-Expires=86400&X-Amz-Signature=77971b20dbb10c44ef437121c505f3c17620cb9d7c68dc0e7a361fd76016c5f6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   Set a username and password to log into our database engine, change the availability to high, and click `Apply`.
   ![username pw](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/66f7836c-63e8-4358-b18c-f9a01f367d5a/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T083522Z&X-Amz-Expires=86400&X-Amz-Signature=6f2804ea0a0f29bb878c2677df5f0c707534146a5de3b6e64aae4e01e8fa11f4&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   
4. Connect to DB Instance
   We need these to connect our Node.js server to our database.
   * After another successful deployment, we can navigate back to `Configuration`. Scroll down to `Database` category again and click on the endpoint that has been created.
   ![endpoint](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/00a99b2f-460b-4d79-b1f3-8d9c31855ace/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T084642Z&X-Amz-Expires=86400&X-Amz-Signature=746a783eebcb0a1dbef984ba95adf3dd6bb7da825ff0370a2241b8c75edefc15&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * The endpoint will lead us to Amazon RDS Console. On the RDS console, click on our newly created database.
   ![new db](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7d875637-bba3-4709-aae8-7a3f6ebb3e7b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T084727Z&X-Amz-Expires=86400&X-Amz-Signature=65d447ee6692f65c6d3aa5f47c222b23d98c59141a5a349728acd60bcc8dffb7&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Click on the security group and a new tab will open and take us to the security group.
   ![sec group](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5b69c357-b29b-4313-9752-53bb3aaae579/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T085859Z&X-Amz-Expires=86400&X-Amz-Signature=9663137606c6c3d92bb1522975dd3f12f462f7dce143e66e2615ab2b79815daf&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Edit Inbound Rule to allow all TCP connections from our network (My IP).
   ![inbound rule](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ed5eb683-bf35-4740-9da5-a1a13bc367fb/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T105845Z&X-Amz-Expires=86400&X-Amz-Signature=3599a9e6a006a3bb1e4e83a7c6a8b67ba451548daac04d683b0636aa47050933&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ![tcp rules](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5744be5c-85d3-4340-93b1-8618e6b3460c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T105943Z&X-Amz-Expires=86400&X-Amz-Signature=cf482ee20715afa474cb3731e881fbde9e0a9e447b3d0ac61f6c89b9c026bfed&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

5. Create Table
   We are going to use MySQL Workbench to connect to our RDS Database.
   * Create Connection
   ![create conn](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/34197653-6d16-4bda-9fab-51c0ac4b3b79/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T110008Z&X-Amz-Expires=86400&X-Amz-Signature=3ff4a55f2ec11e3c8b488f4ec36c28f51001b74bc0bcd73ffb0782247d044c14&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Key in our `RDS endpoint` on the `host` field and input our RDS `username` and `password`. (Optional) The default schema is `ebdb` (this is created by default). Click `OK` and wait for connection to be eastablished.
   ![credentials](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/316d489b-faa5-410b-8e9c-29748ee9ea32/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T110137Z&X-Amz-Expires=86400&X-Amz-Signature=e62689a8f81e85b3fbf9188e43dd53ed749184aab6cd2dcea2d0676a5c1fbd08&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Once we are connected, we can create a table in our database.
   ![create table](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c9ff02b4-27b0-4620-93d3-1a20afccc1da/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T110635Z&X-Amz-Expires=86400&X-Amz-Signature=01642755499ab6726eb979804ac5274fe4742a6a62be23dedb6b7968e4795c9d&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   ```sql
    USE ebdb;
    CREATE TABLE IF NOT EXISTS 
	listings (
		id INT NOT NULL, 
        title VARCHAR(255) NOT NULL, 
        description VARCHAR(255) NOT NULL, 
        price DOUBLE PRECISION NOT NULL, 
        category INT NOT NULL);
   ```

6. Set Environment Variables
   Now, let's set our environment variable because we need the database credentials in order for our nodejs server to connect to our database.
   * Navigate to `Configuration` > `Software` > `Edit`
   ![edit software](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/cd709c31-6bbf-4628-a5af-17867dd06d54/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T111939Z&X-Amz-Expires=86400&X-Amz-Signature=a18775d2fbfd04b53793b03972e3511ba4464a30b696d6c80e3017d63d21f268&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Key in the following fields according to your database configuration and click apply
   ![environment vars](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2ef02cb2-3a7d-471a-bcd5-389542dd3d31/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T112036Z&X-Amz-Expires=86400&X-Amz-Signature=d8f0fce91c17637542c35682a914eb906f905ac6583909f09790d2487fed5829&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
   * Wait until environment change is fully deployed and move on to the next step ([setting up code pipeline](/aws-acf-lab3-part2/code_pipeline))
   ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/afc606ef-fff7-4662-ab33-5d58b65833db/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200819%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200819T112123Z&X-Amz-Expires=86400&X-Amz-Signature=5ef087b842156cb2ca098aeed508e7f659b62626c7e8bf212458fa7f1e53291b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)