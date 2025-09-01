# Project: Jenkins and Github Actions | Cairo Intranet

#### **Overview**

This project focuses on setting up a **Continuous Integration and Continuous Deployment (CI/CD)** pipeline for a Django-based messaging application. The pipeline includes:  
\- **Jenkins** for automated testing, Docker image building, and pushing to Docker Hub.  
\- **GitHub Actions** for running tests, linting checks, code coverage, and Docker image deployment.  
\- **Docker** for containerizing the Django application.

The goal is to automate testing, ensure code quality, and streamline deployment processes.

#### **Learning Objectives**

By completing this project, you will learn how to:  
1\. **Set up Jenkins in Docker** and configure a pipeline for automated testing and Docker builds.  
2\. **Integrate GitHub Actions** to run tests, linting, and code coverage checks.  
3\. **Build and push Docker images** using both Jenkins and GitHub Actions.  
4\. **Secure sensitive credentials** (GitHub, Docker Hub) using Jenkins credentials and GitHub Secrets.  
5\. **Automate workflows** to trigger on code pushes and pull requests.

#### **Key Concepts**

1.  **Continuous Integration (CI)** – Automatically running tests and checks on every code change.  
    
2.  **Continuous Deployment (CD)** – Automating Docker image builds and deployments.  
    
3.  **Containerization** – Using Docker to package the application for consistent deployment.  
    
4.  **Pipeline as Code** – Defining Jenkins and GitHub Actions workflows in YAML/Jenkinsfile.  
    
5.  **Code Quality & Testing** – Using `pytest`, `flake8`, and coverage reports.  
    

#### **Tools & Libraries**

Category

Tools/Libraries

**CI/CD**

Jenkins, GitHub Actions

**Testing**

pytest, Coverage

**Linting**

flake8

**Containerization**

Docker, Docker Hub

**Version Control**

GitHub

**Database**

MySQL (for testing)

#### **Real-World Use Case**

This setup mirrors real-world DevOps workflows where:  
✔ **Developers push code** → **Automated tests run** → **Code quality is checked** → **Docker image is built & deployed**.  
✔ **Teams ensure stability** before merging changes.  
✔ **Deployments become faster and more reliable** using containerization.

This project helps in understanding **CI/CD best practices**, which are widely used in **startups and large-scale applications** to maintain high-quality software delivery.

### **Next Steps**

-   Extend the pipeline with **Kubernetes deployment**.  
    
-   Add **security scanning** (e.g., Snyk, Trivy).  
    
-   Implement **rolling updates** for zero-downtime deployments.  
    

### 📝 Project Assessment (Hybrid)

Your project will be evaluated primarily through **manual reviews**. To ensure you receive your full score, please:

✅ Complete your project on time  
📄 Submit all required files  
🔗 Generate your review link  
👥 Have your peers review your work

An **auto-check** will also be in place to verify the presence of core files and specific workflows needed for manual review.

##### ⏰ Important Note

If the deadline passes, you won’t be able to generate your review link, so be sure to submit on time!

We’re here to support your learning journey. Happy coding! ✨

##### Quiz questions

**Great!** You've completed the quiz successfully! Keep going! (Show quiz)

##### Question #0

Which file is typically used to define a Travis CI pipeline?

-   `Dockerfile`
    
-   `ci-config.yaml`
    
-   `Jenkinsfile`
    
-   `.travis.yml`
    

---

##### Question #1

What is a “stage” in a Jenkins pipeline?

-   A distinct step in the CI/CD pipeline that represents a specific action (e.g., build, test, or deploy)
    
-   A server that manages Jenkins jobs
    
-   A container for storing build artifacts
    
-   A repository branch for merging changes
    

---

##### Question #2

What is the benefit of using separate environments for development, staging, and production in a CI/CD pipeline?

-   To reduce the cost of cloud resources
    
-   To prevent the need for testing
    
-   To isolate bugs and test fixes in non-production environments
    
-   To simplify the build process
    

---

##### Question #3

