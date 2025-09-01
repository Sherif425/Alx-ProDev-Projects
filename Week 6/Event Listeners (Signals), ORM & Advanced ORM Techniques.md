# Project: Event Listeners (Signals), ORM & Advanced ORM Techniques | Cairo Intranet

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

# Event Listeners (Signals), ORM & Advanced ORM Techniques

-   Novice
-   Weight: 1
-   Project over - took place from Jul 28, 2025 1:00 AM to Aug 4, 2025 1:00 AM
-   **Manual QA review must be done** (request it when you are done with the project)
-   An auto review will be launched at the deadline

#### In a nutshell…

-   **Manual QA review:** Pending
-   **Auto QA review:** 0.0/19 mandatory
-   **Altogether:** waiting on some reviews

### Overview

In modern web applications, **performance**, **modularity**, and **clean architecture** are essential. Django provides powerful tools that help developers build robust and maintainable backend systems. Three core concepts that support these goals are:

1.  **Event Listeners using Django Signals**  
    Signals allow decoupled parts of an application to communicate by emitting and listening to events. This enables actions like sending confirmation emails or logging activities whenever a specific model action (like saving or deleting) occurs—without tightly coupling that logic to your views or models.
    
2.  **Django ORM & Advanced ORM Techniques**  
    Django’s Object-Relational Mapper (ORM) enables developers to interact with the database using Python code instead of SQL. It also provides advanced tools to optimize performance—like `select_related`, `prefetch_related`, and query annotations—helping avoid common issues like the N+1 query problem.
    
3.  **Basic Caching**  
    Caching stores frequently accessed data so it can be retrieved faster. Django supports various caching strategies (view-level, template fragment, low-level caching), which can drastically reduce page load time and database load.
    

Together, these techniques improve **application responsiveness**, **database efficiency**, and **code scalability**, making them crucial tools for Django backend developers.

#### Learning Objectives

By the end of this module, learners will be able to:

-   Explain and implement Django **Signals** to build event-driven features.
-   Use Django **ORM** to perform CRUD operations and write efficient queries.
-   Apply **advanced ORM** techniques for optimizing database access.
-   Implement **basic caching** strategies to enhance performance.
-   Follow **best practices** to ensure maintainable, decoupled, and performant backend code.

#### Learning Outcomes

Learners will be able to:

-   Use Django Signals to decouple side-effects from core business logic.
-   Efficiently retrieve and manipulate database data using Django ORM.
-   Avoid performance issues through query optimization techniques.
-   Implement caching at the view, template, or data level to reduce server workload.
-   Write clean and testable backend logic using Django’s built-in tools.

### 1\. **Event Listeners Using Django Signals**

#### What are Signals?

Django **Signals** allow certain senders to notify a set of receivers when specific actions have taken place. They’re useful for triggering side effects like notifications, logging, or updates across different parts of your app.

#### Common Signals:

-   `pre_save` / `post_save`  
    
-   `pre_delete` / `post_delete`  
    
-   `m2m_changed`  
    
-   `request_started` / `request_finished`

#### Best Practices:

-   Keep signal functions lean and avoid long-running tasks.
-   Use the `@receiver` decorator to keep registration clean and explicit.
-   Separate business logic from the signal handler—call a service or utility function.
-   Disconnect signals during tests to prevent unwanted behavior.

### 2\. **Django ORM Basics**

#### 🔧 What is ORM?

The **Object-Relational Mapper (ORM)** allows interaction with the database using Python models. You can query, insert, update, and delete records using intuitive syntax without writing raw SQL.

#### Common Operations:

-   Create: `Model.objects.create(...)`
-   Retrieve: `Model.objects.get(...)`, `.filter()`, `.all()`
-   Update: `.save()`, `.update()`
-   Delete: `.delete()`

#### Best Practices:

-   Always catch exceptions like `DoesNotExist` and `MultipleObjectsReturned`.
-   Chain `.filter()` to narrow queries instead of retrieving all data.
-   Validate data before saving.

### 3\. **Advanced ORM Techniques**

#### Tools for Performance:

-   `select_related()` – for foreign key optimizations (JOINs).
-   `prefetch_related()` – for many-to-many or reverse foreign key optimizations.
-   `annotate()` – for aggregations like counts or sums.
-   `Q()` and `F()` – for complex queries and field-based calculations.
-   **Custom Managers** – to encapsulate and reuse query logic.

#### Best Practices:

-   Avoid repeated queries with eager loading.
-   Use `only()` or `defer()` to limit unnecessary field loading.
-   Profile complex queries using Django Debug Toolbar or `.query`.

