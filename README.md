# Django

Prepare Your Environment
When you’re ready to start your new Django web application, create a new folder and navigate into it. In this folder, you’ll set up a new virtual environment using your command line:
```shell
$ python3 -m venv env
```
This command sets up a new virtual environment named env in your current working directory. Once the process is complete, you also need to activate the virtual environment:
```shell
$ source env/bin/activate
```
If the activation was successful, then you’ll see the name of your virtual environment, (env), at the beginning of your command prompt. This means that your environment setup is complete.

You can learn more about how to work with virtual environments in Python, and how to perfect your Python development setup, but for your Django setup, you have all you need. You can continue with installing the django package.

 Remove ads
Install Django and Pin Your Dependencies
Once you’ve created and activated your Python virtual environment, you can install Django into this dedicated development workspace:

(env) $ python -m pip install django
This command fetches the django package from the Python Package Index (PyPI) using pip. After the installation has completed, you can pin your dependencies to make sure that you’re keeping track of which Django version you installed:

(env) $ python -m pip freeze > requirements.txt
This command writes the names and versions of all external Python packages that are currently in your virtual environment to a file called requirements.txt. This file will include the django package and all of its dependencies.

Note: There are many different versions of Django. While it’s usually best to work with the most recent version when starting a new project, you might have to work with a specific version for one particular project. You can install any version of Django by adding the version number to the installation command:

(env) $ python -m pip install django==2.2.11
This command installs the version 2.2.11 of Django to your environment instead of fetching the most recent version. Replace the number after the double equals sign (==) with the specific Django version you need to install.

You should always include a record of the versions of all packages you used in your project code, such as in a requirements.txt file. The requirements.txt file allows you and other programmers to reproduce the exact conditions of your project build.


Suppose you’re working on an existing project with its dependencies already pinned in a requirements.txt file. In that case, you can install the right Django version as well as all the other necessary packages in a single command:

(env) $ python -m pip install -r requirements.txt
The command reads all names and versions of the pinned packages from your requirements.txt file and installs the specified version of each package in your virtual environment.

Keeping a separate virtual environment for every project allows you to work with different versions of Django for different web application projects. Pinning the dependencies with pip freeze enables you to reproduce the environment that you need for the project to work as expected.

Set Up a Django Project
After you’ve successfully installed Django, you’re ready to create the scaffolding for your new web application. The Django framework distinguishes between projects and apps:

A Django project is a high-level unit of organization that contains logic that governs your whole web application. Each project can contain multiple apps.
A Django app is a lower-level unit of your web application. You can have zero to many apps in a project, and you’ll usually have at least one app. You’ll learn more about apps in the next section.
With your virtual environment set up and activated and Django installed, you can now create a project:

(env) $ django-admin startproject <project-name>
This tutorial uses setup as an example for the project name:

(env) $ django-admin startproject setup
Running this command creates a default folder structure, which includes some Python files and your management app that has the same name as your project:

setup/
│
├── setup/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
└── manage.py
In the code block above, you can see the folder structure that the startproject command created for you:

setup/ is your top-level project folder.
setup/setup/ is your lower-level folder that represents your management app.
manage.py is a Python file that serves as the command center of your project. It does the same as the django-admin command-line utility.
The nested setup/setup/ folder contains a couple more files that you’ll edit when you work on your web application.

Note: If you want to avoid creating the additional top-level project folder, you can add a dot (.) at the end of the django-admin startproject command:

(env) $ django-admin startproject <projectname> .
The dot skips the top-level project folder and creates your management app and the manage.py file right inside your current working directory. You might encounter this syntax in some online Django tutorials. All it does is create the project scaffolding without an extra top-level project folder.

Take a moment to explore the default project scaffolding that the django-admin command-line utility created for you. Every project that you’ll make using the startproject command will have the same structure.

When you’re ready, you can move on to create a Django app as a lower-level unit of your new web application.

 Remove ads
Start a Django App
Every project you build with Django can contain multiple Django apps. When you ran the startproject command in the previous section, you created a management app that you’ll need for every default project that you’ll build. Now, you’ll create a Django app that’ll contain the specific functionality of your web application.

You don’t need to use the django-admin command-line utility anymore, and you can execute the startapp command through the manage.py file instead:

(env) $ python manage.py startapp <appname>
The startapp command generates a default folder structure for a Django app. This tutorial uses example as the name for the app:

(env) $ python manage.py startapp example
Remember to replace example with your app name when you create the Django app for your personal web application.

Note: If you created your project without the dot shortcut mentioned further up, you’ll need to change your working directory into your top-level project folder before running the command shown above.

Once the startapp command has finished execution, you’ll see that Django has added another folder to your folder structure:

setup/
│
├── example/
│   │
│   ├── migrations/
│   │   └── __init__.py
│   │
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
│
├── setup/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
└── manage.py
```
