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

