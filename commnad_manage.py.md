## Run server is for Development mode 

```bash
  python  manage.py  < optional port default is 8000>
```
## Create project 
### this will creqte directory with project name with files
   - all the project setting<p>   settings.py
   - all the roject Urls <p>   urls.py     
   - For development mode server this configure the entrypoint <p>   wsgi.py 
 ```bash
  python  manage.py  startproject < project Name > .
```
## Create app
     - avoid giving name that may conflict saved word like , test, prod , app etc ''
### this will creqte directory with app name name with files
   - all the pages of the application <p>   view.py
   -  test for test defnition actios  <p>   test.py     
   - Data stracture define Data compnenets (tables coulns ets ..) <p>   models.py 
   -  Application configureation and regisreation  <p>   app.py   
   - admin , by default create module for administration of the application ,p. admin.py
     
 ```bash
  python  manage.py  startapp <Name of app>
```
## register the app
```yaml
INSTALLED_APPS = [
    'courses.apps.CoursesConfig',   <--- This is the app registration 
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
```
## this refering to existsng app in :
![image](https://user-images.githubusercontent.com/50881797/172160701-ac8e97d0-8012-48f0-bcb5-da8e72bbfe60.png)


 ```bash
  python  manage.py  
```
##
 ```bash
  python  manage.py  
```
##
 ```bash
  python  manage.py  
```
##
 ```bash
  python  manage.py  
```
##
 ```bash
  python  manage.py  
```
