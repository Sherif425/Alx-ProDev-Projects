# Project: Containerization with docker | Cairo Intranet


#### Overview

Containerization is a lightweight form of virtualization that allows developers to package applications and all their dependencies into a single, consistent unit called a **container**. **Docker** is the most popular platform for building, running, and managing containers. It provides a way to ensure that an application runs reliably across different environments—whether on a developer’s local machine, in testing, staging, or in production.

With Docker, developers can isolate application processes, simplify deployment pipelines, and reduce the “it works on my machine” problem. Containers are fast, portable, and scalable, making them ideal for **microservices architectures**, **CI/CD pipelines**, and **cloud-native development**.

#### Learning Objectives

By the end of this, you will be able to:

-   Understand the concept of containerization and how it differs from traditional virtualization.
-   Install Docker and configure it in a development environment.
-   Build, run, and manage Docker containers using the CLI and Dockerfiles.
-   Create custom Docker images and understand image layers.
-   Use Docker Compose to orchestrate multi-container applications.
-   Integrate Docker into the development workflow to streamline testing and deployment.
-   Understand the role of containers in modern DevOps and CI/CD pipelines.

#### Learning Outcomes

After completing this, you should be able to:

-   Explain how Docker containers encapsulate an application and its environment.
-   Build Docker images using a `Dockerfile`.
-   Run and manage containers using basic Docker commands.
-   Use Docker Compose to define and run multi-container applications.
-   Apply best practices in writing Dockerfiles for efficient and secure containers.
-   Deploy containerized applications consistently across multiple environments.
-   Understand how Docker supports scalability and fault tolerance in cloud-based infrastructure.

#### Best Practices for Using Docker in Development

🛠️ Practice

💡 Description

**Keep images small**

Use minimal base images (like `alpine`) and remove unnecessary files to reduce image size and attack surface.

**Use multi-stage builds**

Separate build and runtime environments in Dockerfiles to optimize final image size.

**Tag images properly**

Always tag your images with version numbers or meaningful identifiers (avoid just `latest`).

**Leverage .dockerignore**

Similar to `.gitignore`, it prevents unnecessary files from being included in your images.

**Run as non-root user**

Avoid running applications in containers as root for security reasons.

**Externalize configuration**

Use environment variables or bind mounts to separate config from code.

**Avoid hardcoding secrets**

Never store passwords, tokens, or secrets in Dockerfiles or images—use secret managers instead.

**Use health checks**

Define `HEALTHCHECK` instructions to ensure container health monitoring.

**Clean up unused resources**

Regularly run `docker system prune` to free up space and remove unused containers/images.

**Use volumes for persistent data**

Containers are ephemeral; use Docker volumes to retain important data between runs.

#### Relevance in Modern Development

Docker has become a cornerstone technology in modern software development due to its:

-   **Consistency across environments**: Docker ensures “build once, run anywhere.”
-   **Rapid onboarding**: Developers can spin up dev environments quickly with containers.
-   **Seamless integration into CI/CD**: Docker supports automation from build to deployment.
-   **Portability**: Containers can run on any platform that supports Docker (local, server, or cloud).
-   **Support for microservices**: Docker simplifies deployment and scaling of services independently.
-   **Simplified dependency management**: All dependencies are bundled in the image.

**Requirements:**

-   Docker
    
-   This project is building upon the messaging app built in week 4. If you have not done that project, kindly go back
    
-   Operating system: ubuntu 20.20
    

#### 📝 Project Assessment (Hybrid)

Your project will be evaluated primarily through **manual reviews**. To ensure you receive your full score, please:

✅ Complete your project on time  
📄 Submit all required files  
🔗 Generate your review link  
👥 Have your peers review your work

An **auto-check** will also be in place to verify the presence of core files needed for manual review.

##### ⏰ Important Note

If the deadline passes, you won’t be able to generate your review link—so be sure to submit on time!

We’re here to support your learning journey. Happy coding! ✨

##### Quiz questions

**Great!** You've completed the quiz successfully! Keep going! (Show quiz)

