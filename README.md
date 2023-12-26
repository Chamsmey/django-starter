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
## Create template

To create template you need to create a folder **template** inside your app directory `accounts/templates/accounts`
**Noted** :  *inside templates directory should be name same your app directory name*
Don't forget to register your app in *settings.py* 
`INSTALLED_APPS = [..., 'account']`


# inheritance template 

That mean we can use template in everywhere you want.
**Parent template** ` {% block your_block_name %} // open tag`
*NOte* : 

/// you can pass child template here 

`{% endblock } // end your_block_name`

**Child template** `{% extends 'parent_directory'%}`
or you  use include to pass something inside your template 
`{% include 'your_template_here' %} ` 
## Render temlplate 

`def home(request) : 
	return render(request, 'your_temlplate_here') `
