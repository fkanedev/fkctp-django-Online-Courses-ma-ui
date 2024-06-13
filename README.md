![Python](https://img.shields.io/badge/Python-3.9-blue.svg)
![Built with Django](https://img.shields.io/badge/Built%20with-Django-b5f05d.svg)
[![Authentication with Django](https://img.shields.io/badge/Authentication%20with-Django-green.svg)](https://docs.djangoproject.com/en/stable/topics/auth/)
[![Session Management with Django](https://img.shields.io/badge/Session%20Management-Django-yellow.svg)](https://docs.djangoproject.com/en/stable/topics/http/sessions/)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

# Online Course Application

An online platform developed using Django for managing courses, user authentication, and student enrollment. It includes features for course creation, lesson management, and an assessment feature for evaluating students.

## Table of Contents
1. [Introduction](#introduction)
2. [Technologies Used](#technologies-used)
3. [Installation and Configuration](#installation-and-configuration)
4. [Usage](#usage)
5. [Development](#development)
   - [Project Structure](#project-structure)
   - [Templates](#templates)
   - [Views](#views)
   - [Models](#models)
6. [Sources](#sources)
7. [License](#license)
8. [Contact](#contact)

## 1. Introduction

### Project Objective
The primary objective of this project is to develop a comprehensive online course management system using the Django framework. The system is designed to facilitate course creation, management, and student enrollment while ensuring robust user authentication and assessment capabilities.

### Key Features
- **Course Management**: Allows instructors to create, update, and manage courses efficiently.
- **User Authentication**: Provides secure login and registration functionalities for users.
- **Enrollment Management**: Enables students to enroll in courses, access course materials, and manage their enrollments.
- **Assessment Feature**: Integrates a system for instructors to create and manage assessments for their courses, allowing students to take and receive feedback on assessments.

## 2. Technologies Used

### Programming Languages
- **Python**: The core language used for backend development with Django.

### Tools and Frameworks
- **Django**: A high-level Python web framework that encourages rapid development and clean, pragmatic design.
- **SQLite**: A lightweight, disk-based database used for local development.
- **Bootstrap**: Utilized for responsive front-end design.

## 3. Installation and Configuration

### Prerequisites
Before setting up the project, ensure that you have the following installed on your local machine:
- **Python 3.x**: The latest version of Python.
- **Pip**: Python's package installer.

### Installation Steps
1. **Clone the repository**:
   ```sh
   git clone https://github.com/fkanedev/fkctp-tmp1
   cd fkctp-tmp1
   ```
2. Install the dependencies:
  ```bash
   pip install -r requirements.txt
   ```
### Environment Setup
- Use manage.py for server management operations.
## 4. Usage
### Running the Server
To start the development server, navigate to the project directory and run:
   ```bash
   python manage.py runserver
   ```
This command will start the server at http://127.0.0.1:8000/.

### Accessing the Application
Once the server is running, open your web browser and go to http://127.0.0.1:8000/ to access the application. You will be able to register as a new user, log in, and explore the course management features.

## 5. Development
### Project Structure
- myproject/: The main Django project directory containing settings and configurations.
- onlinecourse/: Contains the core application responsible for course-related functionalities.
- static/: Holds static files such as CSS and JavaScript.

### Templates
The project uses Django's templating system for rendering HTML. The main templates include:
- course_list.html: Displays a list of available courses, including course titles and brief descriptions.
- course_detail.html: Shows detailed information about a specific course, such as the full course description, instructor details, and enrolled students.
- course_add.html: Provides a form for instructors to create new courses.
- login.html: A login form for user authentication.
- registration.html: A registration form for new users.

These templates are located in onlinecourse/templates/onlinecourse/ and leverage Django template tags and Bootstrap for styling and layout.

### Views
View functions in onlinecourse/views.py handle HTTP requests and render appropriate templates. Key view functions include:
- course_list: Retrieves and displays a list of all courses.
- course_detail: Displays detailed information about a single course based on its ID.
- course_create: Handles the creation of new courses by instructors.
- user_login: Manages user authentication and login process.
- user_registration: Manages new user registration.

These views utilize Django's powerful request handling and template rendering capabilities to dynamically generate content based on user interactions and database queries.

### Models
Django models in onlinecourse/models.py define the structure of the database tables. Key models include:
- Course: Represents a course with fields for title, description, and instructor. This model also includes methods for course-related operations.
- Lesson: Represents individual lessons within a course, with fields for title, content, and associated course.
- Instructor: Stores information about instructors, including user details and courses taught.
- Learner: Stores information about learners, including user details and enrolled courses.

The models are defined using Django's ORM, which provides a high-level abstraction for database operations, making it easy to create, retrieve, update, and delete records.

### Static Files
The static directory contains all static files used in the project, such as:
- CSS: For styling HTML templates.
- style.css: Custom styles for the application.
- JavaScript: For interactive features and client-side validation.
- script.js: Custom scripts for enhanced user interactions.
- Images: Any images used in the application.

These files are served by Django during development and can be collected and served by a web server in a production environment.

## 6. Sources <a name="sources"></a>

- **Template: [IBM Developer Skills Network - Cloud App Development template](https://github.com/ibm-developer-skills-network/final-cloud-app-with-database)**

- **Useful links**:
  - **[Django Application Development with SQL and Databases](https://www.coursera.org/learn/developing-applications-with-sql-databases-and-django/home/week/5)**
  - **[IBM Full Stack Software Developer Professional Certificate](https://www.coursera.org/professional-certificates/ibm-full-stack-cloud-developer)**

## 7. License <a name="license"></a>

This project is licensed under the MIT License - see the [LICENSE](/LICENSE) file for details.

## 8. Contact <a name="contact"></a>

### Contact Information :

- Send me email : **fkanecloudtech@gmail.com**
- Connect with me on [LinkedIn](https://www.linkedin.com/in/your-profile/)
- Visit my [portfolio](https://yourname.github.io) to explore my projects and services.


### Contribution and Support :

Contributions are welcome. Please refer to the [CONTRIBUTING](/CONTRIBUTING) file for more information on how to contribute.
