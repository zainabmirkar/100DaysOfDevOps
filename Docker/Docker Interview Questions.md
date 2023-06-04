- What is Docker, and how does it differ from virtualization? <br/>
  - Docker is an open-source platform that allows you to automate the deployment, scaling, and management of applications using containerization.
It provides an isolated environment called a container that packages the application and its dependencies, making it portable across different environments.
Docker differs from traditional virtualization in that it does not require a full operating system to be emulated. Instead, Docker containers share the host system's kernel, making them lightweight, fast to start, and efficient in resource utilization compared to virtual machines.
  - Instead, Docker containers share the host system's kernel, making them lightweight, fast to start, and efficient in resource utilization compared to virtual machines.




- What is a hypervisor?
  - A hypervisor, also known as a virtual machine monitor (VMM), is software or firmware that enables the creation and management of virtual machines (VMs) on a physical host machine.
  - It allows multiple operating systems (guests) to run concurrently on a single physical server.
  - The primary function of a hypervisor is to abstract and virtualize the underlying hardware resources, such as CPU, memory, storage, and network interfaces. 
  - It provides an interface between the physical hardware and the virtual machines, allowing the guest operating systems to run independently as if they were running directly on the hardware.
  - type 1 and type 2 
  - type 1 example is Xen 
  - type 2 is vmware workstation and virtualbox


- Explain the concept of containerization.

  - Containerization is the process of encapsulating an application and its dependencies into a standardized unit called a container. 
  - Containers provide an isolated and consistent environment for running applications, ensuring that they run reliably across different systems and environments. 
  - They package the application, libraries, and dependencies together, making it easy to deploy, manage, and scale applications without worrying about compatibility issues.


- What are the advantages of using Docker?
  - Portability: Docker containers are lightweight and can run consistently across different platforms and environments.
  - Scalability: Docker enables easy scaling of applications by allowing the creation of multiple instances of containers.
  - Isolation: Containers provide process-level isolation, ensuring that applications run independently without interfering with each other.
  - Efficiency: Docker containers share the host system's kernel, resulting in efficient resource utilization and faster startup times.
  - Reproducibility: Docker allows you to define the entire application stack and dependencies in code, making it easy to reproduce the exact same environment across different systems.


- What is a Docker image? How is it different from a Docker container?
  - A Docker image is a read-only template that contains the application, its dependencies, and other files needed to run the application. 
  - It is built using a Dockerfile, which specifies the instructions to create the image.
  - A Docker container is a running instance of an image. It is created from an image and can be started, stopped, and managed independently. 
  - Multiple containers can be created from the same image, each running as an isolated process.


- What are Docker Volumes?
  - Docker volumes are a way to persist and share data between Docker containers and the host machine.
  - https://github.com/zainabmirkar/100DaysOfDevOps/blob/main/Docker/Day%2036%20Docker%20Volumes.md
  
- What is a Dockerfile
  - dockerfile contains the instructions for building a container
  - It contains the base image reqired to build the application
  - command to be run when the application starts
  - install packages information
  - It is used with the docker build command to generate a Docker image that can be run as a container.


- How can you share data between containers in Docker?
  - Using Docker volumes: Containers can mount the same volume, allowing them to read and write data to a shared location.
  
  
- What is Docker Compose, and how does it simplify container orchestration?
  -Docker Compose is a tool that allows you to define and manage multi-container applications using a declarative YAML file. 
  - It simplifies container orchestration by providing a convenient way to define the configuration, dependencies, and networking of multiple containers as a single application stack. 
  - Docker Compose automates the container creation, startup, and intercommunication, making it easier to deploy and manage complex applications.


- What is Docker Swarm?
  - Docker Swarm is a native clustering and orchestration solution provided by Docker. 
  - It allows you to create and manage a swarm of Docker nodes (hosts) to run and scale containerized applications across multiple machines.



- What is the purpose of a Docker registry?
  - A Docker registry is a central repository for storing and distributing Docker images. It allows users to share and access images from anywhere. Docker
  - Hub is the default public registry, but private registries can be set up for internal use or to store proprietary images.



# Dockerfile questions

- what is cmd?
  - It specifies what command should be executed when the container starts
  - Only the last CMD instruction in the Dockerfile is effective. If multiple CMD instructions are provided, the last one will be used.
  - The CMD instruction is often used to define the default behavior of the container, such as running a specific command or starting the main application.


- What is Entrypoint?
  - The ENTRYPOINT instruction sets the primary command or executable that should be executed when the container starts.
It provides a fixed starting point for the container and cannot be overridden by command-line arguments.
  - Note: If both CMD and ENTRYPOINT are specified in the same Dockerfile, the CMD arguments will be appended to the ENTRYPOINT command.
  - The key difference between CMD and ENTRYPOINT is that CMD can be overridden by providing command-line arguments when running the container, while ENTRYPOINT cannot be overridden.
  
- What is ADD?
  ```ADD http://example.com/file.tar.gz /app/```
  - The file file.tar.gz is downloaded from the URL http://example.com/file.tar.gz and placed in the /app/ directory.

- Difference between add and copy?
  -  the COPY instruction is generally recommended over ADD for copying local files or directories, as it has simpler syntax and doesn't perform any automatic unpacking or retrieval of remote URLs. 
  -  ADD should be used when you specifically need its additional features.





