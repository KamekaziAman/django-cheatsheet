# Django Setup Guide

## 1. Create and Activate Virtual Environment

```bash
python -m venv .venv
.venv\Scripts\activate
```

## 2. Install Django

```bash
pip install django
django-admin startproject NAME
python manage.py runserver
```

---

## 3. Install Django Tailwind

```bash
python -m pip install django-tailwind
```

### Update `settings.py`

```python
INSTALLED_APPS = [
  # other Django apps
  'tailwind',
]
```

### Initialize Tailwind

```bash
python manage.py tailwind init
```

### Update `settings.py` again

```python
INSTALLED_APPS = [
  # ...
  'theme',
  # ...
]

TAILWIND_APP_NAME = "theme"
INTERNAL_IPS = ["127.0.0.1"]
NPM_BIN_PATH = r"C:\nvm4w\nodejs\npm.cmd"
```

### Install Tailwind dependencies

```bash
python manage.py tailwind install
```

### Add Tailwind to HTML Template

```django
{% load static tailwind_tags %}
...
<head>
   ...
   {% tailwind_css %}
   ...
</head>
```

### Give Setting Template Path

```django
BASE_DIR / "templates"
```

### Start Tailwind

```bash
python manage.py tailwind start
```

---

## 4. Create a Django App

```bash
python manage.py startapp appname
```

---

## 5. Database Setup

```bash
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```

---

## 6. Templates Directory

```text
BASE_DIR / "templates"
```

## 7. prettier ignore File

```text
<!---prettier-ignore--->
```

