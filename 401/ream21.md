#  Django models 
---
#### Django web applications access and manage data through Python objects referred to as models. Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms
### Versatile
#### Django can be (and has been) used to build almost any type of website — from content management systems and wikis, through to social networks and news sites. It can work with any client-side framework, and can deliver content in almost any format (including HTML, RSS feeds, JSON, XML, etc). The site you are currently reading is built with Django!

### When designing your models it makes sense to have separate models for every "object" (a group of related information). In this case, the obvious objects are books, book instances, and authors.

![coode](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models/local_library_model_uml.svg)

---
####  Fields

#### A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables. Each database record (row) will consist of one of each field value. Let's look at the example seen below:

### Common field arguments

## Example: : 
### code >> 
---

#### from django.db import models

#### class Musician(models.Model):
####    first_name = models.CharField(max_length=50)
####    last_name = models.CharField(max_length=50)
####    instrument = models.CharField(max_length=100)

#### class Album(models.Model):
####     artist = models.ForeignKey(Musician, on_delete=models.CASCADE)
####     name = models.CharField(max_length=100)
####     release_date = models.DateField()
####     num_stars = models.IntegerField()
---
###  Field types¶

### Each field in your model should be an instance of the appropriate Field class. Django uses the field class types to determine a few things:

- The column type, which tells the database what kind of data to store ( INTEGER, VARCHAR, TEXT).
- The default HTML widget to use when rendering a form field ( <input type="text">, <select>).
- The minimal validation requirements, used in Django’s admin and in automatically-generated forms.




