# Project: IP Tracking: Security and Analytics | Cairo Intranet

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

Week 11

Week 11

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

## Security And Analytics

[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=102426)[

IP Tracking: Security and Analytics

](/projects/102426)

## Milestone 6

[

How PLDs Work (Step-by-Step) - Get it started!

](/concepts/111449?project_id=101646)[

Milestone 6: Deployment and Documentation

](/projects/101646)

# IP Tracking: Security and Analytics

-   Weight: 1
-   Project will start Sep 1, 2025 1:00 AM, must end by Sep 8, 2025 1:00 AM
-   **Manual QA review must be done** (request it when you are done with the project)
-   An auto review will be launched at the deadline

#### Overview

IP tracking is a critical technique for enhancing security, understanding user behavior, and maintaining legal compliance in web applications. In Django, this can be implemented via middleware, asynchronous tasks, and integrations with external services. This module explores how to log, blacklist, geolocate, and analyze IP addresses responsibly and efficiently.

Learners will gain practical experience using Django tools and best practices to build secure and privacy-conscious IP tracking systems that scale.

---

#### Learning Objectives

By the end of this module, learners will be able to:

-   Understand the role of IP tracking in web security and analytics.
-   Implement request logging using Django middleware.
-   Blacklist malicious IPs and manage access control efficiently.
-   Use IP geolocation to enhance personalization and fraud detection.
-   Apply rate limiting techniques to prevent abuse.
-   Detect anomalies using log data and basic machine learning.
-   Address privacy, compliance, and ethical considerations.

---

#### Learning Outcomes

After completing this lesson, learners should be able to:

-   Build middleware to log IP addresses and request metadata.
-   Integrate third-party geolocation APIs and manage usage efficiently.
-   Implement rate limiting using Django or Redis-based solutions.
-   Blacklist and manage harmful IPs through Django models or caching systems.
-   Detect suspicious behavior through log analysis and scheduled tasks.
-   Maintain compliance with GDPR/CCPA through anonymization and data retention.
-   Balance security with user experience and fairness.

---

#### Key Concepts

Concept

Description

IP Logging

Logs IPs, timestamps, and request paths for auditing and debugging.

Blacklisting

Blocks known bad actors from accessing the application.

IP Geolocation

Maps IPs to geographic data to improve security and UX.

Rate Limiting

Prevents abuse by restricting request rates.

Anomaly Detection

Identifies unusual traffic patterns to catch early threats.

Privacy & Ethics

Ensures tracking aligns with legal and ethical standards.

---

#### Best Practices for IP Tracking in Django

Area

Best Practice

Performance

Use Redis or batch logging to avoid DB bottlenecks.

Privacy

Anonymize or truncate IPs before storage.

Debugging

Log selectively and rotate logs to manage disk usage.

Compliance

Update your privacy policy and limit retention duration.

Rate Limiting

Differentiate limits for anonymous vs. authenticated users.

Anomaly Detection

Tune thresholds carefully to reduce false positives.

---

#### Tools & Libraries

-   **Django Middleware**: Intercepts and logs request data  
    
-   **Celery**: Offloads intensive IP tasks like anomaly detection or geolocation  
    
-   **django-ipware**: Retrieves the client IP address reliably, even behind proxies  
    
-   **django-ratelimit**: Simple decorators for request rate control  
    
-   **Redis**: Used for fast lookup of blacklisted IPs and rate limiting  
    
-   **ipinfo.io / GeoIP2**: APIs and databases for IP geolocation  
    
-   **scikit-learn**: For basic machine learning in anomaly detection  
    

---

#### Real-World Use Cases

-   Logging access to sensitive endpoints like `/admin`  
    
-   Blocking spam bots or scrapers from specific IP ranges  
    
-   Redirecting users to localized versions of the site based on their region  
    
-   Identifying abnormal request spikes from a single IP  
    
-   Enforcing API rate limits on freemium or public services  
    
