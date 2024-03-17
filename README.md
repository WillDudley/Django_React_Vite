# Django_React_Vite
Boilerplate for a webapp with a Django backend and React frontend, using Vite.



## Quickstart instructions
The basis for this code was inspired by Leynad21's [tutorial](https://www.youtube.com/watch?v=FdMf_3SurOA). The description of the tutorial includes the following instructions:

### 1) Install and activate virtual environment
In the root folder, on the terminal create a virtual environment.
 Terminal command: `python -m venv env`
 Activate command: `source env/Scripts/activate`

### 2) Creating and setting up Django Project
1. Install django and all the main libraries : 
    1. `pip install django` 
    2. `pip install djangorestframework django-cors-headers`
2. Create project in terminal
   1. `django-admin startproject backend`
3. `cd` to the backend folder
4. Create an app in django in the terminal
    1. `python manage.py startapp [name of the app]`
  
### 3) Create a react app using vite
Go back to the root folder and:
 1. `npm create vite@latest frontend -- --template react`
 2. `cd frontend`
 3. `npm install`

### 4) Open VS code and the run the servers
 1. In the root folder open VS code:
    1. `code .`
 2. Open two terminals and make sure your virtual environment is active
 3. Run django server
    1. `cd` to backend
    2. `python manage.py runserver`
 4. Run react server
    1. `cd` to frontend
    2. `npm run dev`
 
  
### 5) Set up the settings.py to include rest_framework and corsheaders
```
  CORS_ALLOWED_ORIGINS = [
      "http://127.0.0.1:5173",
      "http://localhost:5173",
  ]
  
  Application definition
  
  INSTALLED_APPS = [
      'django.contrib.admin',
      'django.contrib.auth',
      'django.contrib.contenttypes',
      'django.contrib.sessions',
      'django.contrib.messages',
      'django.contrib.staticfiles',
      External Apps
      'rest_framework',
      'corsheaders',
      Internal Apps
      'main',
  ]
  
  MIDDLEWARE = [
      'django.middleware.security.SecurityMiddleware',
      'django.contrib.sessions.middleware.SessionMiddleware',
      "corsheaders.middleware.CorsMiddleware",
      'django.middleware.common.CommonMiddleware',
      'django.middleware.csrf.CsrfViewMiddleware',
      'django.contrib.auth.middleware.AuthenticationMiddleware',
      'django.contrib.messages.middleware.MessageMiddleware',
      'django.middleware.clickjacking.XFrameOptionsMiddleware',
  ]
```