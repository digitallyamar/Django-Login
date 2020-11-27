# Django-Login
A simple repo to provide Registration, Login &amp; Logout functions for Django Apps

# Step 1: Create Django project called DJLogin & an accounts App
        
        - We will use the default sqlite DB so skip installing Djongo
        - We will make use of crispyforms

        python3 -m venv venv
        source venv/bin/activate

        pip install django django-crispy-forms

        django-admin startproject DJLogin .

        django-admin startapp accounts

        python3 manage.py migrate

        python3 manage.py startserver

        By this time, you should have your default Django server up and running.

# Step 2: Create form and view for user registration inside accounts app

        - Create a new file called forms.py.
        - Create NewUserForm class in forms.py with extra "email" field and the save method.
        - Create template HTML file called register.html under templates/accounts directory.
        - Add entries to INSTALLED_APPS in settings.py with values:
            'accounts',
            'crispy_forms',


# Step 3: Add support for login and logout functionality

        - We will include logout link as part of the nav bar which will get enabled only if a user has logged in.