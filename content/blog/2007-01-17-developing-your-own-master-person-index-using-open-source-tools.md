---
title: Developing your own master person index using open source tools
author: Shahid N. Shah
type: post
date: 2007-01-17T05:18:23+00:00
url: /2007/01/17/developing-your-own-master-person-index-using-open-source-tools/
oc_commit_id:
  - https://www.healthcareguy.com/2007/01/17/developing-your-own-master-person-index-using-open-source-tools/1478769091
views:
  - 2790
dsq_thread_id:
  - 5173189354
categories:
  - Opinion

---
There are several types of directories that are useful in healthcare settings; the first is a directory of users and Microsoft Docmain Controller (DC), Active Directory (AD), and LDAP are the most common solutions. DC, AD, etc all help manage a list of users, their roles, and other identity management functions within an enterprise. Another common directory is a master person or master patient index (MPI). MPIs are very useful because it gives a single view of the patient (customer) population within an enterprise.

There are a number of vendors that provide useful MPIs in the commercial world but sometimes, especially in academic or integrated delivery network (IDN) settings it&#8217;s useful to create your own MPI. The best approach is to combine the patient catalogs in various applications and provide a unified front-end. For this purpose, you can use a tool like [Penrose][1].

Penrose is a Java-based open source _virtual directory server_. It basically allows you to connect various data sources (like your clinical apps, your customer-facing apps, support applications, etc) and give a unified view of the patients, users, etc via a virtual LDAP interface. What this allows you to do is to maintain your separate applications where you need to but provide an MPI through a portal for search, lookup, and other purposes. In their words:

> Virtual directory enables federating (aggregating) identity data from multiple heterogeneous sources like directory, databases, flat files, and web services &#8211; real-time &#8211; and makes it available to identity consumers via LDAP.

Penrose has a good architecture, especially for distributed application connectivity within healthcare enterprises, and is worth a look.

 [1]: http://docs.safehaus.org/display/PENROSE/Home