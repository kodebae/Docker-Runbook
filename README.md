# 📒 The Docker Runbook
---
A place for Docker tutorials, learning, examples, and an overall resource guide. 

<img align="center" alt="Coding" width="1200" src="https://media.giphy.com/media/Ab2UG9MKeRyYrERcyC/giphy.gif">

## Intro
---
**Docker is a platform** that allows developers to easily develop, deploy, and run applications in a containerized environment. Docker containers are lightweight, flexible, and can be run on any operating system. They allow developers to package an application with all of its dependencies into a single, portable container, ensuring that the application runs consistently in any environment. This makes it easier to manage and deploy applications, as well as streamline the development process. 

**What is Docker?** Docker is a virtualization software that makes developing and deploying applications much easier. Docker packages all necessary dependencies, libraries, configuration, system tools and runtime into a container. Which can be easily shared and distributed.

With containers you don't have to install any of the services directly onto your operating system.

While **monolithic architecture** is a single, tightly-integrated unit, microservices are made up of loosely-coupled, independently deployable components. Microservices allow for better scalability, flexibility and maintainability, but require additional complexity in communication and orchestration between services.

On the other hand, **microservices** represent a way of building applications where components are small, independent and communicate through simple APIs. Each microservice is responsible for a specific business capability and works as a separate, independent component. This allows for easy scaling and modification of individual services without affecting the functionality of other services. The service gets packaged into one isolated environment. Docker standardized the process of running any service on any local dev environment.

**Docker IS NOT a virtual machine.** Docker will virtualize the application layer and use the Kernel of the host. It doesn't have it own Kernel. A virtual machine has it's own Kernel and also uses the application layer. Docker image files are much smaller. Docker containers takes seconds,not minuets.

### Microservices Risks
| It's important to note that microservices come with their own risk factors preinstalled.
- unnecessarily complexity
- changes impact numerous services
- complex security
- complexity is added to resolve complexity issues
- testing might appear simpler, but usually isn't
- deployment may appear simpler, but usually isn't
- multiple databases
- latency issues may be added via the API layer. So additional testing is required
- Transient errors, implement retry strategies to fix this
- multiple points of failure can occur instead of SPoF

### Microservices Benefits
| There are also plenty of benefits preinstalled into microservices as well.
- improved fault isolation, less risk of single points of failure
- eliminate vendor or technology lock-in
- easy to understand
- smaller and faster to deploy
- scalability

## Basics
---
1.  What is a Docker Image?
- An executable application artifact. This includes the app source code and complete environment configuration. You can add the environment variables, create directories, files, etc.
- Immutable template that defines how a container will be realized. 
- You can run multiple containers from 1 image.

2. What is a Docker Container?
- The container actually starts the application.
- A running instance of an image is a Docker container.

3. How do we get Docker Images?
- A storage and distribution system, the Docker registry.
- [Official Docker Hub](https://hub.docker.com/search?image_filter=official&q=)
- Docker Registry has "official images" that are maintained and developed by a team.
- Docker Hub is the default location that Docker will check to locate any image.

4. Image versioning, also known as image tags?
- What happens if my technology updates? A new Docker image will be created.
- When you need a specific version of a technology you can choose the Docker image of the corresponding version. 
- Latest tag is the latest version of the technology. If you don;t choose a version specifically you get the latest version of the technology. 

## Docker Examples
---
When we install docker we get access to Docker in our CLI. 
### List of Docker CLI Commands
```
docker images
```
- gives a list of available Docker images
```
docker ps
```
- gives a list of currently running containers
```
docker logs 089e2423ff48
```
- the docker logs command plus the container id will give you the logs from the service running in your contianer

### How to pull an image from Docker Hub
1. locate the image you want to pull
2. find the tag you need, select a specific version
3. execute the commmand with image name and version tag seperated by a colon 
``` 
docker pull image:0.14
```
### How to run an image
1. execute the commmand with image name and version tag seperated by a colon
```
docker run image:0.14
```
- add -d tag before image name to run the container detached and in the background.
```
docker run -d image:0.14
```
- to exit the process 'ctrl + c' will kill the contianer and the process will die. 
- if you execute the run command without pulling the image first Docker will automatically search for, pull, then run the image specified.
```
docker stop
```
- stops all running containers

## Files
---
A Dockerfile is a plain text file that contains instructions used to build a Docker image. The structure of a Dockerfile consists of a series of instructions, each on a new line. Here is a breakdown of the Dockerfile structure:

**Base image:** The first line of the Dockerfile specifies the base image to be used. It defines the starting point for the build process. For example, FROM ubuntu:latest selects the latest version of Ubuntu as the base image.

**Maintainer:** The MAINTAINER instruction allows you to specify the author or maintainer of the image. It is an optional field.

**Environment variables:** You can set environment variables using the ENV instruction. These variables are accessible during build time and when the container is running.

**Working directory:** The WORKDIR instruction sets the working directory for any following instructions. It is similar to the cd command.

Copy files: The COPY and ADD instructions copy files and directories from the build context (the current directory) to the container's filesystem.

Executing commands: The RUN instruction executes commands in the container during the build process. Multiple RUN instructions can be chained together.

Exposing ports: The EXPOSE instruction documents the ports that the container listens on at runtime. It does not actually publish the ports.

Entry point: The ENTRYPOINT instruction specifies the command that will be executed when the container runs as an executable. It is often used in combination with the CMD instruction.

Container metadata: Additional metadata about the image can be added using the LABEL instruction.

Container user: The USER instruction specifies the user context for any subsequent commands such as RUN, CMD, or ENTRYPOINT.

Execution context: The CMD instruction provides a default command to run when the container starts. It can be overridden by specifying a command during the docker run command.

These instructions can be combined in any order to create a Dockerfile that accurately reflects the desired configuration of the image.

## Code
---
- code snippet example:
```
FROM ubuntu:latest

RUN apt-get update && apt-get install -y nginx

COPY index.html /usr/share/nginx/html/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]

```

## Do's and Dont's
---
DO:
- use the same port on your host that your container is using
---
DONT:

---

### Cloud Native
---
Uses containers, service meshes, microservices, immutable infrastructure, and declarative API's. Cloud-native refers to an approach to developing and running applications that takes full advantage of the cloud computing delivery model. Cloud-native applications are architected specifically to run optimally in the dynamic and distributed environments that are characteristic of modern cloud infrastructure. These applications are designed to be highly scalable, resilient, and automated, with a focus on maximizing efficiency, agility, and flexibility. Key characteristics of cloud-native applications include the use of containerization, microservices architecture, and DevOps practices, along with a focus on continuous integration and delivery (CI/CD) and infrastructure as code (IaC).

#### Cloud Native Concepts
| Application Architechture
- clean code
- domain driven design
- microservices principles
- kubernetes patterns

## Video Archive
---
- [FCC Docker & K8S Training Course](https://youtu.be/kTp5xUtcalw)
- [virtual machines vs containers](https://youtu.be/eyNBf1sqdBQ)
- [1hr Docker Crash Course](https://www.youtube.com/watch?v=pg19Z8LL06w)

## Additional Resources
---
- [Docker Docs](https://docs.docker.com)
- [Cloud Native Interactive Landscape](landscape.cncf.io/?fullscreen=yes)