---
title: One table to contain all lookup data is not a good idea
author: Shahid N. Shah
type: post
date: 2005-12-02T14:59:33+00:00
url: /2005/12/02/one-table-to-contain-all-lookup-data-is-not-a-good-idea/
oc_commit_id:
  - https://www.healthcareguy.com/2005/12/02/one-table-to-contain-all-lookup-data-is-not-a-good-idea/1478768945
views:
  - 674
dsq_thread_id:
  - 44283210
categories:
  - Opinion

---
Elyse posted a design pattern (antipattern?) in AntiClue&#8217;s _[One table to contain all lookup data][1]_ article and followed it up a few weeks later with [an example][2].

I wrote an article called _Repeat After Me: Healthcare Data Models Matter_ which was published over at [IBM&#8217;s HealthNex][3] and [Tim&#8217;s HIStalk][4] blogs because I wanted their audiences to hear what I wanted to say on the matter. In that article I said that you can not treat databases as a file cabinet â€“ just letting your application toss whatever is necessary into a bunch of tables and then organizing it later is a recipe for disaster. The database is the heart of every information system, not the application. Design the data model right, make it extensible, protect it, nurture it, caress it, care for it, treat it like it&#8217;s the most important thing you own in your architecture &#8212; _because it is_. One of the reasons why so many health IT systems fail has nothing to do with the quality of applications or their UIs but their misunderstanding of data, data structures, data modeling, and use case analysis leading to poorly designed databases that are not extensible or robust. Now, don&#8217;t mistake me for a DBA &#8212; I&#8217;m not talking about physical models here, just logical ones.

Now back to Elyse&#8217;s post: the reason it&#8217;s probably a bad idea to keep all lookup data in one table because it leads to one solution fits all problems approach. Databases are not bit buckets and a table is not just a row storage concept. If you try to collapse multiple tables into a single one you get application developer productivity but you lose semantic meaning of data. Even if you add a little bit of type definition information you lose the ability to do constraint checking and data validation in the database.

Using a single table to manage lookup data will render all lookup data to be the same &#8212; but not all lookup data in a rich and complex field like healthcare is the same. Also consider this: if you do all your data management (relationships, etc) in the application and decide to use the database just for storage, what happens when you want to add another application to your system that uses the data in the first application&#8217;s database? Want to duplicate all that relationship information in the second app? Third app? Fourth app? Good luck.

Now, I don&#8217;t want to pick on Elyse because the problems being solved in that case might be small, the app could be a prototype, etc. There could be completely valid reasons to pick that pattern, but if I was in charge I would spend a bit more time on the entity relationship model and treat lookups with the same care as everything else. Even if developer productivity is impacted you&#8217;ll still get something that will be around much longer: good data.

 [1]: http://www.anticlue.net/archives/000629.htm
 [2]: http://www.anticlue.net/archives/000634.htm
 [3]: http://healthnex.typepad.com/web_log/2005/12/repeat_after_me.html
 [4]: http://histalk.blog-city.com/guest_article__repeat_after_me_healthcare_data_models_matter.htm