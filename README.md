# User Interface Design For P.I Works INC.
<hr></hr>

## Purpose Of This Project

In this project, I designed a sample user interface requested by the P.I Works company.
Its interface is from Django, the web development framework of the Python programming language.


### **Project Contents**

<ul>
  <li id="list-item-1"><a href="#UI">UI (Base Folder Of The Project)</a>
    <ul>
      <li id="list-item-static" style = ""font-weight": "bold";"font-size":"80px";">Static</li>
      <li id="list-item-1-1"><a href="#init">__init__.py</a></li> 
      <li id="list-item-1-2"><a href="#asgi">asgi.py</a></li>
      <li id="list-item-1-3"><a href="#settings">settings.py</a></li>
      <li id="list-item-1-4"><a href="#urls">urls.py</a></li>
      <li id="list-item-1-5"><a href="#wsgi">wsgi.py</a></li>
    </ul>  
  </li> 
  <br></br>
  <li id="list-item-2"><a href="#Products">Products (App File)</a>
  	<ul>
      <li id="list-item-2-migrations" style="font-weight: bold;">Migrations</li> 
      <li id="list-item-2-2"><a href="#init2">__init__.py</a></li>
      <li id="list-item-2-3"><a href="#admin">admin.py</a></li>
      <li id="list-item-2-4"><a href="#apps">apps.py</a></li>
      <li id="list-item-2-5"><a href="#models">models.py</a></li>
      <li id="list-item-2-6"><a href="#tests">tests.py</a></li>
      <li id="list-item-2-7"><a href="#views">views.py</a></li>
    </ul>  
  </li>
  <br></br>
  <li id="list-item-3">Admin Interface
  </li>
  <br></br>
  <li id="list-item-4"><a href="#runserver">Run Server And Connect To The User Interface On The Local Host</li>
   
</ul>  
</body>
</html>
<hr></hr>
<h2 id="UI">UI(Base File Of The Project)</h3>

## <h3 id="init">__init__.py</h3>
 - Python defines two types of packages, regular packages and namespace
   packages. Regular packages are traditional packages as they existed
   in Python 3.2 and earlier. A regular package is typically implemented
   as a directory containing an __init__.py file. When a regular package
   is imported, this __init__.py file is implicitly executed, and the
   objects it defines are bound to names in the package’s namespace. The
   __init__.py file can contain the same Python code that any other module can contain, and Python will add some additional attributes to
   the module when it is imported.
<br></br>
## <h3 id="asgi">asgi.py</h3>
 - As well as WSGI, Django also supports deploying on ASGI, the emerging Python standard for asynchronous web servers and applications. Django’s startproject management command sets up a default ASGI configuration for you, which you can tweak as needed for your project, and direct any ASGI-compliant application server to use.
 <br></br>
## <h3 id="settings">settings.py</h3>
 - It is the file that we edit the settings of functions and applications in the general structure of Django and edit when a new application is added. Since we designed a user interface in this project, I made some design applications using Django's ready-made applications.
 - Here is the code that I wrote:
 
 `INSTALLED_APPS = [
    'admin_interface',
    'colorfield',
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'products'
]`
<br></br>
## <h3 id="urls">urls.py</h3>
- When a user requests a page from your Django-powered site, this is the algorithm the system follows to determine which Python code to execute: Django determines the root URLconf module to use. Ordinarily, this is the value of the ROOT_URLCONF setting, but if the incoming HttpRequest object has a urlconf attribute (set by middleware), its value will be used in place of the ROOT_URLCONF setting. Django loads that Python module and looks for the variable urlpatterns. This should be a sequence of django.urls.path() and/or django.urls.re_path() instances. Django runs through each URL pattern, in order, and stops at the first one that matches the requested URL, matching against path_info. Once one of the URL patterns matches, Django imports and calls the given view, which is a Python function (or a class-based view). The view gets passed the following arguments: An instance of HttpRequest. If the matched URL pattern contained no named groups, then the matches from the regular expression are provided as positional arguments. The keyword arguments are made up of any named parts matched by the path expression that are provided, overridden by any arguments specified in the optional kwargs argument to django.urls.path() or django.urls.re_path().
- Here is the code that I wrote 
`from django.contrib import admin
from django.urls import path

`urlpatterns = [
    path('', admin.site.urls),
]`
<br></br>
## <h3 id="wsgi">wsgi.py</h3>
- Django’s primary deployment platform is WSGI, the Python standard for web servers and applications.

- Django’s startproject management command sets up a minimal default WSGI configuration for you, which you can tweak as needed for your project, and direct any WSGI-compliant application server to use.

<hr></hr>
<h2 id="Products">Products (App File)</h3>

## <h2 id="init2">__init__.py (App File __init__)</h3>
- Django’s primary deployment platform is WSGI, the Python standard for web servers and applications.

- Django’s startproject management command sets up a minimal default WSGI configuration for you, which you can tweak as needed for your project, and direct any WSGI-compliant application server to use.

<br></br>

## <h3 id="admin">admin.py</h3>
- This file manage the Django admin panel which is the include of all UI datas, database and methods
- This file, which is the main and the most important in the project, contains the user models and the methods that are set according to the dynamics of the project.


<br></br>

## <h3 id="apps">apps.py</h3>
- In this file; If any apps is exists, we have to say the name to Django which app we want to add.
<br></br>

## <h3 id="models">models.py</h3>
- In this file; If we want to make changes in an application we have written additionally, we set the necessary database registration operations, field types and display properties of these fields.

<br></br>

## <h3 id="tests">tests.py</h3>
- If we want to test the features and functions in our project, we can write the codes that test all functions in this file. However I don't need to do any auto-tests in this project. 

<br></br>

## <h3 id="views">views.py</h3>
- When we want to change any action fields, form fields or any spesific fields, we can use this file. But ı didn't write any form or etc. in this project

<hr></hr>

## <h2 id="runserver">Run Server And Connect To The User Interface On The Local Host</h3>
- And finally let's reach the User Interface on the local host
- Firstly we must write a short and very simple code on the CMD or Terminal. 
- Here is the code:

`python manage.py runserver`

- This code will be run our project on the [local host](http://127.0.0.1:8000/) and then we will see the Interface.  

<hr></hr>
<h1 style="color:lightblue">In A Nutshell</h1>

- In summary, in this project I designed a basic and simple User Interface (UI) design for that given to me assignment by P.I Works Inc.

- For more project repos, you could visit my [GIThub profile](https://github.com/yusufhandogan)

- Thank's for your times given to me.
