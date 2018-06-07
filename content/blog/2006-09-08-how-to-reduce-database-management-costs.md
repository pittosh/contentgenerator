---
title: How to reduce database management costs
author: Shahid N. Shah
type: post
date: 2006-09-08T12:08:02+00:00
url: /2006/09/08/how-to-reduce-database-management-costs/
oc_commit_id:
  - https://www.healthcareguy.com/2006/09/08/how-to-reduce-database-management-costs/1478769065
views:
  - 2123
ratings_users:
  - 2
ratings_score:
  - 9
ratings_average:
  - 4.5
dsq_thread_id:
  - 5189497618
categories:
  - Opinion

---
Our health IT databases, like in most other industries, are growing fast and sometime out of control. Every time we turn around there&#8217;s another database vendor, small access database, a big Excel file, or embedded database to contend with. Here are some quick but not easy ways to analyze and reduce your database costs:

  * <font color="#656565">Virtualization &#8212; instead of putting everything on physical servers, use tools like VMware and Microsoft Virtual Server to store multiple vendor database servers onto a single physical server. This will save management costs in the primary environment and will simplify disaster recovery.</font>
  * <font color="#656565">Consolidate &#8212; consolidate servers and pay less money for each instance. By moving multiple databases onto the same logical database instance you can reduce licensing costs.</font>
  * <font color="#656565">Standardize &#8212; instead of using different database vendors, try moving to fewer. This one is tough but will have the biggest payout.</font>
  * <font color="#656565">Open Source &#8212; if you&#8217;re able to standardize, try standardizing on open source databases like MySQL, Postgres, and Enterprise DB. <a href="http://www.enterprisedb.com/">Enterprise DB</a> is the most interesting for Oracle folks since that open source database touts its compatibility with Oracle. Don&#8217;t let the commercial vendors scare you away from Open Source databases &#8212; the open source vendors have been supporting some of the world&#8217;s largest databases in heavy production usage for years. They are ready for <em>your</em> workload, too.</font>
  * <font color="#656565">Automate &#8212; decrease the cost of managing lots of databases by automating monitoring and maintenance tasks. I still can believe how many database shops I run into where the DBA&#8217;s still do things manually instead of scripting everything.</font>

In a future posting I&#8217;ll talk about how to get those pesky Microsoft Access and Excel databases under control.