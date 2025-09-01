### **Overview**

This task guides learners through creating essential backend components in Django by defining database models, setting up serializers for API data representation, and implementing a management command to seed the database. By working on the duplicated `alx_travel_app_0x00` project, learners will gain practical experience in structuring relational data, serializing it for API endpoints, and programmatically populating the database with sample data to simulate real-world application scenarios.

### **Learning Objectives**

By the end of this task, learners should be able to:

1.  **Model relational data** in Django using appropriate fields, relationships, and constraints.
2.  **Create serializers** to transform Django model instances into JSON for API responses.
3.  **Implement a management command** to automate database seeding.
4.  **Test and validate** database population using Django’s command-line tools.

### **Learning Outcomes**

Learners will be able to:

-   Define models such as `Listing`, `Booking`, and `Review` with correct relationships (e.g., ForeignKey, OneToMany).
-   Use Django REST Framework (DRF) serializers to prepare model data for APIs.
-   Write and execute a seeding script to insert realistic sample data into the database.
-   Apply database seeding to streamline development and testing workflows.

### **Key Concepts**

-   **Django Models** – Mapping Python classes to database tables.
-   **Relationships** – Implementing one-to-many and many-to-one associations between models.
-   **Constraints** – Ensuring data integrity with validation rules.
-   **Serializers** – Converting complex data types into JSON for APIs using DRF.
-   **Management Commands** – Extending Django’s CLI to perform custom tasks.
-   **Database Seeding** – Populating databases with sample or default data.

### **Tools & Libraries**

-   **Django** – Backend framework for building the application.
-   **Django REST Framework (DRF)** – For creating API serializers and endpoints.
-   **SQLite/PostgreSQL** – Database engines for storing data.
-   **Python** – Programming language for backend logic and scripts.

### **Real-World Use Case**

In a travel booking platform, developers need to design data structures for listings (properties available for booking), customer bookings, and user reviews. Serializers ensure this data can be delivered via APIs to mobile or web clients. During development, seeding the database with sample listings allows frontend developers and testers to work with realistic data without manually creating entries, significantly speeding up the development lifecycle and ensuring consistent test scenarios.

### Additional Resources:

-   [Relationships in Django](/rltoken/nD8STVuaBziR7L2abNFujg "Relationships in  Django")
-   [Django Models Documentation](/rltoken/gjDi6U_A6r1zfzjNq5YVig "Django Models Documentation")
-   [Data Seeding & Initial Data](/rltoken/jTHh2Skdu5qWwKWRmaP6GQ "Data Seeding & Initial Data")
-   [Using django-seed](/rltoken/phmpPrxNOgnGPXTF1IG3lg "Using django-seed")

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

##### 0\. Database Modeling and Data Seeding in Django

mandatory

Score: 0.0% (Checks completed: 0.0%)

**Objective**

Define the database models, create serializers for API data representation, and implement a management command to seed the database.

**Instructions**

-   **Duplicate Project:**
    
    -   Duplicate the project `alx_travel_app` to `alx_travel_app_0x00`
-   **Create Models**:
    
    -   In `listings/models.py`, define `Listing, Booking`, and `Review` models based on the provided structure.
    -   Each model should have appropriate fields, relationships, and constraints.
-   **Set Up Serializers:**
    
    -   Create serializers in `listings/serializers.py` for `Listing` and `Booking` models.
-   **Implement Seeders:**
    
    -   Create a management command in `listings/management/commands/seed.py` to populate the database with sample listings data.
-   **Run Seed Command:**
    
    -   Test the seeder by running the command to populate the database with sample data.

**Repo:**

-   GitHub repository: `alx_travel_app_0x00`
-   Directory: `alx_travel_app`
-   File: `listings/models.py, listings/serializers.py, listings/management/commands/seed.py, README.md`

Check submission View results

##### 1\. Manual Review

mandatory

**Repo:**

-   GitHub repository: `alx_travel_app_0x00`
-   Directory: `alx_travel_app`
