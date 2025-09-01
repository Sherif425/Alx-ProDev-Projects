# Project: Authentication and Permissions | Cairo Intranet

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

# Authentication and Permissions

-   Novice
-   Weight: 1
-   Project over - took place from Jul 21, 2025 1:00 AM to Jul 28, 2025 1:00 AM
-   **Manual QA review must be done** (request it when you are done with the project)
-   An auto review will be launched at the deadline

#### In a nutshell…

-   **Manual QA review:** Pending
-   **Auto QA review:** 0.0/13 mandatory
-   **Altogether:** waiting on some reviews

#### Understanding Authentication and Permission in Enterprise Applications

Authentication and permission systems are the cornerstone of any secure and scalable backend architecture. Whether you’re building a small SaaS platform or a robust enterprise-grade application, implementing robust user access controls ensures the integrity, confidentiality, and availability of your system’s data.

In Django, authentication and authorization (permissions) are elegantly handled through a combination of built-in tools and extendable frameworks. For **mid to senior-level backend engineers**, mastering these components is essential not only for technical growth but also for building secure, maintainable, and scalable systems that align with industry standards and compliance requirements (e.g., GDPR, HIPAA, SOC 2).

In small-scale apps, authentication may seem straightforward with simple login/signup flows. However, as the application scales, challenges such as **multi-role systems**, **fine-grained permissions**, **external integrations (OAuth, JWT, SSO)**, and **API security** become more critical. Understanding how to implement and customize these systems will empower developers to create backend services that are both user-friendly and enterprise-ready.

##### **Learning Objectives**

By the end of this module, learners will be able to:

1.  **Understand Core Concepts**
    
    -   Define authentication and authorization, and understand how Django handles both.
    -   Differentiate between user roles, groups, and permission sets.
2.  **Implement Authentication**
    
    -   Build custom user models and extend Django’s default `User` model.
    -   Implement session-based and token-based (e.g., JWT) authentication.
    -   Integrate third-party authentication services (e.g., OAuth2, SSO).
3.  **Design Permission Systems**
    
    -   Create custom permissions for models, views, and APIs.
    -   Use Django’s `permissions_required`, `@login_required`, and `DRF permissions`.
    -   Implement object-level permissions for more granular control.
4.  **Secure Enterprise APIs**
    
    -   Enforce role-based access control (RBAC) for enterprise applications.
    -   Combine authentication with throttling and rate limiting for production use.
5.  **Audit and Monitor Access**
    
    -   Set up logging, user activity tracking, and audit trails.
    -   Understand best practices for secure password storage, account recovery, and session handling.

##### **Expected Learning Outcomes**

Learners will:

-   Build robust authentication flows using Django and Django REST Framework.
-   Develop scalable permission layers for small to enterprise-grade apps.
-   Apply security principles to protect APIs and sensitive endpoints.
-   Gain confidence in integrating third-party identity providers (IdPs) and implementing custom permissions.
-   Understand how to structure user roles and access hierarchies in complex systems.

##### **Suggested Tools and Libraries to Master**

Tool/Library

Purpose

**Django Allauth**

Streamlined user authentication, including email verification and social auth

**Django REST Framework (DRF)**

Token and session authentication for APIs

**SimpleJWT / djangorestframework-simplejwt**

Lightweight JWT authentication for DRF

**OAuthLib / django-oauth-toolkit**

Secure OAuth2 implementation in Django

**Guardian**

Object-level permissions and per-instance access control

**Auth0**

Third-party identity and access management integration

**Keycloak**

Open-source identity provider for managing enterprise SSO

**Okta**

Enterprise IAM provider with SSO, MFA, and directory services

**PyJWT**

Lightweight JWT token generation and validation

**Auditlog**

Automatic tracking of model changes and user actions for audit trails

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

Which of the following DRF classes is used to create class-based views that can handle HTTP methods like GET, POST, PATCH, and DELETE?

-   APIView
    
-   TemplateView
    
-   View
    
-   ModelView
    

---

##### Question #1

In DRF, what is the purpose of serializers?

-   To convert Python objects into JSON format and vice-versa
    
-   To manage URL routing
    
