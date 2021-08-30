#  Django Forms
---
#### Django provides a Form class which is used to create HTML forms. It describes a form and how it works and appears.
#### It is similar to the ModelForm class that creates a form by using the Model, but it does not require the Model.

#### Each field of the form class map to the HTML form input element and each one is a class itself, it manages form data and performs validation while submitting the form.

```
from django import forms  
 class StudentForm(forms.Form):  
    firstname = forms.CharField(label="Enter first name",max_length=50)  
    lastname  = forms.CharField(label="Enter last name", max_length = 100)  
```        
#### A StudentForm is created that contains two fields of CharField type. Charfield is a class and used to create an HTML text input component in the form.

#### The label is used to set HTML label of the component and max_length sets length of an input value.

#### When rendered, it produces the following HTML to the browser.
```
    <label for="id_firstname">Enter first name:</label>  
     <input type="text" name="firstname" required maxlength="50" id="id_firstname" />  
    <label for="id_lastname">Enter last name:</label> <input type="text" name="lastname" required maxlength="100" id="id_lastname" />  
```

## Instantiating Form in Django

```
 #views.py
    from django.shortcuts import render  
    from myapp.form import StudentForm  
      
    def index(request):  
        student = StudentForm()  
        return render(request,"index.html",{'form':student})  
```

## and add the index.html

```
  #index.html
    <!DOCTYPE html>  
    <html lang="en">  
    <head>  
        <meta charset="UTF-8">  
        <title>Index</title>  
    </head>  
    <body>  
    <form method="POST" class="post-form">  
             
            {{ form.as_p }}  
            <button type="submit" class="save btn btn-default">Save</button>  
    </form>  
    </body>  
    </html>  
```

## Provide the URL in urls

```
    from django.contrib import admin  
    from django.urls import path  
    from myapp import views  
    urlpatterns = [  
        path('admin/', admin.site.urls),  
        path('index/', views.index),  
    ]  
```

![](https://www.javatpoint.com/django/images/django-forms-localhost-index-output.png)      

---
## Django CRUD 
---

#### Django is a Python-based web framework which allows you to quickly create web application without all of the installation or dependency problems that you normally will find with other frameworks. Django is based on MVT (Model View Template) architecture and revolves around CRUD (Create, Retrieve, Update, Delete) operations. CRUD can be best explained as an approach to building a Django web application. In general CRUD means performing Create, Retrieve, Update and Delete operations on a table in a database. Let’s discuss what actually CRUD means

![](https://media.geeksforgeeks.org/wp-content/uploads/20200114185631/Untitled-Diagram-316-1024x630.jpg)

- Create – create or add new entries in a table in the database. 
- Retrieve – read, retrieve, search, or view existing entries as a list(List View) or retrieve a particular entry in detail (Detail View) 
- Update – update or edit existing entries in a table in the database 
- Delete – delete, deactivate, or remove existing entries in a table in the database


        
        
### references :
---
[javatpoint](https://www.javatpoint.com)
[geeksforgeeks](https://www.geeksforgeeks.org)
