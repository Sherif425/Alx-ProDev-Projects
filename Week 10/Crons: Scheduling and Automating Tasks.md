# Project: Crons: Scheduling and Automating Tasks | Cairo Intranet


#### Overview

Cron is a time-based task scheduler in Unix-like systems, commonly used to automate repetitive jobs like backups, notifications, and system maintenance. In the context of Django applications, task scheduling can be integrated at multiple levels — from basic system cron jobs executing Django management commands to advanced asynchronous scheduling with tools like Celery and `django-celery-beat`.

This module explores the various methods of scheduling and automating tasks in Django. Learners will gain hands-on experience using system crontabs, `django-cron`, and Celery to implement reliable and maintainable background processes.

---

#### Learning Objectives

By the end of this module, learners will be able to:

-   Explain what cron jobs are and their role in task automation.
-   Write and schedule cron jobs using the system crontab.
-   Implement recurring tasks using `django-cron` in Django projects.
-   Configure and use Celery for asynchronous and periodic task scheduling.
-   Understand the strengths and limitations of each approach.
-   Apply best practices for debugging and managing automated tasks.

---

#### Learning Outcomes

After completing this lesson, learners should be able to:

-   Schedule and manage cron jobs using `crontab`.
-   Create custom Django management commands for scheduled tasks.
-   Use `django-cron` to define and run cron jobs within the Django ecosystem.
-   Set up Celery with `django-celery-beat` for scalable, distributed task scheduling.
-   Monitor, debug, and secure scheduled processes in production.

---

#### Key Concepts

Concept

Description

Crontab Syntax

Defines when a command should be run, using 5 time fields and a command.

System Cron + Django

Uses native system scheduling to run Django commands on a schedule.

`django-cron`

A library to define scheduled jobs inside Django apps.

Celery & Celery Beat

An asynchronous task queue with support for periodic execution.

Log Management

Redirection of task output to logs for easier monitoring and debugging.

---

#### Best Practices for Using Crons in Django

Area

Best Practice

Scheduling

Use absolute paths in cron jobs to avoid environment-related issues.

Debugging

Redirect output (`>> /log/path.log 2>&1`) to capture logs for each job.

Frequency

Avoid frequent jobs that can strain the system; batch where possible.

Access Control

Use `cron.allow` and `cron.deny` for user-level access restrictions.

Celery Tasks

Keep them idempotent to prevent errors on retries.

Monitoring

Use admin dashboards or custom alerts for task failures in production.

---

#### Tools & Libraries

-   **cron (crontab)**: Native job scheduler on Unix systems  
    
-   **django-cron**: Schedule and manage cron jobs within Django  
    
-   **Celery**: Distributed task queue for asynchronous and periodic jobs  
    
-   **django-celery-beat**: Scheduler for managing periodic Celery tasks via Django Admin  
    
-   **Supervisord/Systemd**: Tools to keep Celery workers alive  
    

---

#### Real-World Use Cases

-   Automatically clearing expired sessions or tokens in a Django app.  
    
-   Generating daily reports or email digests for users.  
    
-   Archiving logs or cleaning up old database records.  
    
-   Asynchronously sending notifications and webhooks at scheduled intervals.  
    
-   Running intensive background tasks during off-peak hours.

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

##### 0\. Task 0: Schedule a Customer Cleanup Script

mandatory

Score: 100.0% (Checks completed: 100.0%)

##### Objective

Set up a GraphQL endpoint and define your first schema and query.

##### Instructions

**1\. Create a Shell Script:** \* Create a shell script `clean_inactive_customers.sh` in the `crm/cron_jobs` directory. \* The script should:

