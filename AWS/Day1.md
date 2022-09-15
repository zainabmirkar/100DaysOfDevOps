
# Jenkins master slave setup on EC2 instance

<img width="960" alt="Day1aws" src="https://user-images.githubusercontent.com/85761276/188203957-9d2c635b-a5e9-496b-9252-b813ebb5d438.png">

1) After signing in to the the AWS Management Console.
2) Open the Amazon EC2 console by selecting EC2 under Compute. From the Amazon EC2 dashboard, Launch Instance.
3) Select Amazon Linux AMI. Choose an Instance Type page, the t2.micro instance.
4) Also I have created a new security group and key pair. Review the changes and launch the instance.
5) Using SSH to connect to my instance and then downloading and installing Jenkins.<br/>
    <img width="539" alt="3" src="https://user-images.githubusercontent.com/85761276/188211239-9d45dcc7-de09-44b4-8737-9116678b3740.png">

7) Configured slave on master instance in the same exact way.<br/>
    <img width="624" alt="4" src="https://user-images.githubusercontent.com/85761276/188211661-2f4e3f61-d952-4533-a94d-1fb1763ffd11.png">
   
Reference:
https://www.jenkins.io/doc/tutorials/tutorial-for-installing-jenkins-on-AWS/

# Installation of Tomcat on AWS EC2 linux & integration with Jenkins

steps are the same as above <br/>

<img width="799" alt="2" src="https://user-images.githubusercontent.com/85761276/188209712-fb690ad6-3587-466f-8a6b-5efef60b3b89.png"><br/>

<img width="664" alt="5" src="https://user-images.githubusercontent.com/85761276/188211974-dd8cf850-d24c-49ef-b496-9f6ca45d3651.png"> <br/>

Reference:
https://devops4solutions.com/installation-of-tomcat-on-aws-ec2-linux-integration-with-jenkins/

Also, this is not a detailed explanation of each and every step. Please do read the references for more information.

