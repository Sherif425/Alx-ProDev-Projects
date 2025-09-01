# Project: Milestone 3: Creating Views and API Endpoints | Cairo Intranet

ProDev Backend Average: 83.34%

-   [
    
    Back-End Web Development Average: 96.1%
    
    
    
    ](/curriculums/70/observe)
-   [
    
    ProDev Backend Average: 83.34%
    
    
    
    ](/curriculums/86/observe)
-   [
    
    Professional Foundations Average: 94.18%
    
    
    
    ](/curriculums/89/observe)

Week 6

Week 6

-   [Week 0](/projects/102638)
-   [Week 1](/concepts/113077?project_id=102975)
-   [Week 2](/projects/101641)
-   [Week 3](/projects/102758)
-   [Week 4](/projects/101642)
-   [Week 5](/projects/101622)
-   [Week 6](/projects/209)
-   [Week 7](/projects/102965)
-   [Week 8](/projects/102087)
-   [Week 9](/projects/101632)
-   [Week 10](/projects/102428)
-   [Week 11](/projects/102426)

## Event Listeners and ORMs

[

Django Advanced Features: Middleware, Signals, and Advanced ORM Techniques

](/concepts/107382?project_id=101623)[

Peer Reviews – Feedback That Fuels Growth 💬

](/concepts/111572?project_id=101623)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101623)[

Event Listeners (Signals), ORM & Advanced ORM Techniques

](/projects/101623)

## Milestone 3

[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101643)[

Milestone 3: Creating Views and API Endpoints

](/projects/101643)

## Shell Basics

[

Struggling with the sandbox? Try this: Using Docker & WSL on your local host

](/concepts/100039?project_id=209)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=209)[

0x03. Shell, init files, variables and expansions

](/projects/209)

# Milestone 3: Creating Views and API Endpoints

-   Novice
-   Weight: 1
-   Project over - took place from Jul 28, 2025 1:00 AM to Aug 4, 2025 1:00 AM
-   **Manual QA review must be done** (request it when you are done with the project)
-   An auto review will be launched at the deadline

#### In a nutshell…

-   **Manual QA review:** Pending
-   **Auto QA review:** 0.0/4 mandatory
-   **Altogether:** waiting on some reviews

### **Overview**

In this task, you will enhance the `alx_travel_app` project by implementing API views to manage **listings** and **bookings**. You’ll create fully functional CRUD (Create, Read, Update, Delete) endpoints using **Django REST Framework (DRF)** and document them with **Swagger** for ease of access and testing. The focus is on following RESTful API design principles while ensuring endpoints are properly tested for reliability.

### **Learning Objectives**

By the end of this task, learners should be able to:

-   Implement **ViewSets** in Django REST Framework to handle multiple model operations efficiently.
-   Configure API routes using DRF’s **routers**.
-   Apply RESTful conventions in API endpoint design.
-   Document APIs with **Swagger** for clear and interactive API exploration.
-   Test API endpoints with tools like **Postman** to verify correctness.

### **Learning Outcomes**

Learners will be able to:

-   Create and manage CRUD endpoints for multiple models in Django REST Framework.
-   Integrate automatic API documentation with Swagger.
-   Deploy well-structured and tested API endpoints that follow REST best practices.
-   Confidently test API functionalities for both successful and error scenarios.

### **Key Concepts**

-   **CRUD Operations**: Create, Read, Update, and Delete functionality for API resources.
-   **ModelViewSet**: A DRF class that provides a complete set of CRUD actions without extra boilerplate.
-   **Routers in DRF**: Automatically map ViewSets to URLs in a RESTful format.
-   **Swagger API Documentation**: Automatically generated interactive API docs.
-   **API Testing**: Using tools like Postman to validate API functionality.

### **Tools and Libraries**

-   **Django** – High-level Python web framework.
-   **Django REST Framework (DRF)** – Toolkit for building Web APIs.
-   **drf-yasg** or **django-rest-swagger** – For Swagger documentation generation.
-   **PostgreSQL** (or SQLite) – Database for storing listings and bookings data.
-   **Postman** – For testing API endpoints.

### **Real-World Use Case**

This task mirrors the backend development process for **travel booking platforms** like **Airbnb**, **Booking.com**, or **Expedia**. These platforms need robust APIs to manage property listings and handle booking requests efficiently. By implementing CRUD endpoints and documenting them with Swagger, developers create scalable, maintainable, and easy-to-test backends that can serve mobile and web applications in real-time.

### Additional Resources

-   [Build a CRUD API](/rltoken/J4yfXhCf6yKuEw9ZDHn2iQ "Build a CRUD API")
-   [Integrating drf-yasg for Swagger](/rltoken/-qxHit9LfIB733SnVuVGVA "Integrating drf-yasg for Swagger")

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

## Tasks

##### 0\. API Development for Listings and Bookings in Django

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective**

Build API views to manage listings and bookings, and ensure the endpoints are documented with Swagger.

**Instructions**

-   **Duplicate Project:**
    
    -   Duplicate the project `alx_travel_app_0x00` to `alx_travel_app_0x01`
-   **Create ViewSets**:
    
    -   In listings/views.py, create viewsets for Listing and Booking using Django REST framework’s ModelViewSet.
    -   Ensure that these views provide CRUD operations for both models.
-   **Configure URLs:**
    
    -   Use a router to configure URLs for the API endpoints.
    -   Ensure endpoints follow RESTful conventions and are accessible under /api/.
-   **Test Endpoints:**
    
    -   Test each endpoint (GET, POST, PUT, DELETE) using a tool like Postman to ensure they work as expected.

**Repo:**

-   GitHub repository: `alx_travel_app_0x01`
-   Directory: `alx_travel_app`
-   File: `listings/views.py, listings/urls.py, README.md`

Check submission View results

##### 1\. Manual Review

mandatory

**Repo:**

-   GitHub repository: `alx_travel_app_0x01`
-   Directory: `alx_travel_app`

View results

Ready for a review

[

Back

](/concepts/111449?project_id=101643)

[

Next

](/concepts/100039?project_id=209)

Copyright © 2025 ALX, All rights reserved.