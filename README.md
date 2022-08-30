**NOTE**: everything in \<brackets> refers to the name for that part of *your* project!

TERMINAL:  
pipenv install django  
pipenv shell  
django-admin startproject \<config> .  
django-admin startapp \<myApp>  
code .

VS CODE:  
\<myApp>/models.py:  
add import:  
```
from django.contrib.auth.models import AbstractUser
```
create model:  
```
class User(AbstractUser):
    pass
```

\<config>/settings.py:  
add AUTH_USER_MODEL:  
```
AUTH_USER_MODEL = '\<myApp>.User'
```

TERMINAL:  
python manage.py makemigrations  
python manage.py migrate  
python manage.py runserver  
(or `./man[TAB]` instead of `python manage.py`)
