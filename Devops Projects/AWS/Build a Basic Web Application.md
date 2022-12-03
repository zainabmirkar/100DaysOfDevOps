# Build a Basic Web Application 


  ![image](https://user-images.githubusercontent.com/85761276/205435567-ab20f576-7b31-4918-ac8d-a5a228e5ab68.png)


## Module 1 - Deploy static resources for your web application using the AWS Amplify Console.
- static web content - including HTML, CSS, JavaScript, images, and other files - will be hosted by AWS Amplify. 
- Create index.html and ZIP (compress) only the HTML file.

  ![image](https://user-images.githubusercontent.com/85761276/205436211-5fae32c6-ed8d-4c92-b1f8-1ffb90395b7b.png)
  
-  log into the Amplify console. Get Started section, under Host your web app, choose the orange Get started button.
-  Select Deploy without Git provider.

  ![image](https://user-images.githubusercontent.com/85761276/205436287-241e1304-90d8-479c-ab4c-bf6cdd06c3fd.png)
- Choose the Save and deploy button.


  ![image](https://user-images.githubusercontent.com/85761276/205436375-c0def317-3b96-4341-86c4-580712b60933.png)


 ## Module 2 - Build a serverless function using AWS Lambda

- Create a lambda function.
- Under Code source, replace the code in index.js with the following:
  ![image](https://user-images.githubusercontent.com/85761276/205437189-14758fc2-d675-431c-b13b-c7e80cb2250c.png)
- Choose the Deploy option, then Test
- Under Event name, enter HelloWorldTestEvent. Copy and paste the following JSON object to replace the default one:
  ![image](https://user-images.githubusercontent.com/85761276/205437237-22433b1a-dd54-48aa-a9bd-d8c660cc7216.png)
- Choose the Save button to create the test event.
- Choose the orange Test button again to run the test event. The result will be displayed in the Execution results section of the code editor.

  ![image](https://user-images.githubusercontent.com/85761276/205437271-524eda36-9dd8-4ac4-be4c-91367963e62c.png)
  
  #### Now we have a working Lambda function.

## Module 3 - Deploy serverless function using Amazon API Gateway

##### Amazon API Gateway helps developers to create and manage APIs to back-end systems running on Amazon EC2, AWS Lambda, or any publicly addressable web service.

![image](https://user-images.githubusercontent.com/85761276/205444652-4f15cb75-3525-451d-9c84-165afade76a6.png)

![image](https://user-images.githubusercontent.com/85761276/205444706-da619b46-3d9c-484b-aa41-fe27b407d2bf.png)

![image](https://user-images.githubusercontent.com/85761276/205444761-5b54bc77-3fca-4b57-9256-c96464b4affb.png)


![image](https://user-images.githubusercontent.com/85761276/205444881-c68dc137-b94e-4237-a82e-c4a3bc63ac8d.png)

![image](https://user-images.githubusercontent.com/85761276/205444919-b6b9e010-310c-4549-a7cc-aceccd272af4.png)


## Module 4 - Creating an Amazon DynamoDB table and enabling Lambda function to store data in it

![image](https://user-images.githubusercontent.com/85761276/205445330-4c21a4e0-63fd-4859-ba50-1c90694ef849.png)

![image](https://user-images.githubusercontent.com/85761276/205445782-42f3ebaa-1df2-49e2-9465-bf73eda2767e.png)

![image](https://user-images.githubusercontent.com/85761276/205446035-6204bc71-7821-470e-ad22-83b112190cd8.png)

![image](https://user-images.githubusercontent.com/85761276/205446111-9d24739b-30b0-4515-a9bd-77132e54bffb.png)

##### We added two services in this module: DynamoDB (for storage) and IAM (for managing permissions securely). Both are connected to our Lambda function, so that it can write to our database.


## Module 5 - Adding Interactivity to my Web App

![image](https://user-images.githubusercontent.com/85761276/205446466-e79d52bf-b9a4-4e3c-b719-06e97e8f41f6.png)

![image](https://user-images.githubusercontent.com/85761276/205446543-7d44c8a4-d550-4872-8aff-503c7bb97b3d.png)

![image](https://user-images.githubusercontent.com/85761276/205446579-dd73eae0-f068-450e-b1fb-6beecc838023.png)



#### Reference 
https://aws.amazon.com/getting-started/hands-on/build-web-app-s3-lambda-api-gateway-dynamodb/















