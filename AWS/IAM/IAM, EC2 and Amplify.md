# IAM 
- IAM stands for  Identity and Access Management.
- It helps you securely control access to AWS resources.
- Never use root account to access aws services.


  ![image](https://user-images.githubusercontent.com/85761276/217570412-0cf27020-afca-4271-8a61-6dde3a0f3dd3.png)


# IAM Users
![image](https://user-images.githubusercontent.com/85761276/217572801-e2274c62-b574-4552-a176-7a267ecab0ec.png)

### When you create an IAM user, they can't access anything in your account until you give them permission. 
# Policies and groups
  ![image](https://user-images.githubusercontent.com/85761276/217573366-41aa4fcb-7ddf-439e-beac-6995596ef59a.png)


- Example: S3 bucket policies - Specify who can access objects stored in an Amazon S3 bucket.
- Policies in AWS are written in JSON format
- here is an example of Admistrator Access Policy <br/>

  ![image](https://user-images.githubusercontent.com/85761276/217576110-56bb67ed-e768-4b27-9743-8cfd4ba38b68.png)
  
 ## Difference between Root user and IAM user
  ![image](https://user-images.githubusercontent.com/85761276/217576660-10b2c1df-f5e4-4351-8dd3-621cb85c977c.png)


# EC2
## What is EC2
![image](https://user-images.githubusercontent.com/85761276/217580582-4d7e21c2-d491-4d74-9f6c-e928c2b72381.png)

-  Provides scalable computing capacity.
-  You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage.

## Features of EC2
- Virtual computing environments, known as instances
- Preconfigured templates for your instances, known as Amazon Machine Images (AMIs)
- CPU, memory, storage, and networking capacity for your instances
- firewall 
- Regions and Availability Zones
- Secure login information for your instances using key pairs
- Elastic IP addresses

## How to Configure an Instance
- Open EC2 Console <br/>
 ![image](https://user-images.githubusercontent.com/85761276/217580996-4568ec9c-1854-4c90-a8d6-b565eec6795e.png)
 
 - Choose AMI <br/>
  ![image](https://user-images.githubusercontent.com/85761276/217581314-44256a00-b046-441c-b903-52fe0ed1682b.png)

- Select Instance type <br/>
  ![image](https://user-images.githubusercontent.com/85761276/217581472-da37b5f0-c4aa-4bad-aa23-639cac4a193a.png)

- Create a Key pair <br/>
  ![image](https://user-images.githubusercontent.com/85761276/217581750-5e2fdb77-397c-4f1c-a635-704f61533fa9.png)

- Create security groups or select the existing ones <br/>
  ![image](https://user-images.githubusercontent.com/85761276/217582073-1565bca2-9d32-4dc1-aea9-2c2ecb4f8f84.png)

- Configure storage <br/>
  ![image](https://user-images.githubusercontent.com/85761276/217582212-0475622b-47b2-4b46-9e2c-e0d330b46b99.png)

- Finally, launch the instance <br/>
  ![image](https://user-images.githubusercontent.com/85761276/217582679-624512da-cf2e-4eff-b320-33946e5c6376.png)

- You can ssh into the instance using MobaXtem or CMD
  ![image](https://user-images.githubusercontent.com/85761276/217588224-be8e9c5c-0a7f-4bff-a8d7-c621dcca8505.png)

  ![image](https://user-images.githubusercontent.com/85761276/217589758-23a55cbb-bfbe-45d0-aefb-821b014dbd48.png)


 # Amplify
  ![image](https://user-images.githubusercontent.com/85761276/217583772-21088010-d1c2-40b7-be43-43182e0b287b.png)

## What is AWS Amplify
- AWS Amplify is a set of purpose-built tools and features that enables frontend web and mobile developers to quickly and easily build full-stack applications on AWS. 

# Hosting a Static Website

## Step 1

![image](https://user-images.githubusercontent.com/85761276/205229517-06dbe654-3fa7-4452-a7f2-d4329348e947.png)

- npx create-react-app amplifyapp
- cd amplifyapp
- npm start


## Step 2 - Creating a repo

[Created this repo](https://github.com/zainabmirkar/amplify_react_app)

## Step 3
Initialize git and push the application to the new GitHub repo

- git init
- git add README.md
- git commit -m "first commit"
- git branch -M main
- git remote add origin url
- git push -u origin main


## Step 4 - To connect your repository, log in to the Amplify Console and choose Get Started at the top of the page then Get Started under Amplify Hosting.

## Step 5
  ![image](https://user-images.githubusercontent.com/85761276/205230367-61a493f7-63f3-4235-aa6e-cde262af82be.png)

## Step 6 - Configure build settings

  ![image](https://user-images.githubusercontent.com/85761276/205230505-10578ebd-79d5-419f-95bf-505b6a43dcf5.png)

## Step 7 - Save and Deploy

  ![image](https://user-images.githubusercontent.com/85761276/205231392-171b6231-920f-4828-b5da-b3c9be42bef9.png)


<br/>

#### Reference
https://aws.amazon.com/getting-started/hands-on/host-static-website/?ref=gsrchandson
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html
https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html
 
 
 
 
 
 
