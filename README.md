# Ex02 Django ORM Web Application
## Date: 26-09-2024

## AIM
To develop a Django application to store and retrieve data from a Bank database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![image](https://github.com/user-attachments/assets/d870b904-5c5f-4331-806d-41398ce9a291)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 customers.

## PROGRAM

admin.py
```
from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)

```
models.py
```
from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.IntegerField(primary_key=True)
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()
 
class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')


```

## OUTPUT

![Screenshot 2024-09-26 221607](https://github.com/user-attachments/assets/fd0ed96b-635c-4cde-aa7b-d103de90b8d7)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
