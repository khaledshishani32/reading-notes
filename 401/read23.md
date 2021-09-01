#  Custom User Model
---
#### Django ships with a built-in User model for authentication and if you'd like a basic tutorial on how to implement log in, log out, sign up and so on see the Django Login and Logout tutorial for more.

#### ESetup

#### To start, create a new Django project from the command line. We need to do several things:

- create and navigate into a dedicated directory called accounts for our code
- install Django
- make a new Django project called config
- make a new app accounts
- start the local web server

#### commands to run:
```        
$ cd ~/Desktop
$ mkdir accounts && cd accounts
$ pipenv install django~=3.1.0
$ pipenv shell
(accounts) $ django-admin.py startproject config .
(accounts) $ python manage.py startapp accounts
(accounts) $ python manage.py runserver
```
 
#### AbstractUser vs AbstractBaseUser

#### Creating our initial custom user model requires four steps:

- update config/settings.py
- create a new CustomUser model
- create new UserCreation and UserChangeForm
- update the admin

![](https://miro.medium.com/max/1000/1*NJPSvC--Lk65_M0lRdB4dg.png)
---
### config/settings.py
```
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'accounts', # new
]
...
AUTH_USER_MODEL = 'accounts.CustomUser' # new
```

### Superuser

#### It's helpful to create a superuser that we can use to log in to the admin and test out log in/log out. On the command line type the following command and go through the prompts.

```
$ python manage.py createsuperuser

```

### Templates/Views/URLs

#### Our goal is a homepage with links to log in, log out, and sign up. Start by updating settings.py to use a project-level templates directory.
### config/settings.py
```
TEMPLATES = [
    {
        ...
        'DIRS': [str(BASE_DIR.joinpath('templates'))], # new
        ...
    },
]
```

        
