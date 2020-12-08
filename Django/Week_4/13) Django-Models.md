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

      class Dreamreal(models.Model):

      website = models.CharField(max_length = 50)
      mail = models.CharField(max_length = 50)
      name = models.CharField(max_length = 50)
      phonenumber = models.IntegerField()

      class Meta:
          db_table = "dreamreal"
      ```
      - Every model inherits from django.db.models.Model.
      - Our class has 2 attributes (2 CharField), those will be the table fields.
  - If u have Database Software such as SQL,SQLite linked with Model use the given command below
      ```sh
      python manage.py syncdb
      ```
## Manipulating Data (CRUD)   
   -  **C** - Create
   -  **R** - Read
   -  **U** - Update
   -  **D** - Delete
     

   
   
