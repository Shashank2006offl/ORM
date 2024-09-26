# Ex02 Django ORM Web Application
## Date: 25/09/2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Blank diagram](https://github.com/user-attachments/assets/635efeae-5287-4a64-9942-186caf68bd8a)



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
```
models.py
from django.db import models
from django.contrib import admin

# Create your models here.
class Book(models.Model):
    book_id = models.IntegerField(primary_key=True)
    book_name = models.CharField(max_length=100)
    Author= models.CharField(max_length=50)
    Date= models.DateField()
    price = models.IntegerField()

class Display_book(admin.ModelAdmin):
    list_display = ('book_id','book_name','Author','Date','price')

admin.py
from django.contrib import admin
from .models import Book,Display_book
# Register your models here.

admin.site.register (Book,Display_book)
```

## OUTPUT
 ![Screenshot 2024-09-24 213955](https://github.com/user-attachments/assets/14938316-1183-4be1-af93-92d23e459f7e)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
