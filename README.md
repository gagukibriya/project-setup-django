Login Functionality With Django

Project Setup

1. Clone the Repository
Create a GitHub repository and clone it using:

    git clone https://github.com/gagukibriya/Login-Functionality-With-Django.git

Change the directory:

    cd Login-Functionality-With-Django

Open the project in VS Code:

    code .

2. Setup Virtual Environment
Create a virtual environment:

    python -m venv venv

Set execution policy:

    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

Activate the virtual environment:

    venv/Scripts/activate
3. Install Django

    pip install Django

Check Django version:

    django-admin --version

4. Create Django Project
Create a Django project named config:

    django-admin startproject config .

5. Create Django Apps
Create two apps named account and tasks:

    python manage.py startapp account
    python manage.py startapp tasks

Add both apps to INSTALLED_APPS in settings.py.

    INSTALLED_APPS = [
        'django.contrib.admin',
        'django.contrib.auth',
        'django.contrib.contenttypes',
        'django.contrib.sessions',
        'django.contrib.messages',
        'django.contrib.staticfiles',
        'account',
        'tasks',
    ]

Database Configuration (PostgreSQL)
6. Create a Database
    Create a database on your PostgreSQL server.

7. Connect Database with Django
Update the DATABASES configuration in settings.py:

    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql',
            'NAME': 'login-with-django',
            'USER': 'postgres',
            'PASSWORD': 'YOUR_PASSWORD',
            'HOST': 'localhost',
            'PORT': '5432',
        }
    }

8. Install Psycopg
    python -m pip install --upgrade "psycopg[binary]"

Check the database server connection.
    Django Admin Panel Setup

9. Create Superuser
    python manage.py createsuperuser
Enter your username and password.

10. Run Django Development Server
    python manage.py runserver

11. Access Django Admin Panel
Open the following URL:
    http://127.0.0.1:8000/admin/

Log in using your superuser credentials.