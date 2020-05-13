# CRUD OPERATIONS:

### What is CRUD?
CRUD stands for Create, Read, Update & Delete.These are the four basic operations 
which are executed on Database Models. We are developing a web app which is capable 
of performing these operations.The CRUD operations are defined as follows:

* **Create Operation** :

  The ability of the application to store data in the database.

* **Read Operation** :

  The ability of the application to read data from the database.

* **Update Operation** :

  The ability of the application to edit the stored value in the database.

* **Delete Operation** :

  The ability of the application to delete the value in the database.

Majority of applications on the internet are CRUD applications. For example – Facebook uses CRUD operations to save your data on their database. You can change your profile picture that means perform the update operation. Of course, you can see the data in-app or browser which is read operation. Also, you can delete your Facebook account which is delete operation.

**Let’s explore the steps to design a CRUD application in Django framework:**
#### 1.Creation of new Project and App:
* For Project creation open command prompt and move to the location where you want to save the project.
Then enter the following command

                 django-admin startproject projectname
 <img src = "images/projectcreation.png">

* After the creation of project enter into the directory where manage.py file is present.
* Then for creating the app give the following command in command prompt,
            
                 python manage.py startapp appname
  <img src = "images/appcreation.png">
                 
   Now, all the required setups are complete. We can proceed further.
   
### 2. Installing Application and Setting the Database:
* To install the app, just add the application’s name in the INSTALLED_APPS list. This is inside settings.py file.
* To setup the database ,add the following commands in the database section,
              
          DATABASES = {
         'default': {
         'ENGINE': 'django.db.backends.mysql',
            'NAME': 'djangoconnection',
          'USER': 'root',
          'PASSWORD':'',
          'HOST':'',
          'PORT':'',
           }
            }
              
              
<img src = "images/appinstallation.png">

### 3. Creation of Model :
* Model is the python file,it is used to create the table in table database as the fields in model.py.
* In model.py we have to assign the table field names along with the data models.
* Syntax:
          
              from django.db import models
              class class_name(models.Model):
                  field1 = models.field1_datamodel(length)
                  field2 = models.field2_datamodel(length)
                  field3 = models.field3_datamodel(length)
                  field4 = models.field4_datamodel(length)
              def __str__(self):
                  return self.field_name
       
  <img src = "images/model.png">
  
 ### 3. Creating the Model Form:
 * Form is a python file.
 * It is a class which is used to create an HTML form by using the Model. It is an efficient way to create a form without writing HTML code.
Django automatically does it for us to reduce the application development time. For example, suppose we have a model containing various fields, we don't need to repeat the fields in the form file.
For this reason, Django provides a helper class which allows us to create a Form class from a Django model.
* Syntax :
            
              from django.forms import ModelForm
              from app_name.models import model_class_name
              class class_name(ModelForm):
	                  class Meta:
		                model = model_class_name
		                fields = '__all__'
                    
 <img src = "images/form.png">
 
 ### 4. Registering Model in Django Admin :
* Here we are editing admin.py existing in crud folder. Import the model you want to register in the admin. In this case, it is a Register.
* Syntax :
          
                  admin.site.register(Register)
               
<img src = "images/admin.png">

### 5. Making View Functions for Django CRUD App :
* The view functions are our actual CRUD operations in Django.The entire operation will be defined in this views.py.
* The view.py file consists of many functions depending upon our requirement.For our CRUD Operations we use 4 different functions likely for creation,getting the data,editing the stored data,and for deleting the data in database.
<img src = "images.view.png">

* Till now we are done with the programming part of our CRUD operations.Next steps are to build our html pages for the final outcome in browser.

### 6. Organising the Templates : 
* In this step we will create a folder named templates in the app folder.
* Now in templates folder create another folder with the appname ,in that appname folder we will create all our html files.
* In our CRUD operations we are using register.html,details.html,edit.html and msg.html files.
*So,now we have to create the html files to complete our crud operations.
    ##### 1. Creation of Register.html file:
    * In this register.html we are doing "**create**" CRUD operation.
    * This html page is linked with the data in forms.py.
    <img src = "images/register.png">
    
    ##### 2. Creation of Details.html file :
    * In this Details.html we are doing "**Read/retrive**" CRUD Operation.
    * This html page displays entries in  the table.
    <img src = "images/details.png">
   
   ##### 3. Creation of Edit.html file :
    * In this Edit.html we are doing "**Edit**" CRUD Operation.
    * This html page Edit the required entry in  the table.
    <img src = "images/edit.png">
    
    ##### 4. Creation of Delete.html file:
    * In this Delete.html we are doing "**Delete**" CRUD Operation.
    * This html page deletes the required entry from the table.
    <img src = "images/delete.png">

### 7. Migrating the files with Django and running the server :
* Till now we done all the required files and all ,now we have to migrate these files with the django server.for that we have to enter the followng command in command prompt,

                    python manage.py makemigrations
                    python manage.py migrate
		    python manage.py runserver
		    
		    
### 8. Browsing our Websites using localhost :
* After migrating the files,we have check our final outcome.
* For that open the webbrowser and enter the localhost site and the url name.
* syntax:
			
			http://127.0.0.1:8000/appname/urlname/
			

		  
          
    



                  
                  




                 













