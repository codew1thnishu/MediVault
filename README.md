# MediReport

## Web-Based Medical Laboratory Report Management System

MediReport is a web-based Medical Laboratory Report Management System designed to manage patients, laboratory staff, users, and medical laboratory reports through a centralized platform.

The system provides role-based access for Administrators, Laboratory Staff, and Patients. It allows authorized laboratory staff to register patients and upload laboratory reports, while patients can securely view and download their own reports.

---

## Features

### 🔐 Authentication & Authorization

- Secure user login
- Password hashing
- Role-based access control
- Separate access for:
  - Administrator
  - Laboratory Staff
  - Patient
- Unauthorized users are prevented from accessing restricted pages

### 👨‍💼 Administrator

Administrators can:

- Access the Admin Dashboard
- Manage system users
- Add users
- Edit user information
- Manage patient records
- View laboratory reports
- View and manage system data

### 🧪 Laboratory Staff

Laboratory Staff can:

- Access the Lab Staff Dashboard
- Register new patients
- View registered patients
- Upload laboratory reports
- Associate reports with patients
- View reports
- Download reports
- Deactivate reports
- Reactivate reports
- Manage report status

### 👤 Patient

Patients can:

- Register/login to the system
- Access their Patient Dashboard
- View their own laboratory reports
- Open reports
- Download reports
- View report status

Patients cannot access another patient's reports.

---

## Technology Stack

### Frontend

- HTML5
- CSS3
- Bootstrap
- JavaScript

### Backend

- Python
- Flask
- Flask-SQLAlchemy

### Database

- MySQL

### Security

- Werkzeug password hashing
- Flask sessions
- Role-based authorization
- Secure file names for uploaded reports

---

## System Architecture

```text
                    ┌─────────────────────┐
                    │       User          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Web Interface     │
                    │   HTML/CSS/JS        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Flask Backend    │
                    │ Authentication      │
                    │ Authorization       │
                    │ Business Logic      │
                    └──────────┬──────────┘
                               │
                ┌──────────────┴──────────────┐
                ▼                             ▼
       ┌─────────────────┐          ┌─────────────────┐
       │      MySQL      │          │  Report Files   │
       │    Database     │          │ Upload Storage  │
       └─────────────────┘          └─────────────────┘
