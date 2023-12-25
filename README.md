# django-starter
# install Django

## Setting up  Virtual Environment  (env) 
- `pip install virtualenv` 
- `virtualenv your_env`
- activate (linux) env `source your_envname/scripts/activate`
## Install Django
- `pip install django`
- `django-admin` to see all command line

## Create Django Project
- `django-admin startproject project_name`
-  Run `python manage.py` to see all command line  in `manage.py`

## Run project
- `python manage.py runserver` with default port
-  `python manage.py runserver 8080` with specific port

## Create app in Django project 
- `python startapp app_name`
### Registeration Routers
- create file `views.py` 
		`from django.shortcuts import render` 
		`from django.http import HttpResponse`	
		`/create your view with function`
		`def home(request):`
		`reutrn HttpResponse('something you wants to display')`

### Route mapping 
- firstly, register in app and after that register in **main** router
- import your view here `urls.py`
- `urlpatterns  = [ path(' ' ,views.home), ... any route here]` in **app directory**
- `urlpatterns  = [ path(' ' ,include( 'app-name.urls')` **main** **directory**
