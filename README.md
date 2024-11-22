## Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![image](https://github.com/user-attachments/assets/f2aca451-c50d-403a-9ec6-fca5f947e244)

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
admin.py
```
from django.contrib import admin
from .models import loan_data,loan

admin.site.register(loan_data,loan)
```


models.py
```
from django.db import models
from django.contrib import admin
class loan_data(models.Model):
    serial_no = models.IntegerField()
    customer = models.CharField(max_length=100)
    bank_name = models.CharField(max_length=100)
    date_of_loan = models.DateField()
    loan_approved = models.CharField(max_length=10)

class loan(admin.ModelAdmin):
    list_display=['serial_no','customer','bank_name','date_of_loan','loan_approved']

```

## OUTPUT

![image](https://github.com/user-attachments/assets/edba4046-68ce-42f3-b35b-84e11a240d8f)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
