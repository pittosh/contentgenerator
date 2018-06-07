---
title: Could everybody’s ADT system use the same database schema?
author: Shahid N. Shah
type: post
date: 2005-12-03T17:30:39+00:00
url: /2005/12/03/could-everybodys-adt-system-use-the-same-database-schema/
oc_commit_id:
  - https://www.healthcareguy.com/2005/12/03/could-everybodys-adt-system-use-the-same-database-schema/1478768947
views:
  - 655
dsq_thread_id:
  - 44283221
categories:
  - Opinion

---
Tim at HISTalk poses a poingnant question: _[Could Everybody&#8217;s ADT System Use the Same Database Schema?][1]_ Some excerpts:

> What I was really thinking about is the idea that the database design tells you how the application works. If that&#8217;s true, then what technical functions of the vendor add the most value? Is it database design, GUI design, algorithms, content, or something else? If our vendor&#8217;s competitor got a copy of the schema I was looking at, would it really reveal any proprietary secrets or otherwise turn on their lightbulbs with great ideas to change their own app? Or, would they be as lost as the clients who called me for elaboration? Maybe they wouldn&#8217;t even be interested. 

Tim elaborates:

> Why can&#8217;t every vendor voluntarily or mandatorily use the same database layout for core information? How many ways can you express and repose standard elements such as date of birth, gender, address, etc.? Vendors can, when under duress, feed their data to a standard interface. Why can&#8217;t all systems just use an approved core set of tables, updated by the same core set of business rules, and then add their value through additional related tables, GUIs, business rules, etc.? Everyone&#8217;s patient database could look and work the same. Seen one, seen &#8217;em all. 

Tim&#8217;s concept of &#8220;one schema to rule them all&#8221; is actually going to be close to reality eventually, but only if we can agree on common business rules as well as data. The idea of &#8220;universal data models&#8221; that guys like [Silverston][2] and I promote is exactly to Tim&#8217;s point: don&#8217;t reinvent the schema wheel.

The reason why we won&#8217;t see a universal schema in healthcare anytime soon is that the it&#8217;s very difficult to create one that is extensible enough. I&#8217;ve been building extensible schemas for years, but they require a great deal of effort, time, and expertise. All of that adds up to _expensive_. Doing the right thing is always a bit more costly. The schemas that are thrown together by many health IT vendors these days would be laughed at by non-healthcare folks. Outside the health IT community, where I still spend a good deal of technical time, data models have been steadily improving and becoming standardized. See the cases of SAP, PeopleSoft, ORACLE apps, etc. Those are large-scale ERP solutions designed to have applications attached to them so their data models are designed to handle it. They&#8217;re certainly not perfect, but certainly more extensible because these applications have to play well with others and are designed to do so.

I hope Tim&#8217;s post, [along with mine][3], starts a real debate among buyers of healthcare about how transparent they want their vendors to be about the database schemas in their products. In our new service-oriented world we need to make sure that vendors are providing software that can plug and play and that starts with extensible schemas that can manage data properly.

It&#8217;s a joke to think we&#8217;ll have an NHIN, RHIOs, CPOE, EHRs, PHRs, EMRs, etc without a basic understanding of data and relationships.

 [1]: http://histalk.blog-city.com/could_everybodys_adt_system_use_the_same_database_schema.htm
 [2]: http://www.amazon.com/exec/obidos/redirect?tag=thehealthcitg-20%26link_code=xm2%26camp=2025%26creative=165953%26path=http://www.amazon.com/gp/redirect.html%253fASIN=0471380237%2526tag=thehealthcitg-20%2526lcode=xm2%2526cID=2025%2526ccmID=165953%2526location=/o/ASIN/0471380237%25253FSubscriptionId=1EECBSVEHWEDC3PMEA82 "View product details at Amazon"
 [3]: http://histalk.blog-city.com/guest_article__repeat_after_me_healthcare_data_models_matter.htm