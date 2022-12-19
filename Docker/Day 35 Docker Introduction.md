## What is a container?

- a container is a sandboxed process on your machine that is isolated from all other processes on the host machine. 
- is a runnable instance of an image. You can create, start, stop, move, or delete a container using the DockerAPI or CLI.
- can be run on local machines, virtual machines or deployed to the cloud.
- is portable (can be run on any OS).
- is isolated from other containers and runs its own software, binaries, and configurations.
- Since the image contains the container’s filesystem, it must contain everything needed to run an application - all dependencies, configurations, scripts, binaries, etc.


## What is Dockerfile?
- A Dockerfile is simply a text-based file with no file extension. 
- A Dockerfile contains a script of instructions that Docker uses to create a container image.

## Docker commands
![image](https://user-images.githubusercontent.com/85761276/208483917-bba694e9-fc9d-401b-8d28-8c888370ea32.png)

![image](https://user-images.githubusercontent.com/85761276/208484024-f4b225c3-256e-4176-a857-80219f82cedf.png)


- You use the -d flag to run the new container in “detached” mode (in the background). 
- You also use the -p flag to create a mapping between the host’s port 3000 to the container’s port 3000. 
- Without the port mapping, you wouldn’t be able to access the application.

- After that you will be able to view your application

![image](https://user-images.githubusercontent.com/85761276/208484225-c389e77a-0a42-4402-95f8-76fc0b5dadea.png)

- docker dashboard

![image](https://user-images.githubusercontent.com/85761276/208484329-a94957ec-56cf-4c19-8061-c374434063ad.png)

![image](https://user-images.githubusercontent.com/85761276/208493682-a986729b-44d1-4f13-ae5d-ee1dea11d8c3.png)

### to delete all the container and images
- docker system prune -a 

- docker rm myapp

#### Reference
https://docs.docker.com/get-started/02_our_app/
