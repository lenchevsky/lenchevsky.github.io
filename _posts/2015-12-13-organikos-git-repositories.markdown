---
layout: default
title: Organikos Git Repositories
date: 2015-12-13 16:40:20.000000000 -07:00
---
Just a few words about the project I've started working on:

**Organikos** is an elegant and minimalistic git repository front-end, very simmilar to BitBucket Server or GitLab. But it has that special something - *Core* concept.
*Core* is the instance that stores a number of git repositories, it may reffer to local server, remote server accessible via *ssh*, *BitBucket* or *GitHub* account.

I'm going to follow this schedule as much as it possible:

<table>
<tr><th>Version</th><th>Date</th><th>Functionality</th></tr>
<tr>
<td> v.0.5 </td><td> March 1st </td><td> Base functionality - repo creation, navigation, file creation and editing, pull requests.</td>
</tr>
<tr>
<td> v.0.7 </td><td> March 14th </td><td> SSH Remote Cores support.</td>
</tr>
<tr>
<td> v.0.9 </td><td> March 21st </td><td> GitHub Cores support.</td>
</tr>
<tr>
<td> v.1.0 </td><td> March 28th </td><td> BitBucket Cores support.</td>
</tr>
<td> v.1.1 </td><td> April 18th </td><td> Installer, <a href="https://github.com/lenchevsky/organikos/issues">bug fixes and new features</a>.</td>
</tr>
</table>

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
