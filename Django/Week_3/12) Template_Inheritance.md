# :star2:Template Inheritance and its Uses:
- <ins> **Template Inheritance**</ins>:
    - It is the most powerful – and thus the most complex – part of Django's template engine is template inheritance. 
    - Template inheritance allows you to build a base “skeleton” template that contains all the common elements of your site and defines blocks that child templates can override.A template system cannot be complete without template inheritance.
    - Temporal inheritance helps us to reduce the code size and redundancy.
    - Blocks and Extends Tags is must to introduce Template inheritance.
- **Tutorial for Better Understanding Of Temporal Inheritance:**
    - **Step 1**: We need to create a project in Django, Use the command given below:
    ```sh
    django-admin startproject MyProject
    ```
    - **Step 2**: After creation of the Django Project, you need to migrate your Django Project.
    ```sh
    cd MyProject
    python manage.py migrate
    ```
    - **Step 3**: (URL Routing)Now we need to create an App,I have named my App as news, but you can name it what ever you want.
    ```sh
    python manage.py startapp news
    ```
    - **Step 4**: (Configuration)Also you need to add your newly created app in the Django settings.py INSTALLED_APPS. make sure that always do this process after creating a new App.
    ```sh
      
     INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'contact',
    'news',
     ]   
     ```
     - **Step 5**:We need to just create a templates folder in your project and you need to add some html files. basically we are going to create three html files.
     - **templates/home.html**
    
     ```sh
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>Home</title>
    </head>
    <body>
      <h1> This is our home page</h1>
    </body>
    </html>
    ```
    - **templates/about.html**
    ```sh
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <title>About</title>
    </head>
    <body>
      <h1> This is our about page</h1>
    </body>
    </html>
    ```
    - You can see that in these two html files, we are duplicating the code, and one of the main concept in Django is DRY(Don’t Repeat Yourself). now for solving of this problem we are going to use django Template Inheritance. basically we are going to create another html file at name of base.html.
    - **Step 6**: template/base.html 
    ```sh
   
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>{% block title %}{% endblock %}</title>
    </head>
    <body>
    {% block body %}
 
 
    {% endblock %}
    </body>
    </html>
    ```
    - **Step 7**:Editing the home and about html files to apply Template inheritance.
    **template/home.html**
    ```sh
    
    {% extends 'base.html' %}

    {% block title %} Home {% endblock %}


    {% block body %}

    <h1> This is our home page</h1>

    {% endblock %}
    ```
    **template/about.html**
    ```sh
    {% extends 'base.html' %}

    {% block title %} About {% endblock %}


    {% block body %}

    <h1> This is our about page</h1>

    {% endblock %}
    ```
   
   - **Step 8**:So now open views.py and we need to add our view functions.
    ```sh
      from django.shortcuts import render
     def home(request):
        return render(request, "home.html")
     def about(request):
        return render(request, "about.html")
    ```



   


    
    - **Step 9**:Also We need to create urls,just create a new python file in your news app at name of urls.py and add these codes or edit in Existing urls.py
    ```sh
    from django.urls import path
    from .views import home, about,contact
    from django.urls import path,include
    from django.contrib import admin
 
    urlpatterns = [
      path('', home, name = 'home'),
      path('about/', about, name = 'about'),
      path('contact/', contact, name = 'contact'),
      path('admin/', admin.site.urls),
 
      path('', include('news.urls')),
       ]
    ```
    - **Step 10**: Just run the server
    ```sh
    python manage.py runserver
    ```
    


    
    
    
    
    
    
    
