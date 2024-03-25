# Ex02 Django ORM Web Application
## Date:22/03/2024

## AIM
To develop a Django application to store and retrieve data from a Train database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Screenshot 2024-03-25 213826](https://github.com/pavithran2046/ORM/assets/139334834/d078c130-69d5-4ab1-8693-ff4638b016bd)

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
admin.py
from django.contrib import admin

from .models import Train, TrainAdmin

admin.site.register(Train, TrainAdmin)

models.py
from django.db import models
from django.contrib import admin
class Train(models.Model):
    Train_code=models.CharField(max_length=20,primary_key=True)
    Train_name=models.CharField(max_length=100)
    start_time=models.TimeField()
    End_time=models.TimeField()
    start_station_code=models.CharField(max_length=20)
    End_station_code=models.CharField(max_length=20)
 
class TrainAdmin(admin.ModelAdmin):
    list_display=('Train_code','Train_name','start_time','End_time','start_station_code','End_station_code')

```
## OUTPUT
![Screenshot 2024-03-25 213849](https://github.com/pavithran2046/ORM/assets/139334834/3e0d3c24-fea0-4106-a1ee-5d7a13653947)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
