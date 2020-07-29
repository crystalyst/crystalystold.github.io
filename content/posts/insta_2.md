---
title: "Modifying the main setting file to start a Django project"
date: "2020-06-09T22:40:32.169Z"
template: "post"
draft: false
slug: "django-endpoint-practice-2"
category: "Web Development"
tags:
  - "Python"
  - "Django"
  - "Backend"
  - "Web Development"
description: "How to modify settings.py in a Django project directory."
socialImage: "/media/42-line-bible.jpg"
---

- [Create a Django project](#create-a-django-project)
- [Modifying practice_project/settings.py](#modifying-practice-project-settings.py)

![42-line-bible.jpg](/media/42-line-bible.jpg)

In the last post, we went over how to create a virtual environment with Django, and why we need to use it.

In this post, using the virtual environment we created, we will create a Django project that contains Sign-in / Sign-up endpoints. 

## Create a Django project

After moving into the directory we created for a web project, use commands below:

```django-admin startproject practice_project```

Then, by using a finder/file explorer, we can now see there are new files and directories created within the current directory we are located.

- If you have installed **tree command**, then you can use it to see files/directories in a graph form. 

```brew install tree```
```tree practice_project```

## Modifying practice_project/settings.py 

Before starting to actually code, we will modify settings.py, which is an overall setting file for this django project.

- First, since this is for practice, we do not need to specify the host who can access to this project. So, we can change ALLOWED_HOSTS like below:

```ALLOWED_HOSTS = ['*']```

- Second, since we are only going to make endpoints for Sign in and Sign up, which are only back-end side, we will delete Django Admin part. 

Also, we are not going to touch base on authentication and security too much at this moment, so that we need to modify these.

<pre>
<code>
INSTALLED_APPS = [
  'django.contrib.contenttypes',
  'django.contrib.sessions',
  'django.contrib.messages',
  'django.contrib.staticfiles'
  # deleted admin and auth
]

MIDDLEWARE = [
  'django.middleware.security.SecurityMiddleware',
  'django.contrib.sessions.middleware.SessionMiddleware',
  'django.middleware.common.CommonMiddleware',
  'django.contrib.messages.middleware.MessageMiddleware',
  'django.middleware.clickjacking.XFrameOptionsMiddleware',
  # deleted csrfViewMiddleware and AuthenticationMiddleware
]
</code>
</pre>

In the next post, we will be going to create a Django application that does provide sign in/sign up endpoints!