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