### 4\. **Basic Caching in Django**

#### What is Caching?

**Caching** stores the result of expensive computations or database queries to avoid reprocessing. Django supports multiple levels of caching, including per-view, per-template-fragment, and manual (low-level) cache APIs.

#### Common Tools:

-   `@cache_page(60 * 15)` – for view-level caching.
-   `{% cache 300 "sidebar" %}` – for template fragment caching.
-   `cache.set()`, `cache.get()` – low-level caching.

#### Best Practices:

-   Don’t cache sensitive or user-specific data unless scoped properly.
-   Use cache versioning and meaningful keys.
-   Invalidate/update cache upon data changes using signals or explicit logic.

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

##### 0\. Implement Signals for User Notifications

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective:** Automatically notify users when they receive a new message.

**Instructions:**

-   Create a Message model with fields like sender, receiver, content, and timestamp.
    
-   Use Django signals (e.g., post\_save) to trigger a notification when a new Message instance is created.
    
-   Create a Notification model to store notifications, linking it to the User and Message models.
    
-   Write a signal that listens for new messages and automatically creates a notification for the receiving user.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-signals_orm-0x04`
-   File: `messaging/models.py, messaging/signals.py, messaging/apps.py, messaging/admin.py, messaging/tests.py`

Check submission View results

##### 1\. Create a Signal for Logging Message Edits

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective:** Log when a user edits a message and save the old content before the edit.

**Instructions:**

-   Add an edited field to the Message model to track if a message has been edited.
    
-   Use the pre\_save signal to log the old content of a message into a separate MessageHistory model before it’s updated.
    
-   Display the message edit history in the user interface, allowing users to view previous versions of their messages.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-signals_orm-0x04`
-   File: `messaging/Models`

Check submission View results

##### 2\. Use Signals for Deleting User-Related Data

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective:** Automatically clean up related data when a user deletes their account.

**Instructions:**

-   Create a delete\_user view that allows a user to delete their account.
    
-   Implement a post\_delete signal on the User model to delete all messages, notifications, and message histories associated with the user.
    
-   Ensure that foreign key constraints are respected during the deletion process by using CASCADE or custom signal logic.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-signals_orm-0x04`
-   File: `messaging/Views`

Check submission View results

##### 3\. Leverage Advanced ORM Techniques for Threaded Conversations

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective:** Implement threaded conversations where users can reply to specific messages, and retrieve conversations efficiently.

**Instructions:**

-   Modify the Message model to include a parent\_message field (self-referential foreign key) to represent replies.
    
-   Use prefetch_related and select_related to optimize querying of messages and their replies, reducing the number of database queries.
    
-   Implement a recursive query using Django’s ORM to fetch all replies to a message and display them in a threaded format in the user interface.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-signals_orm-0x04`
-   File: `Django-Chat/Models`

Check submission View results

##### 4\. Custom ORM Manager for Unread Messages

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective**: Create a custom manager to filter unread messages for a user.

**Instructions:**

-   Add a read boolean field to the Message model to indicate whether a message has been read.
    
-   Implement a custom manager (e.g., UnreadMessagesManager) that filters unread messages for a specific user.
    
-   Use this manager in your views to display only unread messages in a user’s inbox.
    
-   Optimize this query with .only() to retrieve only necessary fields.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-signals_orm-0x04`
-   File: `messaging/Models`

Check submission View results

##### 5\. implement basic view cache

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective:** Set up basic caching for a view that retrieves messages in the messaging app.

**Instructions:**

-   Update your settings.py in your messaging_app/messaging_app/settings.py with the default cache i.e django.core.cache.backends.locmem.LocMemCache as follows:

```
CACHES = { 'default': { 'BACKEND': 'django.core.cache.backends.locmem.LocMemCache', 'LOCATION': 'unique-snowflake', } }

```

-   Use `cache-page` in your views to cache the view that displays a list of messages in a conversation. Learn more about cache-page [here](/rltoken/PcoYTNpZZnOh9kewcrh7Cg "here")
    
-   Set a 60 seconds cache timeout on the view.
    

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-signals_orm-0x04`
-   File: `messaging_app/messaging_app/settings.py, chats/views.py`

Check submission View results

##### 6\. Manual Review

mandatory

**Repo:**

-   GitHub repository: `alx-backend-python`
-   Directory: `Django-signals_orm-0x04`

View results

Ready for a review

[

Back

](/concepts/111449?project_id=101623)

[

Next

](/concepts/111449?project_id=101643)

Copyright © 2025 ALX, All rights reserved.