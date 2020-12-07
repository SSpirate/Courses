# :star2:Configuring The Application:
  - Let’s configure our project to use it.
  - - Using the analogy of the square and circles from the previous comic ,the yellow circle would be our boards app, and the django.contrib.admin, django.contrib.auth, etc, would be the red circles.

- To do that, open the settings.py and try to find the INSTALLED_APPS variable:
    - **settings.py**
    - - Just add our **boards** app to the list of INSTALLED_APPS:
    ```sh
    INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'boards', # Added line
     ]
    ```

- Let’s just experiment how it looks like to create a new page with Django.

- Open the views.py file inside the boards app, and add the following code:
  - **views.py**
    ```sh
    from django.http import HttpResponse

    def home(request):
      return HttpResponse('Hello, World!')
    ```
- Views are Python functions that receive an HttpRequest object and returns an HttpResponse object. Receive a request as a parameter and returns a response as a result. That’s the flow you have to keep in mind!  
