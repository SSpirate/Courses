# :star2: Setting Up Environment:
  - ## For Windows Users:
  - **Step 1** – Installing Python:
    - Django is written in 100% pure Python code, so you'll need to install Python on your system. Latest Django version requires Python 2.6.5 or higher
        
```sh
$ python
Python 2.7.5 (default, Jun 17 2014, 18:11:42)
[GCC 4.8.2 20140120 (Red Hat 4.8.2-16)] on linux2
```
Otherwise, you can download and install the latest version of Python from the link
[Python](http://www.python.org/download)
 - **Step 2** - Installing Django:
    - Just open the Command Prompt and type the command given below:
 ```sh
$ pip install django
``` 
To check whether the installation is correct,Just type the command given below
 ```sh
$ django-admin --version
3.1.4
``` 
  - ## For UNIX/Linux Users:
    - - **Step 1** - Installing Python:
      - Type the command given below to install python
```sh
$ sudo apt install python3-pip –y
``` 
```sh
$ update-alternatives --install /usr/bin/pip pip /usr/bin/pip3 1
``` 
- To check whether the installation of pip is correct, Type the command given below
```sh
$ pip –-version
``` 
  - **Step 2** - Installing Django:
    - Type the command given below to install Django
```sh
$ apt show python3-django
``` 
```sh
$ apt install python3-django
``` 
After the completion of Django installation to check whether the Django installed properly just type the command given below.
```sh
$ django-admin –version
``` 
 - ## For Mac Users:
    - **Step 1** Installing Python:
  ```sh
$ brew install python3
```   
 ```sh
$ sudo easy_install pip
```  
 ```sh
$sudo pip install virtualenv
```   
 ```sh
$ virtualenv   filename
```   
 ```sh
$ cd filename
```   
```sh
$ source bin/activate
```   
- **Step2** - Installing Django:
 ```sh
$ sudo pip install django==3.0.1
```  
To check the installation in correct just type the command given below
 ```sh
$ python -m django --version
```  
