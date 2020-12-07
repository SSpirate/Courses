# :star2: Printing Hello World:
  - We defined a simple view called home which simply returns a message saying Hello, World!.
  - Now we have to tell Django when to serve this view. It’s done inside the urls.py file:

**urls.py**:  
  ```sh
  from django.conf.urls import url
  from django.contrib import admin

  from boards import views

  urlpatterns = [
    url(r'^$', views.home, name='home'),
    url(r'^admin/', admin.site.urls),
  ]
  ```
- But for now, Django works with regex to match the requested URL. For our home view, I’m using the ^$ regex, which will match an empty path, which is the homepage (this url: http://127.0.0.1:8000). If I wanted to match the URL http://127.0.0.1:8000/homepage/, my url would be: url(r'^homepage/$', views.home, name='home').  

- Now run Django using this Command given below:
```sh
python manage.py runserver
```
- Lets see the Output:

![Output](https://simpleisbetterthancomplex.com/media/series/beginners-guide/1.11/part-1/hello-world.png)
