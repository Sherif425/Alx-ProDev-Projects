# Project: Milestone 6: Deployment and Documentation | Cairo Intranet

### **Overview**

This task focuses on deploying a Django application to a production-ready cloud server and ensuring all features, including background tasks and API documentation, are fully functional in the live environment. Learners will gain practical experience with server deployment, Celery task queues, and Swagger API documentation, enabling them to bridge the gap between local development and production systems.

### **Learning Objectives**

By completing this task, learners will:

1.  Understand how to deploy a Django application to various cloud hosting platforms.
2.  Learn how to configure and manage environment variables in a production environment.
3.  Set up and run Celery workers with RabbitMQ for background processing.
4.  Configure and make Swagger API documentation publicly accessible.
5.  Test and validate application functionality in a live environment.

### **Learning Outcomes**

Upon successful completion, learners will be able to:

-   Deploy Django applications to production cloud servers such as AWS, Heroku, DigitalOcean, or PythonAnywhere.
-   Securely configure and manage environment variables on a remote server.
-   Integrate and manage Celery workers with RabbitMQ for asynchronous task handling.
-   Publish API documentation using Swagger for public access.
-   Perform functional testing on deployed applications to ensure production readiness.

### **Key Concepts**

-   **Cloud Deployment**: Moving applications from local development to live hosting environments.
-   **Environment Variables**: Storing sensitive information (e.g., API keys, DB credentials) securely.
-   **Celery Task Queue**: Handling asynchronous tasks in Django applications.
-   **RabbitMQ**: Message broker for managing task queues.
-   **Swagger UI**: Interactive documentation for API endpoints.
-   **Production Testing**: Verifying live application functionality post-deployment.

### **Tools and Libraries**

-   **Python Django** – Web framework for application development.
-   **Celery** – Asynchronous task queue for background jobs.
-   **RabbitMQ** – Message broker for Celery communication.
-   **Swagger / drf-yasg** – API documentation generation.
-   **Cloud Hosting Platforms** – AWS, Heroku, DigitalOcean, PythonAnywhere.
-   **Gunicorn / uWSGI** – WSGI servers for serving Django in production.
-   **NGINX** – Reverse proxy server for production setups.

### **Additional Resources**

-   [Deploying Django to production](/rltoken/iJYjnVOj-CoN5Q75yxjb2Q "Deploying Django to production")
-   [Deploy a Django App on Render](/rltoken/tXEGZKuiIOfGa14GNrfpnQ "Deploy a Django App on Render")
-   [Deploy a Django App on PythonAnywhere](/rltoken/1IJ16VU9KFGDoViFvB3Qgg "Deploy a Django App on PythonAnywhere")

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

## Tasks

##### 0\. Deployment of Django Application with Celery and Public API Documentation

mandatory

**Objective**

Deploy the application to a server and ensure Swagger documentation is publicly accessible.

**Instructions**

-   **Deploy Application:**
    
    -   Deploy the application to a cloud server (e.g., Render, Pythonanywhere - Recommended).
    -   Ensure all necessary environment variables are configured correctly on the server.
-   **Run Celery Worker on Server:**
    
    -   Configure Celery to run on the server with RabbitMQ.
    -   Verify that background tasks work as expected in the live environment.
-   **Configure Swagger**:
    
    -   Ensure that Swagger documentation is accessible publicly at /swagger/ on the deployed server.
-   **Test Deployed Application:**
    
    -   Test all endpoints, including the email notification feature, to confirm they function correctly in production.
