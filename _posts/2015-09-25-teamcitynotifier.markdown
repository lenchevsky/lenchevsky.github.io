---
layout: post
title: TeamCityNotifier
date: 2015-09-25 18:39:32.000000000 -06:00
---
TeamCityNotifier is a [python script](https://github.com/lenchevsky/TeamCityNotifier) which sends a push notification to your smartphone as your TC build is Green/Red of TC Server is down. 

###How To Use?
  1. Pull the repository into your computer
  2. Register at https://pushover.net/
  3. Install Pushover Android or iOS app onto your smartphone from https://pushover.net/clients/ios or https://pushover.net/clients/android
  4. Supply them with your Pushover user key
  5. Register a new Application at https://pushover.net/
  6. Edit settings.cfg
    * Supply it with your TeamCity credentials;
    * Supply it woth your Pushover Application token and devices ids
  7. Run or schedule tc_notifier.py script with your OS CRON or Scheduled Tasks service

######Dependencies 

_pip install pushover requests_