-   Building dashboards to visualize request origins geographically  
    

---

#### Ethical and Legal Considerations

-   **Privacy Regulations (GDPR/CCPA)**: Always anonymize and disclose tracking practices.  
    
-   **Transparency**: Include clear data usage policies and options for users to opt out.  
    
-   **Bias Awareness**: Avoid blanket blocking of regions; use fine-grained logic.  
    
-   **Retention Policies**: Implement auto-deletion of logs after a safe period.  
    

---

Effective IP tracking in Django balances performance, security, and ethics. With the right tools and approach, developers can create scalable systems that protect users and enhance visibility, all while maintaining compliance and trust.

## Tasks

##### 0\. Task 0: Basic IP Logging Middleware

mandatory

##### Objective:

Implement middleware to log the IP address, timestamp, and path of every incoming request.

##### Instructions

1.  Create `ip_tracking/middleware.py` with a middleware class that logs request details.
2.  Define`ip_tracking/models.py` with a `RequestLog` model (fields`: ip_address`,`timestamp`, `path`).
3.  Register the middleware in `settings.py.`

**Repo:**

-   GitHub repository: `alx-backend-security`
-   Directory: `ip_tracking`
-   File: `ip_tracking/middleware.py, ip_tracking/models.py`

##### 1\. Task 1: IP Blacklisting

mandatory

##### Objective:

Implement IP blocking based on a blacklist.

##### Instructions

1.  Create `ip_tracking/models.py` with a `BlockedIP` model (field: `ip_address`).
2.  Modify `ip_tracking/middleware.py` to block requests from IPs in `BlockedIP`. Return `403 Forbidden.`
3.  Create `ip_tracking/management/commands/block_ip.py`to add IPs to`BlockedIP`.

**Repo:**

-   GitHub repository: `alx-backend-security`
-   Directory: `ip_tracking`
-   File: `ip_tracking/middleware.py, ip_tracking/management/commands/block_ip.py`

##### 2\. Task 2: IP Geolocation Analytics

mandatory

##### Objective:

Enhance logging with geolocation data (country, city).

##### Instructions

1.  Install `django-ipgeolocation`.
2.  Extend `RequestLog` in `ip_tracking/models.py` with `country` and `city` fields.
3.  Update `ip_tracking/middleware.py` to populate these fields using the `geolocation API`. Cache results for`24` hours.

**Repo:**

-   GitHub repository: `alx-backend-security`
-   Directory: `ip_tracking`
-   File: `ip_tracking/models.py, ip_tracking/middleware.py`

##### 3\. Task 3: Rate Limiting by IP

mandatory

##### Objective:

Implement rate limiting to prevent abuse.

##### Instructions

1.  Install `django-ratelimit`.
2.  Configure rate limits: 10 requests/minute (authenticated), 5 requests/minute (anonymous).
3.  Apply the rate limit to a sensitive view (e.g., login) in `ip_tracking/views.py`. Configure in `settings.py.`

**Repo:**

-   GitHub repository: `alx-backend-security`
-   Directory: `ip_tracking`
-   File: `ip_tracking/views.py, settings.py`

##### 4\. Task 4: Anomaly Detection

mandatory

##### Objective:

Implement anomaly detection to flag suspicious IPs.

##### Instructions

1.  Create a Celery task in`ip_tracking/tasks.py` to run hourly.
2.  The task should flag IPs exceeding 100 requests/hour or accessing sensitive paths (e.g., `/admin`, `/login`).
3.  Create`ip_tracking/models.py`with a `SuspiciousIP` model (fields: `ip_address`, `reason`).

**Repo:**

-   GitHub repository: `alx-backend-security`
-   Directory: `ip_tracking`
-   File: `ip_tracking/tasks.py, ip_tracking/models.py`

Ready for a review

[

Back

](/concepts/111449?project_id=102426)

[

Next

](/concepts/111449?project_id=101646)

Copyright © 2025 ALX, All rights reserved.