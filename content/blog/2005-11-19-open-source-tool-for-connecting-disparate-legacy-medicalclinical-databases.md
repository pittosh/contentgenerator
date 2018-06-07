---
title: Open source tool for connecting disparate legacy medical/clinical databases
author: Shahid N. Shah
type: post
date: 2005-11-19T16:29:12+00:00
url: /2005/11/19/open-source-tool-for-connecting-disparate-legacy-medicalclinical-databases/
oc_commit_id:
  - https://www.healthcareguy.com/2005/11/19/open-source-tool-for-connecting-disparate-legacy-medicalclinical-databases/1478768927
views:
  - 676
dsq_thread_id:
  - 44283155
categories:
  - Opinion

---
Since most of us in IT spend at least part of our time combining data from multiple databases, it might be worth taking a look at an open source toolkit called [Hydrate][1] that eases the process. From their description:

> Hydrate is a Java tool that provides for fast efficient and error-free transformation of data between three different representations: relational databases, objects in an object-oriented programming language and extended markup language (XML). 

Here are few example situations in which Hydrate is helpful:

  * You want to lay a domain object model view over an existing database or set of databases.
  * Your project involves taking various data files fed from external systems that you want to pull into an object model on your server before writing the results down to a fully relational database.
  * You are building a data warehouse in which you have the broad specifications for the model, but want to provide for flexibility and adaptability for future unpredicted requests.
  * You need to integrate data from many different data sources in a highly performant manner.

Here are reasons _not_ to consider Hydrate:

  * If you are working on a green-field application where you have plain old Java objects (POJOs) that you need to make into persistent objects.
  * If you are looking for a straight in-memory object cache for an underlying database.
  * If you want complete abstraction from your persistence mechanism, and are looking for a tool that completely isolates you from the data storage mechanism.
  * If you have an XML document, particularly if it has an XML schema, and you are trying to map this to and from Java objects, while not caring about any other persistent representation.

 [1]: http://hydrate.sourceforge.net/