What is the main purpose of Continuous Integration (CI) in a CI/CD pipeline?

-   To ensure code changes are automatically tested and integrated into the main branch
    
-   To track changes in the deployment environment
    
-   To automate production deployments
    
-   To create a backup of the source code
    

---

##### Question #4

What is a typical use case for setting up alerts and feedback loops in a CI/CD pipeline?

-   To notify developers of build failures or test issues
    
-   To create backups of the repository
    
-   To automatically scale the number of servers in production
    
-   To track the number of commits made by each developer
    

---

##### Question #5

Which command in GitHub Actions is used to define a workflow file for automated testing and deployment?

-   `pipeline {}`
    
-   `on: [push, pull_request]`
    
-   `kubectl apply`
    
-   `stages {}`
    

---

##### Question #6

Which of the following best describes Jenkins?

-   A container orchestration tool for managing Docker containers
    
-   A version control system for managing source code
    
-   A tool for managing cloud resources
    
-   An open-source automation server used for implementing CI/CD pipelines
    

## Tasks

##### 0\. Install Jenkins and Set Up a Pipeline:

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** install Jenkins in a docker container and set up a pipeline that pulls the source code from GitHub, runs tests using pytest, generates a test report, and triggers the pipeline manually.

\*_Instructions: \*_

-   Run `jenkins` in a docker container by executing the following command

```
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v 
jenkins_home:/var/jenkins_home jenkins/jenkins:lts
```

-   This command will:
    
    -   Pull the latest Long-Term Support (LTS) Jenkins image.
    -   Expose Jenkins on port `8080`.
    -   Map the Jenkins home directory to the host machine to persist data.
-   Access Jenkins dashboard by visiting `http://localhost:8080` in your browser and follow the instructions to set up and configure Jenkins
    
-   Install the `git plugin, Pipeline and ShiningPandaPlugin`. Hint
    
-   Create a `Jenkinsfile` pipeline script that pulls the messaging app’s code from GitHub, installs dependencies, runs tests using `pytest`, and generates a report
    
-   Ensure to add Credentials for GitHub
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/Jenkinsfile`

Check submission View results

##### 1\. Build Docker image with Jenkins

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** building a Docker image for your Django messaging app using Jenkins

**Instructions:**

-   Extend the Jenkins Pipeline Script `Jenkinsfile` to add stages for building and pushing the Docker image
    
-   After updating the Jenkinsfile in your GitHub repository, go to the Jenkins dashboard and trigger the pipeline manually by clicking on `Build Now`.
    
-   Monitor the build logs to verify that the Docker image is built and pushed to Docker Hub successfully.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/Jenkinsfile`

Check submission View results

##### 2\. Set Up a GitHub Actions Workflow for Testing

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Set up github actions for Testing

**Instructions:**

-   Create a `.github/workflows/ci.yml` file in your messaging app’s repository.
    
-   Configure a GitHub Actions workflow that runs the Django tests on every push and pull request.
    
-   Ensure the workflow installs necessary dependencies and sets up a MySQL database for running tests (e.g., using `services` in GitHub Actions).
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/.github/workflows/ci.yml`

Check submission View results

##### 3\. Code Quality Checks in GitHub Actions:

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Run Code Quality Checks in GitHub Actions

\*_Instructions: \*_

-   Extend your GitHub Actions workflow to include a `flake8` check for linting the Django project.
    
-   Fail the build if any linting errors are detected.
    
-   Add a step to generate code coverage reports and upload them as build artifacts.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/.github/workflows/ci.yml`

Check submission View results

##### 4\. Docker Image and github actions

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective:** Build and Push Docker Image using GitHub Actions

**Instructions:**

-   In `dep.yaml` file, Set up a GitHub Actions workflow that builds a Docker image for the messaging app.
    
-   Push the Docker image to Docker Hub
    
-   Use GitHub Actions’ `secrets` feature to store your Docker credentials securely
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/.github/workflows/dep.yml`

Check submission View results



**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