##### Question #0

In Kubernetes, what is the smallest deployable unit that can host containers?

-   Service
    
-   ReplicaSet
    
-   Pod
    
-   Node
    

---

##### Question #1

What is the main function of Docker Compose?

-   To define and run multi-container Docker applications
    
-   To build Docker images from source code
    
-   To manage Docker images across multiple servers
    
-   To automate rolling updates of Docker containers
    

---

##### Question #2

What role does a Kubernetes service play in a containerized application?

-   It defines how pods are exposed to the network
    
-   It handles authentication for container access
    
-   It stores and manages container images
    
-   It orchestrates the deployment of containers across nodes
    

---

##### Question #3

What is the primary purpose of Docker in the context of application development?

-   To automate the deployment of software updates
    
-   To provide a cloud service for hosting applications
    
-   To create virtual machines for applications
    
-   To containerize applications along with their dependencies for consistent deployment
    

---

##### Question #4

What command in Kubernetes is used to scale the number of pods in a deployment?

-   kubectl scale deployment
    
-   kubectl rollout restart
    
-   kubectl create pod
    
-   kubectl expose service
    

---

##### Question #5

Which Kubernetes deployment strategy involves running two versions of an application simultaneously, then switching traffic to the new version when it’s ready?

-   Canary Deployment
    
-   Blue-Green Deployment
    
-   Rolling Update
    
-   Horizontal Scaling
    

---

##### Question #6

In Docker, what is the difference between an image and a container?

-   A container is a template for creating images
    
-   An image can be deployed across multiple servers, while containers are limited to one server
    
-   An image is a running instance of a container
    
-   A container is a running instance of an image
    

## Tasks

##### 0\. set up a docker environment

mandatory

Score: 80.0% (Checks completed: 80.0%)

**Objective:** containerize the [Buliding Robust APIs](/rltoken/SiQL-dz-MyEcsutBmEkUZg "Buliding Robust APIs")

**Instructions:**

-   Create a `Requirements.txt` file and freeze all the dependencies in it. [Hint](/rltoken/4L62-fkmy1Np0deYehQBXg "Hint")
    
-   Install docker for linux. Wondering how, read [here](/rltoken/z0LQRtWUvAXeISbOHIJT_g "here").
    
-   Create a `Dockerfile` in the root of your messaging app project.
    
-   Set up the `Dockerfile` to:
    
    -   Use a base Python image `python:3.10`.
    -   Install necessary dependencies from the `requirements.txt`.
    -   Copy your app code into the container.
    -   Expose the port your Django app runs on (default is 8000).
-   Build the Docker image using the `docker build` command.
    
-   Run the image in a container and ensure the app works correctly
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/Dockerfile`

Check submission Mark submission : in progress... : an error occurred View results

##### 1\. Use Docker Compose for Multi-Container Setup

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective**: Learn how to manage multiple services using Docker Compose.

**Instructions:**

-   Create a `docker-compose.yml` file at the root of your messaging\_app
    
-   Define two services:
    
    -   `web`: for your Django messaging app.
    -   `db`: for a MySQL database.
-   Set up the `db` service with environment variables (such as `MYSQL_USER, MYSQL_DB, MYSQL_PASSWORD`).
    
-   Configure the `settings.py Database variable` to connect to the MYSQL database service using environment variables. [hint](/rltoken/12_WVkM48URMbO_tmc9RnA "hint")
    
-   Use `Docker Compose` to build and run the multi-container setup.
    
-   Verify that the app can interact with the MYSQL database.
    

Nb: do not push your environment variables to github. Ensure they are in a .env file

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/docker-compose.yml`

Check submission View results

##### 2\. Persist Data Using Volumes

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Understand how to use Docker volumes to persist database data.Understand how to use Docker volumes to persist database data.

**Instructions:**

-   Modify the `docker-compose.yml` file to add a volume for the MYSQL service, ensuring that the database data is persisted across container restarts.

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/docker-compose.yml`

Check submission View results

##### 3\. Manual Review

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
