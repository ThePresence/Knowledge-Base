
# Poetry

### Create a new project folder and step in:
```
$ mkdir djangodemo
$ cd djangodemo
```

### Create a basic pyproject.toml with django as dependency:

```
$ poetry init --no-interaction --dependency django
```

### Create venv with all dependencies needed:

```
$ poetry install
```

### Init your demo-project
```
$ poetry run django-admin.py startproject djangodemo
```

### Poetry Shell
```
poetry shell
```

### Installing new dependencies
```
poetry add django-allauth
```
