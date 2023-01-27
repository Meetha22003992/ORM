# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![image](https://user-images.githubusercontent.com/119401038/215165262-f1fd45bd-d308-4f8d-98f1-b7bb7e4e2581.png)


Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Clone the problen from github

### STEP 2:
create new app

### STEP 3:
Enter the code of admin.py and model.py

### Step 4:
Execute django admin and create 10 employee

## PROGRAM
Model.py
from django.db import models
from django.contrib import admin
# Create your models here.
class Employee(models.Model):
    Emp_id=models.CharField(primary_key=True,max_length=150,help_text='Emplopee_id')
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()
class EmployeeAdmin(admin.ModelAdmin):
    list_display=('Emp_id','name','salary','age','email')

Admin.py
from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)

## OUTPUT
![image](https://user-images.githubusercontent.com/119401038/215164940-8ad49c18-d7a3-470e-ae72-a85874db20ad.png)


## RESULT
Program executed sucessfully
