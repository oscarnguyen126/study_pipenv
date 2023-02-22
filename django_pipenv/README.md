I. Install pipenv

* sudo apt update
* sudo pip install pipenv

II. Create virtual environment with pipenv
 
* pipenv --python [version]

III. Install django

* pipenv install django

Startproject

* django-admin startproject [project_name]

Startapp

* django-admin startapp [app_name]

IV. Connect with psql

1. pipenv install psycopg2
2. Edit settings.py

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'django_app_pipenv',
]

DATABASES = {
        'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': '[db_name]', 
        'USER': '[db_user]', 
        'PASSWORD': [db_password],
        'HOST': '127.0.0.1', 
        'PORT': '5432',
    }
}

3. python manage.py makemigrations
4. python manage.py migrate

V. Install gunicorn

* pipenv install gunicorn







