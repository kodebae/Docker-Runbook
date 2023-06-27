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
- unnecessary complexity
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
- [Official Docker Registry](https://hub.docker.com/search?image_filter=official&q=)

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


## Files
---

## Code
---

## Do's and Dont's
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
[FCC Docker & K8S Training Course](https://youtu.be/kTp5xUtcalw)
[virtual machines vs containers](https://youtu.be/eyNBf1sqdBQ)
[1hr Docker Crash Course](https://www.youtube.com/watch?v=pg19Z8LL06w)

## Additional Resources
---
[Docker Docs](https://docs.docker.com)
[Cloud Native Interactive Landscape](landscape.cncf.io/?fullscreen=yes)



