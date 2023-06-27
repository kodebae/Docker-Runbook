# 📒 The Docker Runbook
A place for Docker tutorials, learning, examples, and an overall resource guide. 

## Intro
---
**Docker is a platform** that allows developers to easily develop, deploy, and run applications in a containerized environment. Docker containers are lightweight, flexible, and can be run on any operating system. They allow developers to package an application with all of its dependencies into a single, portable container, ensuring that the application runs consistently in any environment. This makes it easier to manage and deploy applications, as well as streamline the development process. 

What is Docker? Docker is a virtualization software that makes developing and deploying applications much easier. Docker packages all necessary dependencies, libraries, configuration, system tools and runtime into a container. Which can be easily shared and distributed.

While **monolithic architecture** is a single, tightly-integrated unit, microservices are made up of loosely-coupled, independently deployable components. Microservices allow for better scalability, flexibility and maintainability, but require additional complexity in communication and orchestration between services.

On the other hand, **microservices** represent a way of building applications where components are small, independent and communicate through simple APIs. Each microservice is responsible for a specific business capability and works as a separate, independent component. This allows for easy scaling and modification of individual services without affecting the functionality of other services.

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


## Docker Examples
---

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
[Cloud Native Interactive Landscape](landscape.cncf.io/?fullscreen=yes)


