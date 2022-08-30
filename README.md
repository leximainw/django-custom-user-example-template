**NOTE**: everything in \<brackets> refers to the name for that part of *your* project!

__**TERMINAL:**__  
pipenv install django  
pipenv shell  
django-admin startproject \<config> .  
django-admin startapp \<myApp>  
code .

__**VS CODE:**__  
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
AUTH_USER_MODEL = '<myApp>.User'
```

__**TERMINAL:**__  
python manage.py makemigrations  
python manage.py migrate  
python manage.py runserver  
(or `./man[TAB]` instead of `python manage.py`)
