# Project: Understanding Middlewares | Cairo Intranet

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

Week 5

Week 5

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

## Authentication and Permissions

[

Getting Started with Django REST Framework

](/concepts/104247?project_id=101634)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101634)[

Authentication and Permissions

](/projects/101634)

## Understanding Middleware

[

Django Advanced Features: Middleware, Signals, and Advanced ORM Techniques

](/concepts/107382?project_id=101622)[

Peer Reviews – Feedback That Fuels Growth 💬

](/concepts/111572?project_id=101622)[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101622)[

Understanding Middlewares

](/projects/101622)

# Understanding Middlewares

-   Novice
-   Weight: 1
-   Project over - took place from Jul 21, 2025 1:00 AM to Jul 28, 2025 1:00 AM
-   Manual QA review was done on Jul 28, 2025 3:20 AM
-   An auto review will be launched at the deadline

#### In a nutshell…

-   **Manual QA review:** 0.0/3 mandatory
-   **Auto QA review:** 5.5/11 mandatory
-   **Altogether:**  **39.29%**
    -   Mandatory: 39.29%
    -   Optional: no optional tasks

**Overall comment:**

Project was failed automatically.

#### Overview

Middleware is a powerful feature in application design that acts as a bridge between the request and response phases of the application cycle. In this project, learners will explore the concept of middleware, learn how to write custom middleware, and implement logic such as request interception, permission enforcement, request data filtering, logging, and more. Learners will also examine real-world use cases, such as authentication and rate-limiting, and understand the best practices when integrating middleware into a Django application.

This hands-on project will guide you in building a series of middleware components for an Airbnb Clone or similar web application, allowing them to understand middleware’s role in clean architecture and modular backend development.

#### Learning Objectives

By the end of this project, learners should be able to:

-   Understand the concept and lifecycle of middleware in Django.
-   Create custom middleware to intercept and process incoming requests and outgoing responses.
-   Filter and modify request/response data at the middleware level.
-   Implement access control mechanisms using middleware.
-   Use middleware to enforce API usage policies like rate limiting or request validation.
-   Integrate third-party middleware and understand Django’s default middleware stack.
-   Apply best practices for organizing middleware logic in a scalable project.

#### Learning Outcomes

Upon successful completion, learners will:

-   Define and explain how Django middleware works within the request/response cycle.  
    
-   Write and integrate custom middleware in a Django project.  
    
-   Use middleware to enforce permissions and restrict access based on roles, IP, or headers.  
    
-   Filter and clean incoming request data before reaching the views.  
    
-   Log request and response metadata for auditing or debugging purposes.  
    
-   Separate concerns effectively using middleware rather than overloading views.  
    
-   Evaluate the trade-offs and limitations of using middleware for certain functionalities.

#### Implementation Tasks

Learners will:

1.  **Scaffold a Django project** with an `apps/core` structure for separation of concerns.
2.  **Build custom middleware** to:
    -   Log incoming requests and outgoing responses.
    -   Restrict access to authenticated users or specific user roles.
    -   Block requests from banned IPs or suspicious headers.
    -   Modify or validate incoming JSON payloads.
3.  **Configure the `MIDDLEWARE` stack** correctly in `settings.py` to include both built-in and custom middleware.
4.  **Test middleware behavior** using Postman or Django’s test client to verify interception, modification, and rejection of requests.
5.  **Document middleware behavior** using inline comments and Markdown files for clarity and maintainability.

#### Best Practices for Project Setup and Middleware Design

Here are some best practices to follow during implementation:

### 📁 Project Scaffolding Tips

-   Use a modular structure like:

```
  /project-root
    /apps
      /core
        /middleware
        /models
        /views
      /users
      /listings
    /config
    manage.py
```

-   Keep each custom middleware in a separate Python file under `apps/core/middleware/` for clarity.
-   Use environment variables and Django settings to control behavior (e.g., toggle middleware for dev/production).

#### Middleware Best Practices

-   **Keep middleware functions small and focused** — avoid bloating a single middleware with multiple responsibilities.
-   **Chain logic properly** — always call `get_response(request)` unless rejecting the request early.
-   **Use Django’s `request.user`, `request.path`, and `request.method`** for clean conditional logic.
-   **Avoid database-heavy logic** in middleware to maintain performance.
-   **Use logging middleware responsibly** — log minimal and relevant data to avoid clutter.
-   **Write unit tests** for middleware behavior and edge cases.
-   **Document each middleware** clearly — what it does, why it exists, and where it sits in the stack.

#### Limitations and Considerations

While middleware can be powerful, it’s important to recognize its limitations:

-   Middleware shouldn’t replace views or serializers for business logic.
-   Middleware runs on **every** request, so poorly optimized code can degrade performance.
-   Order in `MIDDLEWARE` settings matters — incorrect ordering may break expected behavior.
-   Some functionalities are better suited for views, decorators, or DRF permissions.

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

What is the main advantage of using Django signals?

-   To decouple applications that need to be notified of events
    
-   To manage database transactions
    
-   To execute code asynchronously
    
-   To increase the speed of request processing
    

---

##### Question #1

What happens if a middleware’s **init**() method raises MiddlewareNotUsed?

-   The middleware will be removed from the middleware chain
    
