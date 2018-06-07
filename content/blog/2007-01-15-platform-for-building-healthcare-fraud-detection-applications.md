---
title: Platform for building healthcare fraud detection applications
author: Shahid N. Shah
type: post
date: 2007-01-15T15:05:20+00:00
url: /2007/01/15/platform-for-building-healthcare-fraud-detection-applications/
oc_commit_id:
  - https://www.healthcareguy.com/2007/01/15/platform-for-building-healthcare-fraud-detection-applications/1478769097
views:
  - 2245
dsq_thread_id:
  - 5168364735
categories:
  - Opinion

---
I ran across [Picalo][1], an open source fraud detection platform,&nbsp;and thought it might be a great solution for those of us looking to build our own fraud detection systems in healthcare settings. Here&#8217;s how the authors describe it:

> Picalo is a data analysis application, with focus in fraud detection and data retrieved from corporate databases. It is also the foundation for an automated fraud detection system. 
> 
> Picalo is currently focused on data analysis for fraud and corruption detection. However, it is an open framework that could actually be used for many different types of data analysis: network logs, scientific data, any type of database-oriented data, and data mining.

One of the nicest features of Picalo seem to be [detectlets][2]. These are little bits of analysis code written by analysts and non-programmers to help define what to look for when attempting to detect fraud. By creating libraries of detectlets we could build and share fraud detection rules between IDNs, hospitals, government institutions, etc. Seems very powerful.

The only issue I see with Picalo is that it&#8217;s GPL which means that it&#8217;s not a very friendly open source license for commercial vendors to build their software upon. GPL is great for end users, though&nbsp;(especially if you plan to build your system in an IT shop).

 [1]: http://picalo.org/
 [2]: http://picalo.org/detectlets.spy