# django-notebook

**Contents:**

# Start a project

### 1. Create a Virtual Environment

> Make a directory/Folder for your project. Open a Command Prompt(cmd) on that folder & Type:

```
python -m venv <environment_name>
```

### 2. Acive the Virtual Environment

```
cd <env name>/Scripts/activate.bat
```

### 3. Install Django and Make a project

```
pip install django

django-admin startproject <project_name>

cd <project_name>
```

*Open the project folder in a IDE*

### 4. Migration and runserver

```
python manage.py makemigrations

python manage.py migrate

python manage.py runserver
```

*Visit http://127.0.0.1:8000 from your browser.*

### 5. Create a superuser

```
python manage.py createsuperuser
username: <username> 
email: <email> 
password: <pass>
```

*Visit http://127.0.0.1:8000/admin from your browser. Use your username & password to login.*

### 6. Start an app

```
python manage.py startapp <app_name>
```

*A folder has been created on your project directory with some files..*

Go to `setting.py` in project folder & add your `app name` to `INSTALLED_APPS` variable.

```python
  INSTALLED_APPS = [
    .
	  .

    'app_name',
  ]
```


# Add Templates, Static and Media File

### 1. Add Templates File

> Make a directory/Folder in project root named `templates`.
> goto `settings.py` find `TEMPLATES` variable and add the following code

```python
TEMPLATES = [
    {
    	.
	.
        'DIRS': [os.path.join(BASE_DIR, 'templates')],
        .
    },
]
```

### 2. Add static File

> Make a directory/Folder in project root named `static`.
> goto `settings.py` add the following code at the end

```python
STATIC_URL = '/static/'
STATICFILES_DIRS = (
   os.path.join(BASE_DIR, 'static'),
)
```

### 3. Add media file

> Make a directory/Folder in project root named `media`.
> goto `settings.py` add the following code at the end

```python
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```
> goto `urls.py` add the following code

```python
urlpatterns = [
   .
   .
] + static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)

```
