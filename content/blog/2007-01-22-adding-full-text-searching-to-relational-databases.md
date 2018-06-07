---
title: Adding full-text searching to Relational Databases
author: Shahid N. Shah
type: post
date: 2007-01-22T16:20:16+00:00
url: /2007/01/22/adding-full-text-searching-to-relational-databases/
oc_commit_id:
  - https://www.healthcareguy.com/2007/01/22/adding-full-text-searching-to-relational-databases/1478769101
views:
  - 11011
ratings_users:
  - 4
ratings_score:
  - 19
ratings_average:
  - 4.75
dsq_thread_id:
  - 5175481281
categories:
  - Opinion

---
Relational databases like ORACLE, SQL*Server, and MySQL are great at storing structured data in rows and columns and managing relationships across tables. Relational database are also more write-friendly than read-friendly (like searching). What that means is that vendors and developers often structure the tables and columns more to make it easy for them to write data into than for users to read data out of (because users are always more creative than we think they are).

One way to get around structural limitations is to put full-text searching on top of structured data . One such tool,&nbsp;[DBSight][1], is an inexpensive but useful application that allows you to point to any relational database and then do Google- or Amazon-like searches. While I recommend full-text searching because it is a great addition to most relational databases, you need to make sure you design the privacy and security rules appropriately otherwise users might get access to stuff they shouldn&#8217;t.

If you haven&#8217;t done so already, start asking your vendors to give you full-text searching capabilities in your applications so that they can manage the privacy and security rules.

 [1]: http://www.dbsight.net/