# :star2:Django-Models:
-  A model is a class that represents table or collection in our DataBase, and where every attribute of the class is a field of the table or collection. Models are defined in the app/models.py.
- A model is the single, definitive source of information about your data. It contains the essential fields and behaviors of the data you’re storing. Generally, each model maps to a single database table.
## Creating a Model:
  - Few things to make sure in django are:
      - Each model should be a subclass of **django.db.models.Model** class.
      - Each model attribute maps to the corresponding table attribute.
  - Example For Model is given below:
      ```sh
      from django.db import models
      class Person(models.Model):
      first_name = models.CharField(max_length=30)
      last_name = models.CharField(max_length=30)
      ```
      - Every model inherits from django.db.models.Model.
      - Our class has 2 attributes (2 CharField), those will be the table fields.
  - If u have Database Software such as SQL,SQLite linked with Model use the given command below
      ```sh
      python manage.py syncdb
      ```
  - Or create Database and link with the Models
      ```sh
        CREATE TABLE myapp_person (
        "id" serial NOT NULL PRIMARY KEY,
        "first_name" varchar(30) NOT NULL,
        "last_name" varchar(30) NOT NULL
        );
      ```
## Note:
  - The name of the table, myapp_person, is automatically derived from some model metadata but can be overridden.
  - An id field is added automatically, but this behavior can be overridden. See Automatic primary key fields.
  - The CREATE TABLE SQL in this example is formatted using PostgreSQL syntax, but it’s worth noting Django uses SQL tailored to the database backend specified in your settings file.
   
   
