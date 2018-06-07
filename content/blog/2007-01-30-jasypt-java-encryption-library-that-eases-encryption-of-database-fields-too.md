---
title: 'Jasypt: Java encryption library that eases encryption of database fields too'
author: Shahid N. Shah
type: post
date: 2007-01-30T15:46:47+00:00
url: /2007/01/30/jasypt-java-encryption-library-that-eases-encryption-of-database-fields-too/
oc_commit_id:
  - https://www.healthcareguy.com/2007/01/30/jasypt-java-encryption-library-that-eases-encryption-of-database-fields-too/1478769103
views:
  - 2556
ratings_users:
  - 1
ratings_score:
  - 3
ratings_average:
  - 3
dsq_thread_id:
  - 44283696
categories:
  - Opinion

---
If you&#8217;re writing healthcare apps in Java, take a look at [Jasypt][1]. Especially if you need to encrypt data in your databases. Here&#8217;s how the authors describe it:

> Jasypt is a java library which allows the developer to add basic encryption capabilities to his/her projects with minimum effort, and without the need of having deep knowledge on how cryptography works.
> 
> Features:
> 
>   * Provides **easy encryption tools** for little adoption effort.
> 
>   * Also provides **highly configurable standard encryption tools**, for power-users.
> 
>   * All encryption tools comply with **encryption best practices and security recommendations**. They are also **thread-safe** to avoid concurrency problems even in multi-threaded environments like web applications.
> 
>   * [Jasypt-hibernate][2] provides a transparent mechanism for **persisting data in an encrypted form** using Hibernate.
> 
>   * All encryption tools are designed to be **easily integrable into IoC containers** like the [Spring Framework][3], although, of course, it can be used without one.

I haven&#8217;t had a chance to play with it yet, but I really like the hibernate library that allows transparent persistence of database fields. Most developers find that work depressingly difficult so security usually suffers but if Jasypt does its job perhaps we&#8217;ll get some more security without extra work.

 [1]: http://www.jasypt.org/
 [2]: http://www.jasypt.org/hibernate3.html
 [3]: http://www.jasypt.org/spring.html