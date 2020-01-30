- [Django  Commands](#django-commands)
  - [Install pipenv](#install-pipenv)
  - [Create Venv](#create-venv)
  - [Install Django](#install-django)
  - [Create project](#create-project)
  - [Run server on http: 127.0.0.1:8000 (ctrl+c to stop)](#run-server-on-http-1270018000-ctrlc-to-stop)
  - [Run initial migrations](#run-initial-migrations)
  - [Using the shell](#using-the-shell)
  - [Create admin user](#create-admin-user)
  - [Create test app](#create-test-app)
  - [To activate this project's virtualenv](#to-activate-this-projects-virtualenv)
  - [Youtube Tutorial](#youtube-tutorial)

# Django  Commands

## Install pipenv
```
pip install **pipenv**
```

## Create Venv
```
pipenv shell
```

## Install Django
```
pipenv install django
```

## Create project
```
django-admin startproject NolimitsApp
cd NolimitsApp
```

## Run server on http: 127.0.0.1:8000 (ctrl+c to stop)
```
python manage.py runserver
```

## Run initial migrations
```
python manage.py migrate
```

## Using the shell
```
python manage.py shell

>>>  from polls.models import Question, Choice
>>>  from django.utils import timezone
>>>  Question.objects.all()
>>>  q = Question(question_text="What is your favorite Python Framework?", pub_date=timezone.now())
>>>  q.save()
>>>  q.id
>>>  q.question_text
>>>  Question.objects.all()
>>>  Question.objects.filter(id=1)
>>>  Question.objects.get(pk=1)
>>>  q = Question.objects.get(pk=1)
>>>  q.choice_set.all()
>>>  q.choice_set.create(choice_text='Django', votes=0)
>>>  q.choice_set.create(choice_text='Flask', votes=0)
>>>  q.choice_set.create(choice_text='Flask', votes=0)
>>>  q.choice_set.all()
>>>  quit()
```

## Create admin user
```
python manage.py createsuperuser
or
winpty python manage.py createsuperuser

[Help](https://stackoverflow.com/questions/32532900/not-able-to-create-super-user-with-django-manage-py)
```

## Create test app
```
python manage.py startapp test
```

## To activate this project's virtualenv
```
run pipenv shell.
Alternatively, run a command inside the virtualenv with pipenv run.
```

## Youtube Tutorial

[Setup Python Django with PostgreSQL](https://www.youtube.com/watch?v=Axh8rNKgvmk)
