
## Features

1. Login/Sign Up.
2. JWT Authentication.
3. OTP Verification.
4. Add Equipment details related to various categories like Crop Protection, Harvesting Equipment,etc
5. Search equipments of a particular category using the title.
6. Filter equipment based on their category, price, availability, etc.
7. Book and rent equipment for off-season.
8. Track booking requests.
10. View the list of comments and replies related to particular posts.
11. LimitOffsetPagination for custom pagination style.
12. Support Centre
13. Chat with owner and customer.


**Installing venv (required once)**

**Windows**
```
py -m pip install --user virtualenv
py -m venv env
```
**Linux**
```
python3 -m pip install --user virtualenv
python3 -m venv env
```

You have to start virtual environment everytime you start new terminal -

**Windows**

Using gitbash
```
. env/Scripts/activate
```
Using Powershell
```
. env\Scripts\activate
```
**Linux**
```
source env/bin/activate
```

#### Installing Requirements 

**Windows**
```
pip install -r requirements/base.txt
pip install -r requirements/local.txt
```
**Linux**
```
pip install -r requirements/base.txt
pip install -r requirements/local.txt
```
#### Setting up Environment File

**Configuring Environment Variables**

Make environment file by copying the example file -
```
cd .envs/.local
cp .django .env
cp .postgres .env
``` 

#### Migrating Database
**Windows**
```
py manage.py migrate
```
**Linux**
```
python3 manage.py migrate
```

#### Create Superuser
**Windows**
```
py manage.py createsupeser
```
**Linux**
```
python3 manage.py createsupeser
```

### Starting Development Server
**Windows**
```
py manage.py runserver
```
**Linux**
```
python3 manage.py runserver
``` 

### Leaving the virtual environment
```
deactivate
```

### Update requirements file (Critical)
If you have installed new dependency, the pip freeze command lists the third-party packages and versions installed in the environment. 

**Windows**
```
pip freeze > requirements/local.txt
```
**Linux**
```
pip3 freeze > requirements/local.txt
```

### Update Database  
Everytime you change db models, you need to run makemigrations and migrate to update on database.

**Windows**
```
py manage.py makemigrations
py manage.py migrate
```
**Linux**
```
python3 manage.py makemigrations
python3 manage.py migrate
