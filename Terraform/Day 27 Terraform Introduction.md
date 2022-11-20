# Terraform

# What is terraform provider?
Terraform relies on plugins called providers to interact with cloud providers, SaaS providers, and other APIs.


# Terraform commands
- terraform init - The terraform init command initializes a working directory containing Terraform configuration files. This is the first command that should be run after writing a new Terraform configuration or cloning an existing one from version control.
- terraform destroy - It is a convenient way to destroy all remote objects managed by a particular Terraform configuration.


- terraform plan - The terraform plan command creates an execution plan, which lets you preview the changes that Terraform plans to make to your infrastructure. <br/>



   ![image](https://user-images.githubusercontent.com/85761276/202907017-a71419d6-487b-41a1-98f7-016ba411fac1.png)


- terraform apply - When you run terraform apply without passing a saved plan file, Terraform automatically creates a new execution plan as if you had run terraform plan, prompts you to approve that plan, and takes the indicated actions. 

   ![image](https://user-images.githubusercontent.com/85761276/202907318-589d5a1a-4cb9-4c1e-b56f-4d371c6a4005.png)

    Successfully deployed ec2 instance using terraform. <br/>
    
    
    
     
## If you made a change in your main.tf file then the current deployment will be updated.
   ![image](https://user-images.githubusercontent.com/85761276/202908017-75253f70-2674-4922-b246-67d049be6eda.png)
   
   ![image](https://user-images.githubusercontent.com/85761276/202908049-cec9b0af-f948-44ac-ac23-8d0f5fcefff5.png)

<br/>

# Referencing resources
   ![image](https://user-images.githubusercontent.com/85761276/202909429-db94f42f-a708-4c0f-8794-ef90a24d6cc7.png)

   
   ![image](https://user-images.githubusercontent.com/85761276/202909054-730f22cd-5b67-4804-8c79-4e6685d27d92.png)
    vpc created <br/>
    
   ![image](https://user-images.githubusercontent.com/85761276/202909130-c3f983a4-9305-4c89-869a-f95d978383bf.png)
   
   



    
