---
title: "Django Tutorial 1"
date: "2020-06-14T22:40:32.169Z"
template: "post"
draft: false
slug: "django-endpoint-practice"
category: "Web Development"
tags:
  - "Python"
  - "Django"
  - "Backend"
  - "Web Development"
description: "How to create a virtual environment for a web programming project."
socialImage: "/media/42-line-bible.jpg"
---

- [Why do wee need a Virtual Environment?](#why-do-we-need-a-virtual-environment)
- [Installing a Virtual Environment](#installing-a-virtual-environment)
- [Use the installed Virtual Environment using miniconda](#use-the-installed-virtual-environment-using-miniconda)

![42-line-bible.jpg](/media/42-line-bible.jpg)

To create Sign in / Sign Up Endpoint with Django for practice, we will be going to utilize a Virtual Environment.

## Why do we need a Virtual Environment?

We use the Virtual Environment when we would like to use linux in an environment that is different from a local one.

If we use the Virtual Environment, we can specifically select and download programs that will be used for a certain project. If we do not use the Virtual Environment, and use the local environment only, we would likely end up with utilizing some programs that are not needed or outdated.

## Installing a Virtual Environment

There are many tools to create a Virtual Environment. In this post, we will use miniconda, which is a simplified version of Anaconda.

1. Install wget by using homebrew in linux

```brew install wget```

2. After getting the hash for installing miniconda from its website, install miniconda by using wget.

```wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh```

3. If you are using zsh, enter the command below:

```./Miniconda3-latest-MacOSX-x86_64.sh```

4. After installing miniconda, move to miniconda3/bin directory by using cd miniconda3/bin, and enter the command below.

```source ~/.zshrc```
 
## Use the installed Virtual Environment using miniconda

1. Create a virtual environment

```conda create -n <env_name> <python=ver or django ~~~>```

2. Check the list of virtual environments

```conda env list```

3. Activate(connect) a virtual environment / Deactivate(disconnect) a virtual environment

```conda activate <env_name> / conda deactivate```

4. Delete a virtual environment

```conda env remove -n <env_name>```

5. Install Django in the created virtual environment (After activating the virtual environment where we want to install Django)

```pip intall django```

- pip is the Package Management System that helps intalling and managing python-based packages.

6. Create a directory to start a web programming project

```mkdir <proj_name>```
```cd <proj_name>```

Now, we are at the virtual environment where Django is installed!