# :star2: Starting A New Project
  - To start a new Django project, run the command below:
  ```sh
  django-admin startproject myproject
  ```
  - After we run the command above, it will generate the base folder structure for a Django project.
  ```sh
  myproject/                  <-- higher level folder
 |-- myproject/             <-- django project folder
 |    |-- myproject/
 |    |    |-- __init__.py
 |    |    |-- settings.py
 |    |    |-- urls.py
 |    |    |-- wsgi.py
 |    +-- manage.py
 +-- venv/                  <-- virtual environment folder
 ```
  - Initially the project consists of Five Files those are:
    - **manage.py**: a shortcut to use the django-admin command-line utility. It’s used to run management commands related to our project. We will use it to run the development server, run tests, create migrations and much more.
    - **__init__.py**: this empty file tells Python that this folder is a Python package.
    - **settings.py**: this file contains all the project’s configuration. We will refer to this file all the time!
    - **urls.py**: this file is responsible for mapping the routes and paths in our project. For example, if you want to show something in the URL /about/, you have to map it here first.
    - **wsgi.py**: this file is a simple gateway interface used for deployment. You don’t have to bother about it. Just let it be for now.
 -  Django comes with a simple web server installed. It’s very convenient during the development, so we don’t have to install anything else to run the project locally. We can test it by executing the command:
 ```sh
 python manage.py runserver
 ```
- Now open the following URL in a Web browser: http://127.0.0.1:8000 and you should see the following page:
![Page](https://simpleisbetterthancomplex.com/media/series/beginners-guide/1.11/part-1/it-worked.png)
