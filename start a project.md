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
