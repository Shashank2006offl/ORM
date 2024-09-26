# Ex02 Django ORM Web Application
## Date: 25/09/2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![WhatsApp Image 2024-03-22 at 10 38 51_9b34163d](https://github.com/Rohanjeyachandiran/ORM/assets/161102491/aa07dfcb-5b74-48b8-9795-316c7ef56006)



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
