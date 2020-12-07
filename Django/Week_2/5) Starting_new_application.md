# :star2: Django Application:
  - ## In Django there are two important concepts
       ## :star: **Projects**
       ## :star: **Applications**
  - ## **Project**:
      - It is a collection of configurations and apps. One project can be composed of multiple apps, or a single app.
  - ## **Application**:
      - It is a Web application that does something. An app usually is composed of a set of models (database tables), views, templates, tests.
  - ## Note:
      - We cannot able to run the App without Project.
  To create our first app, go to the directory where the manage.py file is and executes the following command:
  ```sh
  django-admin startapp boards
  ```
  - This is the following directory structure for myapp:
  
  ```sh
  myproject/
 |-- myproject/
 |    |-- boards/                <-- our new django app!
 |    |    |-- migrations/
 |    |    |    +-- __init__.py
 |    |    |-- __init__.py
 |    |    |-- admin.py
 |    |    |-- apps.py
 |    |    |-- models.py
 |    |    |-- tests.py
 |    |    +-- views.py
 |    |-- myproject/
 |    |    |-- __init__.py
 |    |    |-- settings.py
 |    |    |-- urls.py
 |    |    |-- wsgi.py
 |    +-- manage.py
 +-- venv/
  ```
- **migrations/**: here Django store some files to keep track of the changes you create in the models.py file, so to keep the database and the models.py synchronized.
- **admin.py**: this is a configuration file for a built-in Django app called Django Admin.
- **apps.py**: this is a configuration file of the app itself.
- **models.py**: here is where we define the entities of our Web application. The models are translated automatically by Django into database tables.
- **tests.py**: this file is used to write unit tests for the app.
- **views.py**: this is the file where we handle the request/response cycle of our Web application.
