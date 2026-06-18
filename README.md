# Secure Task Management Application (secure-task-app)

An implementation of an injection-free, role-based Task Management web application built using secure-by-design architectural paradigms. This project serves as the major assessment for **IKB 21503: Secure Software Development** at UniKL MIIT.

## 1. Project Description
The **Secure Task Management Application** is a collaborative system for managing workflows, task assignments and tracking progress securely. This application is build using the Python **Django** framework and focuses on addressing OWASP Top 10 vulnerabilities. 

Rather than relying purely on passive framework automation, this system actively integrates robust input sanitization pipelines, strict multi-tenant data boundaries, structural session security and continuous third-party vulnerability remediation to guarantee the confidentiality, integrity, and availability of system state profiles.

## 2. Security Features Summary
This application implements the following security controls aligned with OWASP ASVS:
* **Input Validation:** Strict regex and built-in validators to prevent injection attacks.
* **Authentication & Session Security:** Enforced session timeouts (30 mins), HttpOnly cookies and strict password complexity validators.
* **Access Control (RBAC):** Strict data isolation between standard "Users" and "Admins" to prevent Insecure Direct Object Reference (IDOR).
* **Sensitive Data Protection:** Cryptographic secrets and debug variables are strictly decoupled from version control using `.env` files.
* **Output Encoding:** Enforced Django template auto-escaping to mitigate Stored XSS and HTML Injection vectors.
* **Audit Logging:** Centralized recording of security events (logins, task modifications, profile updates) with IP tracking.

## 3. Dependencies
This project operates on Python 3.10+ and Django. All third-party dependencies are tracked in `requirements.txt` and have been cleared by **Snyk** Software Component Analysis (SCA) to ensure supply chain security.
Core packages include:
* `Django`
* `django-environ` (For secure secret management)


## 4. Installation Steps
1. **Clone the Project Repository:**
   ```bash
   git clone https://github.com/denniiyyy/secure-task-app-django.git
   cd secure-task-app-django
   ```
2. Initialize Local Virtual Environment:
   ```bash
   python -m venv venv
   ```
3. Activate Environment Context:
   ```bash
   venv\Scripts\activate
   ```
4. Provision Third-Party Modules:
   ```bash
   pip install -r requirements.txt
   ```
5. Environment Configuration:
   Rename the provided `.env.example` file to `.env`
   
6. Execute Relational Schema Migrations:
   ```bash
   python manage.py migrate
   ```
7. How to Run the App:
   ```bash
   python manage.py runserver
   ```
## Admin Credentials
   username: `admin1`
   password: `Admin123!`
   
## System Screenshots

 <img width="1857" height="991" alt="image" src="https://github.com/user-attachments/assets/a630b10a-1712-4ce1-bec8-0928ec9e4383" />

<img width="1897" height="927" alt="image" src="https://github.com/user-attachments/assets/65b5c7b2-fc06-49bb-bf45-e59f475a93bb" />

<img width="1897" height="932" alt="image" src="https://github.com/user-attachments/assets/2d7ae8e9-5039-4a87-8f99-a5a99b2b8755" />

<img width="1916" height="927" alt="image" src="https://github.com/user-attachments/assets/2d8ef403-6ef2-4e95-a3d9-ef864e4a60fe" />

<img width="1897" height="930" alt="image" src="https://github.com/user-attachments/assets/6a246d07-51df-443d-a299-1305c77a1d98" />

<img width="1917" height="931" alt="image" src="https://github.com/user-attachments/assets/723c18fa-56d3-49e5-9937-5446aa9c9b5f" /> 