-   Django will restart the server
    
-   Django will raise an error
    
-   The middleware will be called again with different arguments
    

---

##### Question #2

Which of the following methods connects a receiver function to a signal?

-   Signal.connect
    
-   Signal.link
    
-   Signal.emit
    
-   Signal.notify
    

---

##### Question #3

What is the primary purpose of middleware in Django?

-   To globally alter Django’s request or response processing
    
-   To manage URL routing
    
-   To handle database queries
    
-   To manage user authentication
    

---

##### Question #4

Which Django ORM method is used to retrieve a single object from the database that matches a query?

-   get()
    
-   exclude()
    
-   filter()
    
-   all()
    

---

##### Question #5

What will the following query do?

-   Retrieve entries published in the year 2023
    
-   Retrieve all entries published before 2023
    
-   Retrieve entries published exactly on January 1, 2023
    
-   Retrieve entries with a pub\_date of 2023-01-01
    

---

##### Question #6

What should you use to ensure that a receiver function is not registered multiple times?

-   sender
    
-   disconnect()
    
-   dispatch\_uid
    
-   weak=True
    

---

##### Question #7

What is the purpose of using Q objects in Django queries?

-   To create complex queries with logical operators
    
-   To automatically generate primary keys
    
-   To perform database transactions
    
-   To enforce foreign key constraints
    

---

##### Question #8

Which method would you use to create and save a model instance in a single step?

-   create()
    
-   add()
    
-   save()
    
-   update()
    

---

##### Question #9

Which method in middleware is responsible for processing each request and returning a response?

-   get\_response
    
-   process\_view
    
-   **init**
    
-   **call**
    

## Tasks

##### 0\. project set up

mandatory

Score: 50.0% (Checks completed: 100.0%)

**Objective:** Set up the django messaging app locally

**Instructions:**

-   Make a copy of the `messaging_app` directory done in the project [Building Robust APIs](/rltoken/VKSW5TrX61hxlzoft0a7fg "Building Robust APIs"),
    
-   Rename the copied directory to `Django-Middleware-0x03`
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-Middleware-0x03`
-   File: `Django-Middleware-0x03/*`

Check submission View results

##### 1\. Logging User Requests(Basic Middleware)

mandatory

Score: 50.0% (Checks completed: 100.0%)

**Objective:** Create a middleware that logs each user’s requests to a file, including the timestamp, user and the request path.

**Instructions:** - create a file `middleware.py` and Create the middleware class `RequestLoggingMiddleware` with two methods, `__init__`and `__call__`.

-   In the `__call__` implement a logger that log’s the following information **f"{datetime.now()} - User: {user} - Path: {request.path}“**
    
-   Configure the Middleware section in the `settings.py` with your newly created middleware
    
-   Run the server to test it out. python manage.py runserver
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-Middleware-0x03`
-   File: `chats/middleware.py, requests.log`

Check submission View results

##### 2\. Restrict Chat Access by time

mandatory

Score: 50.0% (Checks completed: 100.0%)

**Objective:** implement a middleware that restricts access to the messaging up during certain hours of the day

**Instructions:**

-   Create a middleware class `RestrictAccessByTimeMiddleware` with two methods, `__init__`and`__call__`. that check the current server time and deny access by returning an error 403 Forbidden
    
    -   if a user accesses the chat outside 9PM and 6PM.
-   Update the `settings.py` with the middleware.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-Middleware-0x03`
-   File: `Django-Middleware-0x03/chats/middleware.py`

Check submission View results

##### 3\. Detect and Block offensive Language

mandatory

Score: 50.0% (Checks completed: 100.0%)

**Objective:** Implement middleware that limits the number of chat messages a user can send within a certain time window, based on their IP address.

**Instructions:**

-   Create the middleware class `OffensiveLanguageMiddleware` with two methods, `__init__`and`__call__`. that tracks number of chat messages sent by each ip address and implement a time based limit i.e 5 messages per minutes such that if a user exceeds the limit, it blocks further messaging and returns and error
    -   use the `__call__`method to count the number of POST requests (messages) from each IP address.
    -   Implement a time window (e.g., 1 minute) during which a user can only send a limited number of messages.
-   Ensure the middleware is added to the`MIDDLEWARE` setting in the `settings.py`

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-Middleware-0x03`
-   File: `Django-Middleware-0x03/chats/middleware.py`

Check submission View results

##### 4\. Enforce chat user Role Permissions

mandatory

Score: 50.0% (Checks completed: 100.0%)

**Objective:** define a middleware that checks the user’s role i.e admin, before allowing access to specific actions

**Instructions:**

-   Create the middleware class RolepermissionMiddleware with two methods, `__init__` and `__call__`. that checks the user’s role from the request
-   If the user is not admin or moderator, it should return error 403
    -   Ensure the middleware is added to the MIDDLEWARE setting in the settings.py

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-Middleware-0x03`
-   File: `Django-Middleware-0x03/chats/middleware.py`

Check submission View results

##### 5\. Manual Review

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-Middleware-0x03`

View results

Ready for a new review

[

Back

](/concepts/111449?project_id=101622)

[

Next

](/projects/209)

Copyright © 2025 ALX, All rights reserved.