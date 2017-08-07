# PurpleBox WordPress site on AWS

This tutorial walks through creating your own WordPress site through PurpleBox's AMI in Amazon Web Services. PurpleBox's WordPress AMI is a preconfigured Amazon Linux image that runs WordPress with a MySql database.

This tutorial assumes you already have an AWS account and are relatively comfortable on the command line. If you experience any difficulties or have any feedback, please leave a comment.

## Getting Started

First we will need to create our own security group for public and administrator access to the site. Log in to your AWS console and navigate to the EC2 dashboard. In the EC2 dashboard, under network and security, click security groups and create security group.

![security group](https://user-images.githubusercontent.com/29229030/29010951-4182702e-7afd-11e7-9c79-09f88cd47bf1.PNG)

Next we will create a security group allowing HTTP, HTTPS, and SSH.

![security group02](https://user-images.githubusercontent.com/29229030/29010744-7735293e-7afb-11e7-8ed0-8e4464e80776.PNG)

Note: The security group created is the default webserver security group and is open to anyone. It is recommended to limit the SSH source to known IP addresses only.

## Launching Your Instance

Now it is time to launch your WordPress instance. In the EC2 dashboard, under instances, click launch instance.

![instance](https://user-images.githubusercontent.com/29229030/29010925-0b62a252-7afd-11e7-970e-7c80afa884d4.PNG)

In the community AMIs, search for PurpleBox WordPress.

![instance 02](https://user-images.githubusercontent.com/29229030/29011081-39f6d808-7afe-11e7-8fed-67e4110aebdc.PNG)

Select the image and follow through the initial steps of the startup wizard using settings based on your needs.

In "Step 6: Configure Security Group", choose select an existing security group and click on the webserver security group we created previously.

Review and launch the instance. When prompted, choose create a new key pair and save that file somewhere safe. This private key will allow you to securely SSH into your instance.

In a couple minutes your WordPress instance should be running. Once you see that the status checks have finished, copy the public DNS that is in the description of your instance and run it in your browser. This domain name will take you to the WordPress installation page where you can get started in creating your own WordPress site!

![wordpress](https://user-images.githubusercontent.com/29229030/29011516-b17389a0-7b01-11e7-9d5b-9e8002d3cb37.PNG)

## Additional Information

You can access your instance via SSH using the default Amazon Linux username 'ec2-user' and the Amazon private key you created in the previous steps.

### Database Credentials
Database Name: wordpressdb

Database Username: root

Database Password: password





 


