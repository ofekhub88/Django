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
     - avoid giving a name that may conflict the saved words like , test, prod , app etc ''
### this will create  directory with app name name with files
   - all the pages of the application <p>   view.py
   -  test for test defnition actios  <p>   test.py     
   - Data stracture define Data compnenets (tables coulns ets ..) <p>   models.py 
   -  Application configureation and regisreation  <p>   app.py   
   - admin , by default create module for administration of the application ,p. admin.py
     
 ```bash
  python  manage.py  startapp <Name of app>
```
##  create the model object in teh databse
 ```bash
  python  manage.py  migrate
```
## Create teh model object of the apps  
 ```bash
  python  manage.py  makemigrations < app name>
  python  manage.py  migrate 
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