-   Use Django’s `manage.py` shell to execute a Python command that deletes customers with no orders since a year ago.
-   Log the number of deleted customers to a `/tmp/customer_cleanup_log.txt` with a `timestamp`.
-   Include a shebang (`#!/bin/bash)` and ensure the script is executable (`chmod +x`).

**2\. Create a Crontab Entry:**

-   Create a file`crm/cron_jobs/customer_cleanup_crontab.tx`t with a single line specifying the cron job to run the script every Sunday at 2:00 AM.
-   Ensure no extra newlines in the file.

**Repo:**

-   GitHub repository: `alx-backend-graphql_crm`
-   File: `clean_inactive_customers.sh, customer_cleanup_crontab.txt`

Check submission View results

##### 1\. Schedule a GraphQL-Based Order Reminder Script

mandatory

Score: 0.0% (Checks completed: 0.0%)

##### Objective

Create a Python script that uses a GraphQL query to find pending orders (order\_date within the last week) and logs reminders, scheduled to run daily using a cron job.

##### Instructions

1.  Create a Python Script:
2.  Create `send_order_reminders.py` in `crm/cron_jobs.`
3.  The script should:
4.  Use the gql library to query the GraphQL endpoint `(http://localhost:8000/graphql)` for orders with order\_date within the last 7 days.
5.  Log each order’s ID and customer email to `/tmp/order_reminders_log.txt` with a timestamp.
6.  Print `"Order reminders processed!"`to the console.
    
7.  Create a Crontab Entry:
    
8.  Create `crm/cron_jobs/order_reminders_crontab.txt` with a single line to run the script daily at 8:00 AM.
    
9.  Ensure no extra newlines.
    

**Repo:**

-   GitHub repository: `alx-backend-graphql_crm`
-   File: `send_order_reminders.py, order_reminders_crontab.txt`

Check submission Mark submission : in progress... : an error occurred View results

##### 2\. Heartbeat Logger with django-crontab

mandatory

Score: 100.0% (Checks completed: 100.0%)

##### Objective

Implement a django-crontab job that logs a heartbeat message every 5 minutes to confirm the CRM application’s health, integrating with the GraphQL schema.

##### Instructions

1.  Install `django-crontab`:

-   Add `django-crontab` to requirements.txt.
-   Add `django_crontab` to `INSTALLED_APPS` in`crm/settings.py.`

1.  Define the Cron Job:

-   In `crm/cron.py`, define a function `log_crm_heartbeat` that:
-   Logs a message in the format`DD/MM/YYYY-HH:MM:SS CRM is alive` to`/tmp/crm_heartbeat_log.txt.`
-   Appends to the file (does not overwrite).
    
-   Optionally, queries the GraphQL `hello field` to verify the endpoint is responsive.
    

1.  Configure the Cron Job:

-   In crm/settings.py, add to CRONJOBS:

```

CRONJOBS = [
    ('*/5 * * * *', 'crm.cron.log_crm_heartbeat'),
]

```

**Repo:**

-   GitHub repository: `alx-backend-graphql_crm`
-   File: `crm/cron.py, crm/settings.py, requirements.txt`

Check submission View results

##### 3\. Schedule a GraphQL Mutation for Product Stock Alerts

mandatory

Score: 100.0% (Checks completed: 100.0%)

##### Objective

Create a django-crontab job that runs every 12 hours, uses a GraphQL mutation to update low-stock products (stock < 10), and logs the updates.

##### Instructions

1.  Define a GraphQL Mutation:

-   In `crm/schema.py`, add a `UpdateLowStockProducts` mutation that:
    
    -   Queries products with `stock < 10.`
    -   Increments their stock by 10 (simulating restocking).
    -   Returns a list of updated products and a success message.

1.  Create a Cron Job:

-   In `crm/cron.py`, define `update_low_stock` that:
    
    -   Executes the `UpdateLowStockProducts` mutation via the GraphQL endpoint.
    -   Logs updated product names and new stock levels to `/tmp/low_stock_updates_log.txt` with a timestamp.
-   In `crm/settings.py`, add to `CRONJOBS`:
    

```

CRONJOBS = [
    ('0 */12 * * *', 'crm.cron.update_low_stock'),
]
```

**Repo:**

-   GitHub repository: `alx-backend-graphql_crm`
-   File: `crm/schema.py, crm/cron.py, crm/settings.py`

Check submission View results

##### 4\. Celery Task for Generating CRM Reports

Optional

Score: 100.0% (Checks completed: 100.0%)

##### Objective

Configure a Celery task with Celery Beat to generate a weekly CRM report (summarizing total orders, customers, and revenue) and log it, integrating with the GraphQL schema.

##### Instructions:

**1\. Set Up Celery:**

-   Add `celery` and `django-celery-beat` to `requirements.txt.`
-   Add `django_celery_beat` to INSTALLED\_APPS in `crm/settings.py.`
-   Create `crm/celery.py` to initialize the Celery app with Redis as the broker (`redis://localhost:6379/0`).
-   Update `crm/__init__.py` to load the Celery app.

**2\. Define the Celery Task:**

-   In `crm/tasks.py`, define a task `generate_crm_report` that:
-   Uses a GraphQL query to fetch: \* Total number of customers. \* Total number of orders. \* Total revenue (sum of `totalamount` from orders).
-   Logs the report to`/tmp/crm_report_log.txt` with a timestamp in the format `YYYY-MM-DD HH:MM:SS - Report: X customers, Y orders, Z revenue.`

**3\. Schedule with Celery Beat:**

-   In `crm/settings.py`, configure:

```
CELERY_BEAT_SCHEDULE = {
    'generate-crm-report': {
        'task': 'crm.tasks.generate_crm_report',
        'schedule': crontab(day_of_week='mon', hour=6, minute=0),
    },
}
```

**4\. Document Setup:**

Create `crm/README.md` with steps to:

-   Install`Redis` and dependencies.
-   Run migrations (`python manage.py migrate`).
-   Start Celery worker (`celery -A crm worker -l info`).
-   Start Celery Beat (`celery -A crm beat -l info`).
-   Verify logs in `/tmp/crm_report_log.txt.`

**Repo:**

-   GitHub repository: `alx-backend-graphql_crm`
-   File: `crm/celery.py, crm/tasks.py, crm/settings.py, crm/__init__.py, requirements.txt, crm/README.md`

