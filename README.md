# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![Screenshot 2023-01-23 133238](https://user-images.githubusercontent.com/118262199/213993129-3d6f78be-8211-4574-b0d0-3ee26f64259d.png)


## DESIGN STEPS

### STEP 1:
Clone the problem from github
### STEP 2:
create a new app
### STEP 3:
Enter the code for admin.py and model.py
### STEP 4:
execute django admin and create 10 employees

## PROGRAM

model.py

from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')
    
admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
*

## OUTPUT

![Screenshot 2023-01-20 113439](https://user-images.githubusercontent.com/118262199/213993192-535c1259-ce52-4237-a2d0-04b66347b01f.png)


## RESULT
program executed successfully
