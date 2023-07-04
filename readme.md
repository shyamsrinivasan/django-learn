# Steps for initiliazing a Django app
1. Test if Django is installed `python -m django --version`
2. Create a Django project `django-admin startproject myapp`
The above step creates the root `myapp` directory that behaves as a project container, the subdirectory `myapp` (initialized as python package) and the `manage.py` module
3. Verification: change to outer `myapp` directory and run `python manage.py runserver`. To verify the Django project works, go to `http://127.0.0.1:8000` (the default localhost) on the web browser. Alternatively, the ip address and port can be specified using `python manage.py runserver 0.0.0.0:8000`
4. Create an (one or more) app inside the project to import as a top-level module by changing to the outer `myapp` directory and running `python manage.py startapp newapp`.
This will create a newapp dirctory (initialized as a python package) with all relevant files to get started.
5. Create all necessary database tables (based on INSTALLED_APPS) by running `python manage.py migrate`
6. After defining all models for `newapp` in `newapp.models.py`, run `python manage.py makemigrations newapp` to create/change database models.
To see the SQL commands executed by the `migrate` command, run `python manage.py sqlmigrate poll xxx`
