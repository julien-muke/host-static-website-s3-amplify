# ![aws](https://github.com/julien-muke/Search-Engine-Website-using-AWS/assets/110755734/01cd6124-8014-4baa-a5fe-bd227844d263) Hosting a static website using Amazon S3 and AWS Amplify.


![aws_amplify_02](https://github.com/user-attachments/assets/eb6d99d0-9d13-43d8-b361-8284cc9cff84)


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

Static websites are an efficient and cost-effective way to deliver content to users, as they consist of pre-built HTML, CSS, and JavaScript files that require no server-side processing. Hosting such websites on AWS provides a scalable, reliable, and secure solution, leveraging the cloud provider's global infrastructure.

AWS offers multiple services to simplify static website hosting. Amazon S3 (Simple Storage Service) allows you to store and serve static files with high availability and minimal cost. AWS Amplify, a development and hosting platform, streamlines deployment and continuous integration for modern web applications. To ensure seamless access and custom domain management, Amazon Route 53, AWS's DNS service, plays a crucial role in routing user requests to your website.

In this guide, you'll learn how to use these AWS services together to host a static website. We'll cover:

1. Setting up a static website using Amazon S3 with public file hosting.
2. Deploying and managing your website using AWS Amplify for a streamlined CI/CD pipeline.
3. Configuring custom domains and DNS routing with Amazon Route 53 to make your website accessible to the world.


## <a name="tech-stack">⚙️ Tech Stack</a>

- Amazon Amazon S3 (Simple Storage Service)
- AWS Amplify
- Amazon Route 53

## <a name="quick-start">🤸 Quick Start</a>

Before starting this guide, you will need:

**Prerequisites**

- [Create an AWS account](https://aws.amazon.com/)
- Static website source code (html, css and javascript) used in the video can be found [here]()
- Custom Domain with [Amazon Route 53](https://aws.amazon.com/getting-started/hands-on/get-a-domain/) or use a 3rd party domain registrar for example [Hostinger](https://www.hostinger.com/)


## <a name="steps">☑️ Steps</a>

The procedure for deploying this architecture on AWS consists of the following steps:

* Step 1. [Create a bucket](#create-a-bucket)
* Step 2. [Create a new Amplify App](#create-a-new-amplify-app)
* Step 3. [Add a custom domain name with Amazon Route 53](#custom-doamin-with-route-53)


## <a name="create-a-bucket">➡️ Step 1 - Create a bucket</a>





## 💰 Cost

All services used are eligible for the AWS Free Tier. However, charges will incur at some point so it's recommended that you shut down resources after completing this tutorial.