# ![aws](https://github.com/julien-muke/Search-Engine-Website-using-AWS/assets/110755734/01cd6124-8014-4baa-a5fe-bd227844d263) Hosting a static website using Amazon S3 and AWS Amplify.


![aws_amplify_03](https://github.com/user-attachments/assets/ea0a31d5-0d5f-41a3-aa47-2a026410362f)


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

<a href="https://youtu.be/joP8nzHAKJI?si=TCLQqoX9aOsIEDZG" target="_blank"><img src="https://github.com/sujatagunale/EasyRead/assets/151519281/1736fca5-a031-4854-8c09-bc110e3bc16d" /></a>

## <a name="introduction">🤖 Introduction</a>

Static websites are an efficient and cost-effective way to deliver content to users, as they consist of pre-built HTML, CSS, and JavaScript files that require no server-side processing. Hosting such websites on AWS provides a scalable, reliable, and secure solution, leveraging the cloud provider's global infrastructure.

AWS offers multiple services to simplify static website hosting. Amazon S3 (Simple Storage Service) allows you to store and serve static files with high availability and minimal cost. AWS Amplify, a development and hosting platform, streamlines deployment and continuous integration for modern web applications. To ensure seamless access and custom domain management, Amazon Route 53, AWS's DNS service, plays a crucial role in routing user requests to your website.

In this guide, you'll learn how to use these AWS services together to host a static website. We'll cover:

1. Setting up a static website using Amazon S3 with public file hosting.
2. Deploying and managing your website using AWS Amplify.
3. Configuring custom domains and DNS routing with Amazon Route 53 to make your website accessible to the world.


## <a name="tech-stack">⚙️ Tech Stack</a>

- Amazon Amazon S3 (Simple Storage Service)
- AWS Amplify
- Amazon Route 53

## <a name="quick-start">🤸 Quick Start</a>

Before starting this guide, you will need:

**Prerequisites**

- Have an [AWS account](https://aws.amazon.com/)
- Static website source code (html, css and javascript) used in the video can be found [here](https://drive.google.com/drive/folders/1YZyObL5uVO5Yvwjb1M6BTp6OKIQ1ja10?usp=sharing)
- (Optional) Custom Domain with [Amazon Route 53](https://aws.amazon.com/getting-started/hands-on/get-a-domain/) or use a 3rd party domain registrar for example [Hostinger](https://www.hostinger.com/)


## <a name="steps">☑️ Steps</a>

The procedure for deploying this architecture on AWS consists of the following steps:

* Step 1. [Create a bucket](#create-a-bucket)
* Step 2. [Upload files to S3](#upload-files-to-s3)
* Step 3. [Create a new Amplify App](#create-a-new-amplify-app)
* Step 4. [Add a custom domain name with Amazon Route 53](#custom-doamin-with-route-53)


## <a name="create-a-bucket">➡️ Step 1 - Create a bucket</a>

To create a bucket

1. Sign in to the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3/.
2. Choose Create bucket.
3. Enter the Bucket name.
4. Choose the Region where you want to create the bucket.
5. Choose a Region that is geographically close to you to minimize latency and costs, or to address regulatory requirements. The Region that you choose determines your Amazon S3 website endpoint. For more information, see 
[Website endpoints](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteEndpoints.html).
6. Keep the default settings and create the bucket, choose Create bucket.

![Create-S3-bucket-S3-us-east-1-12-02-2024_05_39_PM](https://github.com/user-attachments/assets/c356382e-de3b-487f-8b3d-834dae15e754)


## <a name="upload-files-to-s3">➡️ Step 2 - Upload files to S3</a>

This procedure explains how to upload objects and folders to an Amazon S3 bucket by using the console.

To upload folders and files to an S3 bucket:

1. In the Buckets list, choose the name of the bucket that you want to upload your folders or files to, then click `View details`.

![Screenshot 2024-12-02 174053](https://github.com/user-attachments/assets/2762a2a1-e9b9-4718-b580-91ca49e54576)

2. Choose Upload.

![Screenshot 2024-12-02 174142](https://github.com/user-attachments/assets/6c1f0b44-f87b-44af-80ae-827c324fac21)

3. In the Upload window, Drag and drop files and folders to the Upload window.

![Screenshot 2024-12-02 174210](https://github.com/user-attachments/assets/ede3c609-5deb-4c12-ad4a-d8dbba0e27ab)

4. To upload your files, choose Upload.

Note: If you want the static website used in this tutorial, you can find the source code [here](https://drive.google.com/drive/folders/1YZyObL5uVO5Yvwjb1M6BTp6OKIQ1ja10?usp=sharing)

Amazon S3 uploads your files. When the upload completes, you can see a success message on the Upload status page.

![Screenshot 2024-12-02 174555](https://github.com/user-attachments/assets/e8975f02-f640-4b3f-87a0-369826b4a098)


## <a name="create-a-new-amplify-app">➡️ Step 3 - Create a new Amplify App</a>

If you done this in the past, you might know that to host your static website on Amazon S3 was just enable `static website hosting on S3` and you can still do that at least for now.

But now the recommendation is to go with amplify instead. There is a new way to host a static website on AWS, it includes S3 as well as amplify hosting. There have been some changes and very recently the recommendation changed to using amplify hosting instead of only S3.

Now, to host static website with AWS Amplify with content stored on S3:

1. From the Amazon S3 Console, click on `Properties` then scroll down to `static website hosting`
2. Click on `Create Amplify App`

![Screenshot 2024-12-02 174700](https://github.com/user-attachments/assets/9935edb8-27c2-4f77-8a83-3ed8fe8ca248)

3. That'll open up a new tab and take us to the amplify console and here it's basically created a new app for us it's linking it up to the the S3 bucket and all we have to do is save and deploy.

![Screenshot 2024-12-02 174754](https://github.com/user-attachments/assets/4da8656a-b9e4-48a4-96bd-fa459aa839a9)

Note: Amplify Hosting is a fully managed service that makes it easy to deploy your websites on a globally available content delivery network (CDN) powered by Amazon CloudFront, allowing secure static website hosting. 

![Screenshot 2024-12-02 174956](https://github.com/user-attachments/assets/d64ec4ab-ecb2-4500-9d04-929b0f16270f)

Note: Now, something that happened on the backend that you might not notice, unless you did this
in the past, is that if we go to the S3 bucket and click on permissions tab, then under bucket policy, you used to have to manually go enter a `policy` that would give access to the files in the bucket, otherwise you would get a permission denied error.

But we don't have to do that anymore with amplify, you'll see the policy got filled in automatically for us and we don't get any sort of access denied.

## <a name="custom-doamin-with-route-53">➡️ Step 4 - Add a custom domain name with Amazon Route 53</a>

Amazon Route 53 is a highly available and scalable DNS service. For more information, see Amazon Route 53 in the [Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html) Developer Guide.

If you already have a Route 53 domain, use the following [instructions](https://docs.aws.amazon.com/amplify/latest/userguide/to-add-a-custom-domain-managed-by-amazon-route-53.html) to connect your custom domain to your Amplify app.

If you are not using Amazon Route 53 to manage your domain, you can add a custom domain managed by a third-party DNS provider to your app deployed with Amplify (we'll use this option in this tutorial).

To add a custom domain managed by a third-party DNS provider:

1. Navigate to the Amplify console.
2. Choose your app that you want to add a custom domain to.
3. In the navigation pane, choose Hosting, Custom domains.
4. On the Custom domains page, choose Add domain.
5. Enter the name of your root domain. For example, if the name of your domain is `https://example.com`, enter `example.com`
6. Amplify detects that you are not using a Route 53 domain and gives you the option to create a hosted zone in Route 53.
7. Then choose Create hosted zone on Route 53, then click configure domain.

![Screenshot 2024-12-02 175942](https://github.com/user-attachments/assets/a2a85a9e-68e0-4179-b183-5c683d567c42)


To create a hosted zone in Route 53:

a. Choose Create hosted zone on Route 53.
<br>b. Choose Configure domain.
<br>c. Hosted zone name servers are displayed in the console. Go to your DNS provider's website and add the name servers to your DNS settings.


![Custom-Domains-Amplify-us-east-1-12-02-2024_06_00_PM](https://github.com/user-attachments/assets/88b6f8c4-3f96-4b61-8f88-3544bf0c6a31)

<br>d. Copy your name server and go to your third-party DNS provider's website and add the name servers to your DNS settings.

![Screenshot 2024-12-02 180224](https://github.com/user-attachments/assets/1765df42-1d0d-4b9c-834d-0659040dc0ad)

<br>d. Select I have added the above name servers to my domain registry.

7. By default, Amplify automatically creates two subdomain entries for your domain. For example, if your domain name is example.com, you will see the subdomains https://www.example.com and https://example.com with a redirect set up from the root domain to the `www` subdomain.

8. Choose the SSL/TLS certificate to use. You can either use the default managed certificate that Amplify provisions for you, or a custom third-party certificate that you have imported into AWS Certificate Manager.
9. Use the default Amplify managed certificate, Choose Amplify managed certificate.
10. Choose Add domain.

![Custom-Domains-Amplify-us-east-1-12-02-2024_06_03_PM](https://github.com/user-attachments/assets/2a17a441-267f-40ff-8200-a14d1e8a5ce9)

Amazon Amplify will create, configure the SSL certificate and activate your domain.


![Screenshot 2024-12-02 180415](https://github.com/user-attachments/assets/6e4cbf7a-f8f4-4f73-a4b4-bb5d2634c86e)


Once you domain is activated, Visit your custom domain to verify the website is accessible.

![Screenshot 2024-12-02 181606](https://github.com/user-attachments/assets/f44e1145-0cf3-46e9-a7a0-14d427aaef59)


## Conclusion

By following these steps, you can efficiently host a static website on AWS using Amazon S3, AWS Amplify, and Amazon Route 53, ensuring scalability, reliability, and a professional user experience.

## 💰 Cost

All services used are eligible for the AWS Free Tier. However, charges will incur at some point so it's recommended that you shut down resources after completing this tutorial.