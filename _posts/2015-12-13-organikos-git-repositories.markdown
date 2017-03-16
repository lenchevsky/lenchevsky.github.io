---
layout: post
title: 'Organikos Git Repositories'
date: 2015-12-13 16:40:20.000000000 -07:00
category: blog, project
author: oleg
tag:
- django
- ci
---
Just a few words about the project I've started working on:

**Organikos** is an elegant and minimalistic git repository front-end, very simmilar to BitBucket Server or GitLab. But it has that special something - *Core* concept.
*Core* is the instance that stores a number of git repositories, it may reffer to local server, remote server accessible via *ssh*, *BitBucket* or *GitHub* account.

I'm going to follow this schedule as much as it possible:

| Version | Date | Functionality |
|-------|--------|---------|
| v.0.5 | March 1st | Base functionality - repo creation, navigation, file creation and editing, pull requests. |
| v.0.7 | March 14th | SSH Remote Cores support.|
| v.0.9 | March 21st | GitHub Cores support. |
| v.1.0 | March 28th | BitBucket Cores support. |
| v.1.1 | April 18th | Installer, [bug fixes and new features](https://github.com/lenchevsky/organikos/issues).|


### screenshots and videos
Landing Page
![Repo Landing Page](https://raw.githubusercontent.com/lenchevsky/organikos/master/pictures/screens/repo_list.png)


Repo Files List
![Repo Files List](https://raw.githubusercontent.com/lenchevsky/organikos/master/pictures/screens/repo_files.png)


Repo File Source View
![Repo File](https://raw.githubusercontent.com/lenchevsky/organikos/master/pictures/screens/repo_source.png)


### dependencies
* Django 1.8.3
* Python Python 2.7.10

#### python dependencies
* gitpython 1.0.1
* django-bootstrap3 6.2.2
* django-bootstrap-themes 3.1.2
