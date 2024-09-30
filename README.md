![Python 3.9](https://img.shields.io/badge/Python-3.9-blue.svg)
![Built with Django](https://img.shields.io/badge/Built%20with-Django-brightgreen.svg)
![Authentication - Django](https://img.shields.io/badge/Authentication-Django-blue.svg)
![Session Management - Django](https://img.shields.io/badge/Session%20Management-Django-orange.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)

# Online Course Application
This project involves developing an online platform using Django for managing courses, user authentication, student enrollment and an assessment feature for evaluating students. It demonstrates the practical application of Django in a real-world scenario. It's part of my training in the [IBM Full Stack Software Developer Professional Certificate](https://www.coursera.org/professional-certificates/ibm-full-stack-cloud-developer) utilizing a [template](https://github.com/ibm-developer-skills-network/final-cloud-app-with-database) provided by IBM Developer Skills Network.

# Topics

`Python`, `Django`, `Online Course Management`, `Authentication`, `Session Management`, `Student Enrollment`, `Assessment Feature`, `Course Management`, `SQLite`, `Bootstrap`, `Web Development`, `Django Models`, `Django Views`, `Django Templates`, `IBM Full Stack Software Developer Professional Certificate`, `Git`, `GitHub`, `REST API`, `ORM`, `MIT License`

## Table of Contents
1. [Introduction](#introduction)
2. [Technologies Used](#technologies-used)
3. [Installation and Configuration](#installation-and-configuration)
4. [Usage](#usage)
5. [Development](#development)
   - Project Structure
   - Templates
   - Views
   - Models
6. [Sources](#sources)
7. [License](#license)
8. [Contact](#contact)

## 1. Introduction <a name="introduction"></a>

### Project Objective
The primary objective of this project is to develop a comprehensive online course management system using the Django framework. The system is designed to facilitate course creation, management, and student enrollment while ensuring robust user authentication and assessment capabilities.

### Key Features
- **`Course Management`** : Allows instructors to create, update, and manage courses efficiently.
- **`User Authentication`** : Provides secure login and registration functionalities for users.
- **`Enrollment Management`** : Enables students to enroll in courses, access course materials, and manage their enrollments.
- **`Assessment Feature`** : Integrates a system for instructors to create and manage assessments for their courses, allowing students to take and receive feedback on assessments.

## 2. Technologies Used <a name="technologies-used"></a>

### Programming Languages
- **Python** : The core language used for backend development with Django.

### Tools and Frameworks
- **Django** : A high-level Python web framework that encourages rapid development and clean, pragmatic design.
- **SQLite** : A lightweight, disk-based database used for local development.
- **Bootstrap** : Utilized for responsive front-end design.

## 3. Installation and Configuration <a name="installation-and-configuration"></a>

### Prerequisites
Before setting up the project, ensure that you have the following installed on your local machine:
- **Python 3.x** : The latest version of Python.
- **Pip** : Python's package installer.

### Installation Steps
1. **Clone the repository**:
   ```sh
   git clone https://github.com/fkanedev/fkctp-django-Online-Courses-ma-ui
   cd fkctp-django-Online-Courses-ma-ui
   ```
2. Install the dependencies:
  ```bash
   pip install -r requirements.txt
   ```
### Environment Setup
- Use manage.py for server management operations.
## 4. Usage <a name="usage"></a>
### Running the Server
To start the development server, navigate to the project directory and run:
   ```bash
   python manage.py runserver
   ```
This command will start the server at http://127.0.0.1:8000/.

### Accessing the Application
Once the server is running, open your web browser and go to http://127.0.0.1:8000/ to access the application. You will be able to register as a new user, log in, and explore the course management features.

## 5. Development <a name="development"></a>
### Project Structure 
- **myproject/** : The main Django project directory containing settings and configurations.
- **onlinecourse/** : Contains the core application responsible for course-related functionalities.
- **static/** : Holds static files such as CSS and JavaScript. These files are served by Django during development and can be collected and served by a web server in a production environment.

### Templates
The project uses Django's templating system for rendering HTML. Templates are located in [onlinecourse/templates/onlinecourse](https://github.com/fkanedev/fkctp-django-Online-Courses-ma-ui/blob/master/onlinecourse/templates/onlinecourse) include:
- **user_login_bootstrap.html** : A login form for user authentication.
- **user_registration_bootstrap.html** : A registration form for new users.
- **course_list_bootstrap.html** : Displays a list of available courses, including course titles and brief descriptions.
- **course_detail_bootstrap.html** : Shows detailed information about a specific course, such as related lessons. If user is authenticated, show course exam with a list of question.
- **exam_result_bootstrap.html** : Display exam results, with passed or failed info and final score.

These templates leverage Django template tags and Bootstrap for styling and layout.

### Views
View functions in [onlinecourse/views.py](https://github.com/fkanedev/fkctp-django-Online-Courses-ma-ui/blob/master/onlinecourse/views.py) handle HTTP requests and render appropriate templates. Key view functions include:
- **views.registration_request** : Manages new user registration.
- **views.login_request** and **views.logout_request** : Manages user authentication, login and logout process.
- **views.CourseListView.as_view()** : Retrieves and displays a list of all courses.
- **views.enroll** : Creates an enrollment for authenticated user.
- **views.CourseDetailView.as_view()** : Displays detailed information about a single course and related exam.
- **views.submit : Creates an** exam submission record.
- **views.show_exam_result** : Checks if learner passed exam, shows their question results and final score.

These views utilize Django's powerful request handling and template rendering capabilities to dynamically generate content based on user interactions and database queries.

### Models
Django models in [onlinecourse/models.py](https://github.com/fkanedev/fkctp-django-Online-Courses-ma-ui/blob/master/onlinecourse/models.py) define the structure of the database tables. Key models include:

- **Course** : Represents a course with fields for name, image, description, publication date, instructors, and total enrollment. This model also includes a flag to check if the course is enrolled.  
- **Lesson** : Represents individual lessons within a course, with fields for title, order, content, and associated course.
- **Instructor** : Stores information about instructors, including a foreign key to the user model, full-time status, and total number of learners.
- **Learner** : Stores information about learners, including a foreign key to the user model, occupation, date of birth, and social link.
- **Enrollment** : Links users to courses with fields for enrollment date, mode, and rating.
- **Question** : Used to persist question content for a course, with a foreign key to the course, grade points, and question text. Includes a method to check if the learner's selected choices are correct.
- **Choice** : Stores choices for a question, with fields for choice text and a flag indicating if it is correct.
- **Submission** : Links an enrollment to multiple choices, allowing the tracking of learner answers.

The models are defined using Django's ORM, which provides a high-level abstraction for database operations, making it easy to create, retrieve, update, and delete records.


## 6. Sources <a name="sources"></a>

- **Template : [IBM Developer Skills Network - Cloud App Development template](https://github.com/ibm-developer-skills-network/final-cloud-app-with-database)**

- **Useful links** :
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
