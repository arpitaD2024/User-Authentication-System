# User Authentication System

This project is a Django web application focused on user authentication and management. It allows users to sign up, log in, and access a personalized welcome page. The application is designed to provide a user-friendly interface for managing user accounts.

## Description

This Django 5.0 project provides user authentication (login and signup) and displays a welcome message upon successful login.  It utilizes HTML templates for the user interface and interacts with a database (SQLite by default, with MySQL also referenced in the code).

**Important:** This project is for educational purposes and contains security vulnerabilities (see below). Do not use it in a production environment without addressing these weaknesses.

## Features

*   User registration (signup).
*   User login.
*   Error handling for user authentication (e.g., missing accounts, invalid credentials).
*   Welcome page displaying user information upon successful login.
*   Admin interface for managing user data (via Django admin).

## Key Files and Functionality

*   `myapp/models.py`: Currently empty. This file is intended for defining the database models for your application (e.g., User model, profile information, etc.).
*   `myapp/views.py`: Contains the logic for handling user interactions, including login (`login_action`) and signup.  It connects to a MySQL database for user data (though SQLite is the default database in settings).  The `login_action` function handles POST requests for login, retrieves user credentials, queries the database, and renders either the welcome page or the error page.
*   `templates/`: Holds the HTML templates for the user interface:
    *   `login_page.html`: The login form.
    *   `signup_page.html`: The signup form.
    *   `weclcome.html`: The welcome page displayed after successful login.
    *   `error.html`: The error page displayed for authentication issues.
*   `myproject/settings.py`: Contains the configuration for the Django project, including database settings (currently SQLite), installed apps, middleware, and template settings.
*   `myproject/urls.py`: Defines the URL routing for the application, mapping URLs to specific views.
*   `myapp/admin.py`: Used to register models with the Django admin interface, allowing you to manage your data through a web interface.

## Installation

1.  Clone the repository:

    ```bash
    git clone <https://github.com/arpitaD2024/User-Authentication-System/>
    ```
2.  Navigate to the project directory:

    ```bash
    cd myproject
    ```
3.  Install the required packages:

    ```bash
    pip install -r requirements.txt  # Create requirements.txt using: pip freeze > requirements.txt
    ```
4.  Run database migrations:

    ```bash
    python manage.py migrate
    ```

## Usage

1.  Start the development server:

    ```bash
    python manage.py runserver
    ```
2.  Open your web browser and go to `http://127.0.0.1:8000/`.
3.  Use the login page to authenticate or register a new account.

