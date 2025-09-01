# Project: Caching in Django | Cairo Intranet

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

# Caching in Django

-   Novice
-   Weight: 1
-   Project over - took place from Aug 25, 2025 1:00 AM to Sep 1, 2025 1:00 AM
-   An auto review will be launched at the deadline

#### In a nutshell…

-   **Auto QA review:** 17.0/17 mandatory
-   **Altogether:**  **100.0%**
    -   Mandatory: 100.0%
    -   Optional: no optional tasks

#### Overview

This project implements a Django-based property listing application with Redis caching at multiple levels. The system demonstrates various caching strategies including view-level caching, low-level queryset caching, and proper cache invalidation techniques. The application uses Docker to containerize PostgreSQL for data persistence and Redis for caching, providing a realistic development environment that mirrors production setups.

#### Learning Objectives

-   Implement multi-level caching strategies in Django applications
-   Configure and integrate Redis as a cache backend
-   Set up containerized services (PostgreSQL and Redis) using Docker
-   Understand cache invalidation techniques using Django signals
-   Analyze cache performance metrics
-   Develop efficient database query patterns with caching
-   Structure Django projects for maintainability and scalability

#### Key Concepts

1.  **Multi-level Caching**: Implementing both view-level and low-level caching
2.  **Cache Invalidation**: Using Django signals to maintain cache consistency
3.  **Containerization**: Managing dependencies with Docker containers
4.  **Cache Metrics**: Monitoring and analyzing Redis cache performance
5.  **Database Optimization**: Reducing database load through intelligent caching

#### Tools and Libraries

-   **Django**: Web framework for building the property listing application
-   **PostgreSQL**: Relational database for persistent storage
-   **Redis**: In-memory data store used for caching
-   **Docker**: Containerization platform for service management
-   **django-redis**: Django cache backend for Redis integration
-   **psycopg2**: PostgreSQL adapter for Python
-   **Python’s logging**: For tracking cache metrics and performance

#### Real-World Use Case

This project models a real estate listing platform where: 1. Property listings are frequently accessed but rarely modified 2. Database load needs to be minimized during peak traffic 3. Data consistency must be maintained despite caching 4. Performance metrics are monitored to optimize cache effectiveness

Such caching implementations are crucial for: - High-traffic listing platforms (real estate, e-commerce) - Applications with expensive database queries - Systems requiring sub-second response times - Platforms needing to scale efficiently under load

The techniques demonstrated provide a blueprint for building performant web applications while maintaining data consistency and reducing infrastructure costs.

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

##### 0\. Set Up Django Project with Dockerized PostgreSQL and Redis

mandatory

Score: 100.0% (Checks completed: 100.0%)

##### Objective

Initialize a Django project for the property listing app, configure PostgreSQL and Redis in Docker, and set up the cache backend.

##### Instructions

**1\. Create the Django Project:**

-   Initialize a Django project named `alx-backend-caching_property_listings.`
-   Create a Django app named `properties` inside the project.
-   Create a Property model in `properties/models.py` with fields:
    -   `title` (CharField, max\_length=200)
    -   `description` (TextField)
    -   `price` (DecimalField, max_digits=10, decimal_places=2)
    -   `location` (CharField, max\_length=100)
    -   `created_at` (DateTimeField, auto_now_add=True)
-   Run migrations to create the database schema.

1.  **Set Up Dockerized PostgreSQL and Redis:**

-   Create a `docker-compose.yml` file in the project root to define two services:
    -   `PostgreSQL`: Use the official `postgres:latest` image, expose port `5432`, and set environment variables for database configuration.
    -   `Redis`: Use the official `redis:latest image`, expose port `6379`.
-   Ensure both services are accessible from the Django app (e.g., `PostgreSQL` via `postgres:5432`, `Redis` via`redis:6379`).

**3\. Configure Django Settings:**

-   Install required Python packages: `django`, `django-redis`, `psycopg2-binary`.
-   Add `django-redis` to `INSTALLED_APPS` in `alx-backend-caching_property_listings/settings.py.`
-   Configure the `database` to use `PostgreSQL` in `alx-backend-caching_property_listings/settings.py`
-   Configure `Redis` as the cache backend in `alx-backend-caching_property_listings/settings.py`

**Repo:**

-   GitHub repository: `alx-backend-caching_property_listings`
-   File: `alx-backend-caching_property_listings/settings.py, docker-compose.yaml, properties/models.py,`

Check submission View results

##### 1\. Cache Property List View

mandatory

Score: 100.0% (Checks completed: 100.0%)

##### Objective

Cache the property list view’s response in Redis for 15 minutes.

##### Instructions

-   Create a `property_list` view in `properties/views.py` to return all properties.
-   Apply `@cache_page(60 * 15)`to cache the response in Redis.
-   Map the view to `/properties/` via URL configuration.

**Repo:**

-   GitHub repository: `alx-backend-caching_property_listings`
-   File: `properties/views.py, properties/urls.py, alx_backend_caching_property_listings/urls.py`

Check submission View results

##### 2\. Low-Level Caching for Property Queryset

mandatory

Score: 100.0% (Checks completed: 100.0%)

##### Objective

Cache the Property queryset in Redis for 1 hour using Django’s low-level cache API.

##### Instructions

1.  Create properties/utils.py with a get_all_properties() function that:

-   Checks Redis for `all_properties` using `cache.get('all_properties').`
-   Fetches`Property.objects.all()` if not found.
-   Stores the queryset in Redis with `cache.set('all_properties', queryset, 3600).`
-   Returns the queryset.

1.  Update `property_list` to use`get_all_properties().`

**Repo:**

-   GitHub repository: `alx-backend-caching_property_listings`
-   File: `properties/utils.py, properties/views.py`

Check submission View results

##### 3\. Cache Invalidation Using Signals

mandatory

Score: 100.0% (Checks completed: 100.0%)

##### Objective

Invalidate the all\_properties Redis cache on Property create/update/delete using Django signals.

##### Instructions

-   Create `properties/signals.py` with `post_save` and `post_delete` signal handlers that call `cache.delete('all_properties').`
-   In `properties/apps.py`, override `ready()` to import signals.py.
-   Update `properties/__init__.py` for the app config.

**Repo:**

-   GitHub repository: `alx-backend-caching_property_listings`
-   File: `properties/signals.py, properties/apps.py, properties/__init__.py`

Check submission View results

##### 4\. Cache Metrics Analysis

mandatory

Score: 100.0% (Checks completed: 100.0%)

##### Objective

Retrieve and analyze Redis cache hit/miss metrics.

##### Instructions

1.In `properties/utils.py`, add `get_redis_cache_metrics()` to:

-   Connect to Redis via `django_redis.`
-   Get `keyspace_hits` and `keyspace_misses` from INFO.
-   Calculate hit ratio (`hits / (hits + misses)`).
-   Log metrics and return a dictionary.

**Repo:**

-   GitHub repository: `alx-backend-caching_property_listings`
-   File: `properties/utils.py`

Check submission View results

[

Back

](/concepts/111449?project_id=102428)

[

Next

](/projects/102426)

Copyright © 2025 ALX, All rights reserved.