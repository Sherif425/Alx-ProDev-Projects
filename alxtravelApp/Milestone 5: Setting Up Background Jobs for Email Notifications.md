# Project: Milestone 5: Setting Up Background Jobs for Email Notifications | Cairo Intranet

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

Week 10

Week 10

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

## Scheduling and Automation

[

Automating Tasks in Django: From Cron Basics to Advanced Scheduling

](/concepts/110234?project_id=102247)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=102247)[

Crons: Scheduling and Automating Tasks

](/projects/102247)

## Milestone 5

[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101645)[

Milestone 5: Setting Up Background Jobs for Email Notifications

](/projects/101645)

## Caching In Django

[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=102428)[

Caching in Django

](/projects/102428)

# Milestone 5: Setting Up Background Jobs for Email Notifications

-   Novice
-   Weight: 1
-   Project over - took place from Aug 25, 2025 1:00 AM to Sep 1, 2025 1:00 AM
-   Manual QA review was done on Aug 31, 2025 6:18 PM
-   An auto review will be launched at the deadline

#### In a nutshell…

-   **Manual QA review:** 5.0/5 mandatory
-   **Auto QA review:** 5.0/5 mandatory
-   **Altogether:**  **100.0%**
    -   Mandatory: 100.0%
    -   Optional: no optional tasks

**Overall comment:**

Good Job

### **Overview**

This task focuses on enhancing the `alx_travel_app` project by implementing asynchronous background processing using **Celery** with **RabbitMQ** as the message broker. The main feature added is an **email notification system** that sends booking confirmations without blocking the main request-response cycle. This ensures improved performance and a better user experience.

### **Learning Objectives**

By completing this task, learners will:

-   Understand how to integrate **Celery** with **RabbitMQ** in a Django application.
-   Learn to configure asynchronous task processing for improved performance.
-   Implement an email notification feature triggered by user actions.
-   Gain experience in working with Django’s email backend for automated communications.

### **Learning Outcomes**

After completing this task, learners will be able to:

-   Configure and run Celery with RabbitMQ as a message broker.
-   Create and manage shared tasks in Django using Celery.
-   Trigger Celery tasks from Django views or viewsets.
-   Test and verify asynchronous operations such as sending emails.

### **Key Concepts**

-   **Asynchronous Task Processing:** Running time-consuming tasks in the background.
-   **Message Broker:** Middleware (RabbitMQ) used to send and receive task messages between Django and Celery.
-   **Celery Configuration:** Setting up `celery.py` and integrating it into `settings.py`.
-   **Shared Tasks:** Functions decorated with `@shared_task` for execution by Celery workers.
-   **Email Backend in Django:** Configuring SMTP settings for sending automated emails.

### **Tools and Libraries**

-   **Django** – Backend web framework for building the application.
-   **Celery** – Distributed task queue for background task execution.
-   **RabbitMQ** – Message broker to handle communication between Django and Celery.
-   **SMTP Email Backend** – For sending booking confirmation emails.

### **Additional Resources**

-   [What is a Message Queue?](/rltoken/X3qOrEDTd_7Hf7tvUwhLMg "What is a Message Queue?")
-   [Everything about Celery](/rltoken/dsr1Nai1vyqdh1_a3XtyBQ "Everything about Celery")
-   [RabbitMQ with Python: From Basics to Advanced Messaging Patterns (A Practical Guide)](/rltoken/xPY6xV1A3r35JzYMoYRVGA "RabbitMQ with Python: From Basics to Advanced Messaging Patterns (A Practical Guide)")
-   [Building a Sample Project Using Celery with Python](/rltoken/FcqXTDRJPOSgNnmzWlDdwQ "Building a Sample Project Using Celery with Python")

### **Real-World Use Case**

In real-world travel or booking platforms like **Booking.com** or **Airbnb**, sending booking confirmation emails instantly is critical but should not delay the user experience. Using **Celery** with **RabbitMQ**, the email sending process can be offloaded to a background worker, ensuring users receive instant feedback while the system handles notifications asynchronously. This approach is scalable and can also be extended to other time-consuming tasks such as invoice generation, report creation, or SMS notifications.

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

##### 0\. Background Task Management with Celery and Email Notifications in Django

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective**

Configure Celery with RabbitMQ to handle background tasks and implement an email notification feature for bookings.

**Instructions**

-   **Duplicate Project:**
    
    -   Duplicate the project `alx_travel_app_0x02` to `alx_travel_app_0x03`
-   **Configure Celery**:
    
    -   Set up Celery with RabbitMQ as the message broker.
    -   Add Celery configurations in `settings.py` and create a `celery.py` file in the project root.
-   **Define Email Task:**
    
    -   In `listings/tasks.py`, create a shared task function to send a booking confirmation email.
    -   Ensure the email task uses the Django email backend configured in `settings.py`.
-   **Trigger Email Task:**
    
    -   Modify the `BookingViewSet` to trigger the email task upon booking creation using `delay()`.
-   **Test Background Task:**
    
    -   Test the background task to ensure the email is sent asynchronously when a booking is created.

**Repo:**

-   GitHub repository: `alx_travel_app_0x03`
-   Directory: `alx_travel_app`
-   File: `alx_travel_app/settings.py, listings/tasks.py, listings/views.py, README.md`

Check submission View results

##### 1\. Manual Review

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Repo:**

-   GitHub repository: `alx_travel_app_0x03`
-   Directory: `alx_travel_app`

View results

Ready for a new review

[

Back

](/concepts/111449?project_id=101645)

[

Next

](/concepts/111449?project_id=102428)

Copyright © 2025 ALX, All rights reserved.