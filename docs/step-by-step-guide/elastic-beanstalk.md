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
   ![create app](../../assets/eb/1.png)

   * Name the Elastic Beanstalk application and add a tag (optional)
   ![name](../../assets/eb/2.png)

   * Select platform version and sample application code (we are going to deploy our server from code pipeline later on). Press `Create Application` and wait for the application to deploy.
   ![platform](../../assets/eb/3.png)

   * This is how it looks like after a successful deployment
   ![deploy success](../../assets/eb/4.png)

2. Add Elastic Load Balancing and Auto Scaling Group to Elastic Beanstalk Environment
   * Navigate to `Configuration`, scroll down to the `Capacity` category and press the `Edit` button.
   ![capacity config](../../assets/eb/5.png)
   
   * Modify the `Environment Type`, `Number of Instances`, `Instance Type`, `Availability Zones`, and `Scaling Triggers`
   ![env type, instances](../../assets/eb/6.png)
   ![type, az](../../assets/eb/7.png)
   ![triggers](../../assets/eb/9.png)
   * Read the warning message and `Confirm`
   ![warn confirm](../../assets/eb/10.png)

   * Wait for the application to deploy again.

3. Add an Amazon RDS Database to Elastic Beanstalk Environment
   * After a successful deployment, navigate to `configuration`, scroll down to `Database` category, and `Edit`
   ![edit database](../../assets/eb/12.png)
   * Modify database configurations as needed. In our case, since our website is relatively small, we are using a `MySQL` database engine with `db.t2.micro` instance class and 5GB storage.
   ![engine](../../assets/eb/13.png)
   Set a username and password to log into our database engine, change the availability to high, and click `Apply`.
   ![username pw](../../assets/eb/14.png)
   
4. Connect to DB Instance
   We need these to connect our Node.js server to our database.
   * After another successful deployment, we can navigate back to `Configuration`. Scroll down to `Database` category again and click on the endpoint that has been created.
   ![endpoint](../../assets/eb/15.png)
   * The endpoint will lead us to Amazon RDS Console. On the RDS console, click on our newly created database.
   ![new db](../../assets/eb/16.png)
   * Click on the security group and a new tab will open and take us to the security group.
   ![sec group](../../assets/eb/17.png)
   * Edit Inbound Rule to allow all TCP connections from our network (My IP).
   ![inbound rule](../../assets/eb/18.png)
   ![tcp rules](../../assets/eb/19.png)

5. Create Table
   We are going to use MySQL Workbench to connect to our RDS Database.
   * Create Connection
   ![create conn](../../assets/eb/20.png)
   * Key in our `RDS endpoint` on the `host` field and input our RDS `username` and `password`. (Optional) The default schema is `ebdb` (this is created by default). Click `OK` and wait for connection to be eastablished.
   ![credentials](../../assets/eb/21.png)
   * Once we are connected, we can create a table in our database.
   ![create table](../../assets/eb/22.png)
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
   ![edit software](../../assets/eb/23.png)
   * Key in the following fields according to your database configuration and click apply
   ![environment vars](../../assets/eb/24.png)
   * Wait until environment change is fully deployed and move on to the next step ([setting up code pipeline](/aws-acf-lab3-part2/code_pipeline))
   ![](../../assets/eb/25.png)