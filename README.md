# ![aws](https://github.com/julien-muke/Search-Engine-Website-using-AWS/assets/110755734/01cd6124-8014-4baa-a5fe-bd227844d263) Hosting a static website using Amazon S3 and AWS Amplify.


![Blank diagram-19](https://github.com/user-attachments/assets/1d4fa91d-2efd-46f8-b8c4-bbd834f4dbfc)

<div align="center">

<h3 align="center">How to Host a static website using Amazon S3 and AWS Amplify</h3>

   <div align="center">
     Build this hands-on demo step by step with my detailed tutorial on <a href="http://www.youtube.com/@julienmuke/videos" target="_blank"><b>Julien Muke</b></a> YouTube. Feel free to subscribe 🔔!
    </div>
</div>

## 🚨 Tutorial

This repository contains the steps corresponding to an in-depth tutorial available on our YouTube
channel, <a href="http://www.youtube.com/@julienmuke/videos" target="_blank"><b>Julien Muke</b></a>.

If you prefer visual learning, this is the perfect resource for you. Follow my tutorial to learn how to build projects
like these step-by-step in a beginner-friendly manner!

<a href="https://youtu.be/HcqDrF-k7bc?si=vc-ViXgOG4B7IOEl?feature=shared" target="_blank"><img src="https://github.com/sujatagunale/EasyRead/assets/151519281/1736fca5-a031-4854-8c09-bc110e3bc16d" /></a>

## <a name="introduction">🤖 Introduction</a>

Deploying a WordPress website on AWS involves leveraging various AWS services to ensure scalability, reliability, and security. In this guide, we will walk you through the process of setting up a WordPress site using Amazon EC2 for hosting, Amazon RDS for database management, and Amazon Application Load Balancer (ALB) for efficient traffic distribution.

Additionally, we will utilize Amazon Route 53 for domain name management and DNS routing. This comprehensive approach not only simplifies the deployment process but also equips your WordPress site with the robust infrastructure needed to handle varying levels of traffic, ensuring optimal performance and uptime.


## 📐 Architecture Diagram Overview

* Users will request to open WordPress website, that request will be received by Route 53 which is a domain Management Service in AWS.
* We will use Route 53 to host DNS entries of the website's domain.
* Route 53 will send request to Application Load Balancer (ALB), it handles distribution of the traffic, if you have multiple instances of the same website, it will handle all the incoming requests. 
* ALB also support SSL certificate through AWS Certificate Manager, we will use it to issue a new SSL certificate for our domain name and ALB will apply that SSL certificate and send request to EC2 instance.
* EC2 instance is a virtual server where we will install all the needed packages to run WordPress  and create files of our WordPress website.
* We will make EC2 and RDS accessible to public source and enforce security via Security Group rules.
* We will create an EC2 instance which will be our Virtual Server and RDS instance which will be used for Database Hosting.

## <a name="tech-stack">⚙️ Tech Stack</a>

- Amazon EC2
- Amazon Application Load Balancer (ALB)
- Amazon RDS
- Amazon Route 53
- AWS Certificate Manager
- WordPress


## <a name="steps">☑️ Steps</a>

The procedure for deploying this architecture on AWS consists of the following steps:

* Step 1. [Create EC2 for WordPress](#create-ec2-for-wordpress)
* Step 2. [Connect to EC2 instance via Instance connect](#connect-ec2-to-instance)
* Step 3. [Connect to EC2 instance via SSH client (local Terminal)](#connect-ec2-to-ssh)
* Step 4. [Install Apache on Amazon Linux 2](#install-apache)
* Step 5. [Install PHP & MariaDB on Amazon Linux 2](#install-php-mariadb)
* Step 6. [Download the latest WordPress zip file](#download-wordpress)
* Step 7. [Create RDS instance for WordPress website](#rds-wp)
* Step 8. [Connect RDS and EC2 instance](#connect-rds-ec2)
* Step 9. [WordPress Installation on Amazon Linux 2 EC2 instance](#install-wp-on-ec2)

## <a name="create-ec2-for-wordpress">➡️ Step 1 - Create EC2 for WordPress</a>



## 💰 Cost

All services used are eligible for the AWS Free Tier. However, charges will incur at some point so it's recommended that you shut down resources after completing this tutorial.