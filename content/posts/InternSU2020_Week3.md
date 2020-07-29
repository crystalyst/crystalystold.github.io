---
title: "Koodon - Project Plan for Backend"
date: "2020-07-28T22:40:32.169Z"
template: "post"
draft: false
slug: "summer-internship-2020-2-3"
category: "Internship"
tags:
  - "Python"
  - "Django"
  - "Backend"
  - "Web Development"
  - "Internship"
description: "A weekly log for my Software Engineering summer internship at Koodon - Week 2"
socialImage: "/media/42-line-bible.jpg"
---

![42-line-bible.jpg](/media/42-line-bible.jpg)

- [What did I and our team do for the week 2](#what-did-i-and-our-team-do-for-the-week-2)
- [Database Modeling - The beauty of constructing a database](#database-modeling-the-beauty-of-constructing-a-database)
- [Why did we decide to completely recreate the web application](#why-did-we-decide-to-completely-recreate-the-web-application)
- [spa-or-mpa-csr-or-ssr](#spa-or-mpa-csr-or-ssr)


## What did I and our team do for the week 2?

This week, throughout many team meetings, my fellow interns, the head UX/UI designer, and I mostly focused on three main missions: 

- First, to establish a Database modeling for our service (a web application), by utilzing [Aquerytool](https://aquerytool.com/). 
- Second, to decide whether or not we will completely rebuild the service and leave the current e-commerce solution that the company has been using.
- Third, to decide whether or not we will create our web application either in SPA (Single Page Application) or MPA (Multiple Page Application), and also either in CSR (Client Side Rendering) or SSR (Server Side Rendering).

## Database Modeling - The beauty of constructing a database

As a back-end developer, I think that modeling a database is one of the trickiest parts since there are so many factors to consider. 

Along with my fellow back-end intern, we established more than 30 tables for the database for our project, which contains tables like Accounts, Products, Consignments, Status_codes, and so on. All of these tables are associated with one-to-one, one-to-many, and many-to-many relationships with other tables.

At first, we finished establishing our first-version of tables in two days, and started to make database tables in models.py for our apps in our Django project. However, as we continuously talked with other members, especially about the product design, we realized that there are many exceptional cases we need to take into account in terms of storing our data. In this sense, we added more tables and columns in some existing tables to refelct the changes needed.

## Why did we decide to completely recreate the web application

Initially, the CEO and the head UX/UI designer suggested that they are thinking about replacing only the part of their services to their own, which means that the web application that the company is going to use will have two components - <u>**1. the service that is like an e-commerce under the current e-commerce solution**</u> and <u>**2. the service that will be created by us, which is a sales agency for second-hand luxury goodss.**</u>

After contemplating on this issue as a team, we ended up with rebuilding the entire service instead of utilizing two seperated components. This is because we thought that this requires a user to sign in twice, to use both purchaing and selling features, which would likely provide a bad user experience.

## SPA or MPA / CSR or SSR

Our front-end interns and UX/UI designer were contemplating about which page application, either SPA or MPA, we need to use to build our web application. In short, we decided to use SPA for our project, since the tech stacks our front-end interns have are mostly related to React.js, even if it has some decifits particulary in terms of SEO (Search Engine Optimization). To deal with this deficit on SEO, we will be going to use Next.js.

Since I was not familiar about this, as my tech stacks are mostly back-end, I will conduct some research on SPA/MPA/SSA/CSA in the following week to engage in the conversations with the front-end developers and the designer.

