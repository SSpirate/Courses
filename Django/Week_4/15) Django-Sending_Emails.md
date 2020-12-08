# :star2:Django-Sending_Emails:
  - Django comes with a ready and easy-to-use light engine to send e-mail.
  - We need to import of smtplib inorder to utilize this Django-Sending_Emails.
  - In Django you just need to import django.core.mail.
  - To start sending e-mail, edit your project settings.py file and set the following options −

* EMAIL_HOST − smtp server.

* EMAIL_HOST_USER − Login credential for the smtp server.

* EMAIL_HOST_PASSWORD − Password credential for the smtp server.

* EMAIL_PORT − smtp server port.

* EMAIL_USE_TLS or _SSL − True if secure connection.

## Sending a Simple E-mail
  - Let's create a "SimpleEmail" view to send a e-mail.
  ```sh
  from django.core.mail import send_mail
  from django.http import HttpResponse

  def sendSimpleEmail(request,emailto):
    res = send_mail("hello SSpirate", "How r u", "polo@gmail.com", [emailto])
    return HttpResponse('%s'%res)
  ```
- Here is the details of the parameters of send_mail −

  - subject − E-mail subject.

  - message − E-mail body.

  - from_email − E-mail from.

  - recipient_list − List of receivers’ e-mail address.

  - fail_silently − Bool, if false send_mail will raise an exception in case of error.

  - auth_user − User login if not set in settings.py.

  - auth_password − User password if not set in settings.py.

  - connection − E-mail backend.

  - html_message − (new in Django 1.7) if present, the e-mail will be multipart/alternative.

- Let's create a URL to access our view −
```sh
from django.conf.urls import patterns, url

urlpatterns = paterns('myapp.views', url(r'^simpleemail/(?P<emailto>
   [\w.%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,4})/', 
   'SimpleEmail' , name = 'SimpleEmail'),)
```
- So when accessing /myapp/simpleemail/polo@gmail.com, you will get the following page −

![Link](https://www.tutorialspoint.com/django/images/sending_simple_email.jpg)
