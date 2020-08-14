---
layout: default
title: Alternative Solution
nav_order: 4
permalink: /alternative_solution/
parent: Solutions
---
# Alternative Solution and Comparisons

Our team used Visual Studio Code to build and edit the codes of our website instead of using AWS Cloud9 as our IDE so that our solution to our problem statement would be more cost effective as Visual Studio Code is a free IDE to use. Other than that, the team is more familiar with the Visual Studio Code environment which makes building the website faster and more efficient.

WordPress is a versatile Content management system (CMS) that enables several users to build and operate a website without knowledge of coding. Although much simpler to configure than an HTML site, it would be more challenging managing and maintaining a WordPress site. We do not have to worry about plugin compatibility or site maintenance for the HTML website. However, since we require a developer to make some improvements, we have no control over the site. Therefore, we chose to use S3 instead of WordPress.

To optimize the time to deliver the data, we used Amazon CloudFront to serve the static contents.

With Elastic Beanstalk, you can quickly deploy and manage applications in the AWS Cloud without having to learn about the infrastructure that these applications run. Elastic Beanstalk reduces the complexity of management without restricting choice or control. Simply upload the code, and Elastic Beanstalk automatically manages the details of capacity provisioning, load balancing, scaling and device safety monitoring.  

Compared to a 3-Tier Architecture, each tier executes a specific task and may be controlled independently of each other. This allows development teams more flexibility by allowing them to update the essential aspects of the application independently of the other parts. This additional flexibility will increase total time and shorten development cycle times by supplying development teams with the flexibility to replace or upgrade different independent tiers without impacting other areas of the system.
