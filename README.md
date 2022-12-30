# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![diagram](https://user-images.githubusercontent.com/119560117/210086634-457f7a17-c016-4d2b-9b09-8deb3f7794ef.jpeg)

## DESIGN STEPS

### STEP 1:
Create a Django app Go to the app directory In models.py create two classes And save the models.py
### STEP 2:
Go to admins.py And put the two class in admins.py from the models.py And save the file
### STEP 3:
Start the Django server Then move to admin page
## PROGRAM
###Models.py
```
from django.db import models
from django.contrib import admin
class Employee (models.Model):
unique_number=models.CharField(max_length=20,primary_key=True)
name=models.CharField(max_length=100)
age=models.IntegerField()
email=models.EmailField()
job=models.CharField(max_length=100)
class EmployeeAdmin(admin.ModelAdmin):
list_display=('unique_number','name','age','email','job')
```
###Admin.py
```
from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT
![1st output](https://user-images.githubusercontent.com/119560117/210086668-63cf2a19-0429-48ee-b134-8e3340b66f37.png)

###Verifying Primary Key
![2nd output](https://user-images.githubusercontent.com/119560117/210086679-867e460a-4c75-40c6-bea1-616b69a612cf.png)

## RESULT
The output for Django ORM is successful.