-   To handle database migrations
    
-   To render HTML templates
    

---

##### Question #2

Which of the following is NOT a built-in authentication scheme provided by Django REST Framework?

-   SessionAuthentication
    
-   OAuth2Authentication
    
-   BasicAuthentication
    
-   TokenAuthentication
    

---

##### Question #3

What is the primary purpose of Django REST Framework (DRF)?

-   To create web APIs using Django’s ORM and other features
    
-   To handle template rendering in Django applications
    
-   To handle user authentication in Django applications
    
-   To manage static files in Django projects
    

---

##### Question #4

In TokenAuthentication, how is the token sent by the client to authenticate the request?

-   As a cookie
    
-   In the body of the request
    
-   As a query parameter in the URL
    
-   In the Authorization header prefixed with “Token”
    

---

##### Question #5

Which authentication scheme uses Django’s default session backend to authenticate API requests?

-   BasicAuthentication
    
-   RemoteUserAuthentication
    
-   TokenAuthentication
    
-   SessionAuthentication
    

---

##### Question #6

What is the default response code returned when an unauthenticated request is made to a DRF view with authentication required?

-   401 Unauthorized
    
-   404 Not Found
    
-   200 OK
    
-   403 Forbidden
    

---

##### Question #7

What should be done to ensure that TokenAuthentication is secure when used in a production environment?

-   Ensure the API is available only over HTTPS
    
-   Store the token in the URL
    
-   Use it over HTTP connections
    
-   Disable CSRF protection
    

---

##### Question #8

What must be included in AJAX requests when using SessionAuthentication for “unsafe” HTTP methods such as POST, PUT, PATCH, and DELETE?

-   A valid CSRF token
    
-   Basic authentication credentials
    
-   A JWT token
    
-   A session cookie
    

---

##### Question #9

Which HTTP method is used to partially update an existing resource in a REST API?

-   POST
    
-   PATCH
    
-   GET
    
-   PUT
    

## Tasks

##### 0\. Implement Authentication

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective:** Add user authentication using JWT (JSON Web Tokens) or Session Authentication.

**Instructions:**

-   Install `djangorestframework-simplejwt` for JWT Authentication.
    
-   Configure the authentication settings in the `settings.py`. More on how to: [here](/rltoken/UZQPtPz_cDAT5lzq1qhkUw "here")
    
-   Ensure all users can access their own messages and conversations
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/settings.py, messaging_app/chats/auth.py, messaging_app/urls.py, messaging_app/chats/permissions.py`

Check submission View results

##### 1\. Add Permissions

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective**: Create custom permission classes to control access.

**Instructions:**

-   Create and extend the permissions class `IsParticipantOfConversation` to:
    
    -   Allow only authenticated users to access the api
    -   Allow only participants in a conversation to send, view, update and delete messages
-   Apply the custom permissions to your viewsets to enforce access control
    
-   Update your settings.py to set default permissions globally
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `chats/permissions.py, chats/Views.py, messaging_app/settings.py`

Check submission View results

##### 2\. Pagination and Filtering

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective:** implement pagination and filtering for messages

**Instructions:**

-   Add pagination listing on the messages such that the api fetches 20 messages per page. Resource: [here](/rltoken/uHqJm6nDO2W79dkWHJ8DJg "here")
    
-   Using `django-filters` , Add filtering class `MessageFilter` to your views to retrieve conversations with specific users or messages within a time range
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `messaging_app/settings.py, chats/views.py, chats/permissions.py, chats/filters.py, chats/pagination.py`

Check submission View results

##### 3\. Testing the API Endpoints

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective:** Use postman to test api endpoints

**Instructions:**

-   Test creating a conversation, sending messages and fetching conversations
    
-   Test authentication (JWT token login) and ensure that unauthorized users cannot access private conversations.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`
-   File: `post_man-Collections`

Check submission View results

##### 4\. Manual Review

mandatory

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `messaging_app`

View results

Ready for a review

[

Back

](/concepts/111449?project_id=101634)

[

Next

](/concepts/107382?project_id=101622)

Copyright © 2025 ALX, All rights reserved.