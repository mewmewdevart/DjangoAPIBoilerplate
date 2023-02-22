## Walkthrough
### How to install + Architecture of a Django Project


### How to start
1. Create and activate our virtual environment
```bash
$ python3 -m venv .venv

$ . .venv/bin/activate
```

2. Select the python interpreter <br>
  Check if your IDE have the Python Interpreter actived <br>
  https://www.jetbrains.com/help/pycharm/configuring-python-interpreter.html#view_list


3. Install Django, Rest_Framework and Corsheaders
```bash
$ pip install django djangorestframework django-cors-headers

# create the file with the install list to run the project
$ pip freeze > requieriments.txt
```

4. Create the project folder and the api folder
```bash
$ django-admin startproject api_root .

$ django-admin startapp api_rest .
```

//I need edited it
Your structure need to be like: <br>

Folder Structure/ <br>
- api_root (Project Folder) <br>
-   setting.py General settings <br>
-   urls.py Link the application <br>

- api_rest (Application Folder) <br>
-   models.py Create models for the database <br>
-   admin.py Configure model editing <br>
-   serializers.py Generate JSONs of models <br>
-   views.py API functions <br>
-   urls.py Link functions

5. Add the path of the installed components, the corsheaders middleware, and the origin in api_root/settings.py




---


### Tasks list
- [x] Users api CRUD endpoints
- [x] DRF JWT Authentication
- [x] Add docker configurations
- [ ] Document folder structure
- [ ] Configure Static/media & templates
- [ ] Integrate material ui & react js on templates
 
#### Jwt token endpoint
Method | Endpoint | Functionanlity
--- | --- | ---
POST | `/api-token-auth` | Request jwt token

#### User Endpoints

Method | Endpoint | Functionality
--- | --- | ---
GET | `/api/user` | List users
POST | `/api/user/create` | Creates a user
GET | `/api/user/profile/{pk}` | Retrieve a user
PUT | `/api/user/update/{pk}` | Edit a user
DELETE | `/api/user/destroy/{pk}` | Delete a user


### Installation 
If you wish to run your own build, you two options
 1. User Docker compose.
    
    `$ git clone https://github.com/p8ul/django-rest-framework-boilerplate`
    
    `$ cd django-rest-framework-boilerplate`    
    `$ docker-compose up`
 
 2. Without docker
 
First ensure you have python globally installed in your computer. If not, you can get python [here](python.org).

After doing this, confirm that you have installed virtualenv globally as well. If not, run this:

    $ pip install virtualenv
Then, Git clone this repo to your PC

    $ git clone https://github.com/p8ul/django-rest-framework-boilerplate
    $ cd django-rest-framework-boilerplate
Create a virtual environment

    $ virtualenv .venv && source .venv/bin/activate
Install dependancies

    $ pip install -r requirements.txt
Make migrations & migrate

    $ python manage.py makemigrations && python manage.py migrate
Create Super user
    
    $ python manage.py createsuperuser

### Launching the app
    $ python manage.py runserver

### Run Tests
    $ python manage.py test



