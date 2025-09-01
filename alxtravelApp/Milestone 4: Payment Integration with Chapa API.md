# Project: Milestone 4: Payment Integration with Chapa API | Cairo Intranet

### **Overview**

This task focuses on integrating the **Chapa Payment Gateway** into a Django-based travel booking application. Learners will implement secure payment initiation, verification, and status handling for bookings. The workflow covers creating models for payment tracking, API endpoints for initiating and verifying payments, and integrating background email notifications upon successful payment.

### **Learning Objectives**

By the end of this task, learners will be able to:

-   Configure and securely store API credentials for third-party payment gateways.
-   Create Django models to manage and track payment transactions.
-   Build API endpoints for payment initiation and verification.
-   Implement payment workflows integrated into a booking system.
-   Handle payment status updates and transaction logging.
-   Test payment flows using a sandbox environment.

### **Learning Outcomes**

Upon completing this task, learners will be able to:

-   Successfully connect a Django application to the Chapa API.
-   Initiate payments and direct users to secure payment pages.
-   Verify payment statuses and update records accordingly.
-   Send automated confirmation emails after successful transactions.
-   Demonstrate a fully functional and tested payment flow in a booking context.

### **Key Concepts**

-   **API Integration** – Connecting Django with the Chapa API for payment processing.
-   **Secure Credential Management** – Storing API keys in environment variables.
-   **Django Models** – Structuring and persisting payment transaction data.
-   **HTTP Requests** – Sending POST and GET requests to initiate and verify payments.
-   **Asynchronous Tasks** – Using Celery for sending confirmation emails.
-   **Error Handling** – Managing failed or incomplete payments gracefully.

### **Tools and Libraries**

-   **Django** – Backend framework for building the application.
-   **PostgreSQL** – Database for persisting bookings and payment data.
-   **Chapa API** – Payment gateway for initiating and verifying transactions.
-   **Requests** – Python library for making API calls to Chapa.
-   **Celery** – For background email sending after successful payment.
-   **dotenv** – For managing environment variables securely.

### **Additional Resources**

-   [Online Payment Gateway Integration: A Thorough Guide](/rltoken/k1vt9qrsc_CPqin05pQDrA "Online Payment Gateway Integration: A Thorough Guide")
-   [Integrating Payment Gateways in Django: A Guide for E-Commerce Projects](/rltoken/GH0czZ2k6ZSUErfT2N__8g "Integrating Payment Gateways in Django: A Guide for E-Commerce Projects")

### **Real-World Use Case**

Payment processing is a critical feature in online booking systems, e-commerce platforms, and subscription-based services. This task simulates integrating a **real-world payment gateway (Chapa)** into a **travel booking application**. The workflow mirrors industry standards, covering secure payment initiation, transaction tracking, verification, and automated communication, skills essential for professional backend development in fintech, travel, and e-commerce solutions.

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

##### 0\. Integration of Chapa API for Payment Processing in Django

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Objective**

Integrate the Chapa API for handling payments, allowing users to make bookings with secure payment options. Configure the API to initiate and verify payments and handle the payment status accordingly.

**Instructions**

-   **Duplicate Project**:
    
    -   Duplicate the project `alx_travel_app_0x01` to `alx_travel_app_0x02`
-   **Set Up Chapa API Credentials:**
    
    -   Create an account with Chapa (https://developer.chapa.co/) to obtain the API keys.
    -   Store the API keys in environment variables for security (`CHAPA_SECRET_KEY`).
-   **Create Payment Model:**
    
    -   In `listings/models.py`, create a `Payment` model to store payment-related information such as booking reference, payment status, amount, and transaction ID.
-   **Create Payment API View:**
    
    -   In `listings/views.py`, create an API endpoint that initiates the payment by making a POST request to the Chapa API with booking details.
    -   Upon initiating the payment, store the transaction ID returned by Chapa and set the initial status to “Pending.”
-   **Verify Payment**:
    
    -   Add an endpoint in the API to verify the payment status with Chapa after a user completes a payment.
    -   Update the payment status in the `Payment` model based on the verification response from Chapa (e.g., “Completed” or “Failed”).
-   **Implement Payment Workflow:**
    
    -   When a user creates a booking, initiate the payment process and provide them with a link to complete the payment via Chapa.
    -   On successful payment, send a confirmation email to the user (using Celery for background tasks).
    -   Handle any errors or payment failures gracefully, updating the status in the `Payment` model accordingly.
-   **Test Payment Integration**:
    
    -   Use Chapa’s sandbox environment to test payment initiation and verification.
    -   Ensure the entire payment workflow functions correctly, from initiation to status verification.

**Note:** Include screenshots or logs demonstrating successful payment initiation, verification, and status update in the Payment model.

**Repo:**

-   GitHub repository: `alx_travel_app_0x02`
-   Directory: `alx_travel_app`
-   File: `listings/views.py, listings/models.py,README.md`

Check submission View results

##### 1\. Manual Review

mandatory

Score: 100.0% (Checks completed: 100.0%)

**Repo:**

-   GitHub repository: `alx_travel_app_0x02`
-   Directory: `alx_travel_app`
