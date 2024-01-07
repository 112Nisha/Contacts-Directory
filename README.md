# Contacts Directory

This web application is designed to manage and organize information about students and faculty within IIIT Hyderabad. It allows for easy access to student and faculty details and provides functionalities to update existing information, add new entries, and search the database efficiently.

## Getting Started

To run this application:
- Clone the repository.
- Run `app.py`.
- Open the generated link in any web browser.

## Usage

### Home Page

Upon accessing the application, the home page (`index.html`) welcomes users with institute photos and relevant information. Also provided are options to navigate to the following:
- Student Database: Accesses the student information page.
- Faculty Database: Accesses the faculty information page.

### Student Database

The Student Information Page displays the following student details: 
- Roll number
- Phone number
- CGPA
- House
- Branch

#### Functionalities

- **Update Student Information:**
  Requires a unique key for authentication before allowing updates to student details (name, phone, email). 
- **Add Student:**
  Allows the addition of new student information. Reserved for admin office and is authenticated using a specific key (`appaji_key`). 
- **Find a Student:**
  Enables searching the database based on various parameters such as name, email, phone, house, branch, and CGPA.

### Faculty Database

The Faculty Information Page shows the following faculty details: 
- Name
- Email
- Phone number
- Major Research area
- Office hours
- Office

#### Functionalities

- **Update Faculty Information:**
  Requires a key (e.g., `aftab_key`) possessed by all faculty members for updating their information.
- **Add Faculty:**
  Allows the addition of new faculty information. Restricted to admin access with a specific key. 
- **Find a Faculty:**
  Enables filtering based on fields like name, email, phone number, major research area, office hours, and office.

## Security Measures

### Key Authentication

Certain functionalities (update/add) require a specific key for authorization, preventing unauthorized access. For our website, we have given this as the id in the database. It can be manipulated by a hash function to generate stronger keys, or we can have a password field in the database that will be randomly generated.

### Webpage Inspection Protection

Measures are in place to safeguard keys from being revealed through webpage inspection, ensuring site security.
