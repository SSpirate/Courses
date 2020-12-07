# :star2: Admin Interface:
  - Django provides a ready-to-use user interface for administrative activities. We all know how an admin interface is important for a web project. Django automatically generates admin UI based on your project models.

:star: **Starting The Admin Interface**:
  - The Admin interface depends on the django.countrib module. To have it working you need to make sure some modules are imported in the INSTALLED_APPS and MIDDLEWARE_CLASSES tuples of the myproject/settings.py file.

:star: **Configuring the INSTALLED_APPS and MIDDLEWARE_CLASSES to make admin interface**:  
  - For INSTALLED_APPS make sure you have −
    
 ```sh
    - INSTALLED_APPS = (
   'django.contrib.admin',
   'django.contrib.auth',
   'django.contrib.contenttypes',
   'django.contrib.sessions',
   'django.contrib.messages',
   'django.contrib.staticfiles',
   'myapp',
    )
 ```
  
  - For MIDDLEWARE_CLASSES make sure you have−
```sh
    MIDDLEWARE_CLASSES = (
   'django.contrib.sessions.middleware.SessionMiddleware',
   'django.middleware.common.CommonMiddleware',
   'django.middleware.csrf.CsrfViewMiddleware',
   'django.contrib.auth.middleware.AuthenticationMiddleware',
   'django.contrib.messages.middleware.MessageMiddleware',
   'django.middleware.clickjacking.XFrameOptionsMiddleware',
    )
```
- Before launching your server, to access your Admin Interface, you need to initiate the database −

```sh
$ python manage.py migrate
```
- syncdb will create necessary tables or collections depending on your db type, necessary for the admin interface to run. Even if you don't have a superuser, you will be prompted to create one.

- If you already have a superuser or have forgotten it, you can always create one using the following code 
```sh
$ python manage.py createsuperuser
```
- **Configuring myproject/url.py for Admin Interface.The url.py should be like the code given below:**
  ```sh
  from django.conf.urls import patterns, include, url

  from django.contrib import admin
  admin.autodiscover()

  urlpatterns = patterns('',
  url(r'^admin/', include(admin.site.urls)),
  )

  ```
