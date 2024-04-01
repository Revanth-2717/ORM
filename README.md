# Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
models.py :
```PYTHON
from django.db import models
from django.contrib import admin
class Library(models.Model):
    bookauthor=models.CharField(max_length=20)
    bookname=models.CharField(max_length=25)
    bookid=models.IntegerField(primary_key=True)
    published_date=models.DateField()
    bookcost=models.IntegerField()

class LibraryAdmin(admin.ModelAdmin):
    list_display=("bookauthor","bookname","bookid","published_date","bookcost")
```

admin.py
```python
from django.contrib import admin
from.models import Library,LibraryAdmin
admin.site.register(Library,LibraryAdmin)
```
## OUTPUT

![Screenshot 2024-04-01 213530](https://github.com/Revanth-2717/ORM/assets/152462274/ba08d237-0ec9-4d3e-9105-f2df389b58ef)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
