---
layout: post
title: 'Atlassian Products for Django Development: Overview'
date: 2015-12-05 20:36:48.000000000 -07:00
category: blog
author: oleg
tag:
- django
- ci
- atlassian
---
Hello boys and girls!
![Atlassian+Django=Love](/content/images/2015/12/combine_images-1.jpg)
Today I would like to speak about [Atlassian Bamboo](https://www.atlassian.com/software/bamboo/) - the continuous integration product from the company that gave us such great products as JIRA, Confluence, SourceTree and BitBucket Server (previously known as Stash). I myself use SourceTree and BitBucket Server almost every day for my projects and have extensive experience with JIRA and Confluence.
Typically, development teams use Bamboo as well as Jenkins CI server for Java or .NET applications build process, but I will try to configure it to build [Django](https://www.djangoproject.com) applications.

######Before we start

First, a few words about that exactly we want to achieve, about prerequisites and shortcuts.

Actually, we need to implement the workflow in which the *Assigner* (tech lead) creates a new **JIRA** ticket which may be either bug or new feature request and assign it to an *assignee* (developer); in the next place, *assignee* automatically creates a new branch on **BitBucket Server** by moving **JIRA** ticket into *In Progress* status. Next, *assignee* make some changes in Django code and commit them into previously created branch on **BitBucket Server**. Then **Bamboo**, that listens for new commits, checkouts the code and *builds* it - in context of Django that means essentially just to run a shell script ``./manage.py test``, parse the output to understand if we have an error (the next step is to validate the front-end sanity with [Selenium](http://www.seleniumhq.org/) unit tests, but it will be covered in next post) and deploy Django Apps onto QA or Production server. And as a result we have build outcome information available on **Bamboo**, **BitBucket Server** and **JIRA**.

For this exercise we need three environments (for **JIRA**, **BitBucket**, **Bamboo**) and developer workstation with IDE and Git-client installed.
You may ask: Why do we need so many environments? Why not just run all Atlassian software on the same machine?
Well, this is a really bad idea as all these products require really efficient hardware - my suggestion is to allocate at least *2G* of RAM for each installation.

>Please note, that for **Bamboo** installation I will use *Amazon EC2* environment. 

**Ready for Dessert?** Please watch the video bellow if you would like to get a general idea how JIRA, BitBucket Server and Bamboo work together in real life. 
<iframe width="420" height="315" src="https://www.youtube.com/embed/7ftBnNmYHWw" frameborder="0" allowfullscreen></iframe>

