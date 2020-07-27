---
title: "Django Tutorial 1"
date: "2020-07-13T22:40:32.169Z"
template: "post"
draft: false
slug: "django-tutorial-polls"
category: "Web Development"
tags:
  - "Python"
  - "Django"
  - "Backend"
  - "Web Development"
description: "Quick Refresher on Django Tutorial"
socialImage: "/media/42-line-bible.jpg"
---

- [Basic setup for the project](#basic-setup-for-the-project)
- [The digital age](#the-digital-age)
- [Loss of humanity through transitions](#loss-of-humanity-through-transitions)
- [Chasing perfection](#chasing-perfection)

![42-line-bible.jpg](/media/42-line-bible.jpg)

To start using Python and Django Web Framework for my summer internship as a Back-end engineer, I am starting to learn Django with the official documentation.

This is the tutorial to make a simple project, which is called "mysite," contaning an application named polls and admin.

- The polls app lets user view polls and make votes
- The admin site enables user to modify and view the polls database.

## Basic setup for the project

Assuming that Django is already installed in the current virtual directory, create the project with django.

```django-admin startproject mysite```

Then, we can see a project directory, "mysite," containing manage.py and its subdirectory "mysite."

- manage.py is a python file that enables a programmer to interact with this Django project (associated with variouscommands - I'd recommend not to edit this!)

![Tutorial1-1.jpg](/media/Tutorial1-1.jpg)

Not to get confused, since the mother directory and its subdirectory have the idential name, "mysite," change the mother directory's name to mysite_project. (You cannot change the subdirectory's name, as it is used by Django as things go on)

```mv mysite mysite_project```

![Tutorial1-1.jpg](/media/Tutorial1-1.jpg)

Let's move into mysite_project directory now. Since we need an application that enables users to view and make polls, create polls application. 

- Each Django project can contain multiple applications and apps can be reused in other Django projects.

- To make an application for this Django project, we need to be located in the directory where manage.py is at.

```python manage.py startapp polls```

![Tutorial1-1.jpg](/media/Tutorial1-1.jpg)

However, even if we just created the polls application, our Django project, mysite, cannot recognize it automatically. 

So, we need to register the polls application in the project settings, which is settings.py, located in the mysite directory.

```vi settings.py```

![Tutorial1-1.jpg](/media/Tutorial1-1.jpg)

As we can see, there is a section called INSTALLED_APPS in settings.py, having all applications installed in the current Django project.

So, to register the polls application, we can simply write the name of our newly created application, polls, in INSTALLED_APPS.

![Tutorial1-1.jpg](/media/Tutorial1-1.jpg)

Now we have installed our first application in this Django project!


## Construct a database

Before we make actual functions that make us view and make polls, we are going to build a database for this polls application. This is called models.py located in the polls directory.

- To make a database, we need to decide which database engine will be used in this Django project. In this project, we will use the default database sqlite3 same as the tutorial.

Let's edit the polls/models.py to build the database.

<pre>
<code>
#As Django provides a default models module, we are 
from django.db import models 

</code>
</pre>

As 



Now, let's make some functions for the newly created polls application.

After moving into the polls directory, edit views.py, which will contain actual functions like voting for the application.

Finally, what we need to touch base on for the basic setting is URL. Django finds applications and their views with URLS, 


```vi views.py```

<pre>
<code>
from django.http import HttpResponse

def index(request):
	return HttpResponse("This is a polls application")
</code>
</pre>