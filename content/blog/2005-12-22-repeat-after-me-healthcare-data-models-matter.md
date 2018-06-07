---
title: 'Repeat after me: healthcare data models matter'
author: Shahid N. Shah
type: post
date: 2005-12-22T14:31:54+00:00
url: /2005/12/22/repeat-after-me-healthcare-data-models-matter/
oc_commit_id:
  - https://www.healthcareguy.com/2005/12/22/repeat-after-me-healthcare-data-models-matter/1478768967
views:
  - 2216
dsq_thread_id:
  - 5241263958
categories:
  - Opinion

---
As we all know, healthcare applications come and go but data lives on forever. We’ve seen that since the beginning of the computer industry; when we move from legacy systems into more “modern” architectures, we often leave behind applications but we almost always take along the data into the future. Even though data is so important, we in health IT don’t seem to spend the quality time necessary to structure our schemas and databases in such a way as to make it easier to maintain in the future. We often don’t design our data models solidly and we don’t test it well. Although things should have improved when we got to object oriented programming (OOP), object-oriented technology has actually caused data management principles to be unintentionally compromised.

Large-scale object-oriented applications development, which is fairly new to healthcare, has not improved our ability to manage data using sound data management principles. This is because in the world of objects, data is simply considered part of the state of an object. For example, a person object’s demographics are considered the state of the person object. An encounter’s data is considered state of a transaction object. Most modern object-relational mapping (ORM) tools try to hide SQL and the underlying relationships of the database. This is great if the data model is designed from the ground up by a relational modeler and then the ORM is applied on top of it. More often than not, though, the ORM is used to generate the schema – which means that an application programmer is determining the data model, not a data modeler. What’s wrong with that? Simple: if the application were the most important thing, that’s fine but if we want the data to live forever we need to define the data, its usage, how it’s structured, etc before we design the application and not the other way around.

Our friends in the health IT applications development community need to be taught that data modeling is not just a technical exercise. You can’t define a data model with a bunch of engineers and other “geeks” sitting around a table. Data modeling is about understanding all the uses of the data, the relationships and attributes involved in the data, and most importantly how the data management approach will grow and change in the future. It’s the last part (extensibility of the database) that is often forgotten in most systems. All this involves direct communication with end users, stakeholders, and other non-technical personnel. This seems pretty obvious but in my 15 years of experience I’ve learned that databases are treated as a file cabinet – just let your application toss whatever is necessary in there and then we’ll deal with organizing it later. When you do that, it’s a recipe for disaster.

When you’re building your own systems, you should attempt to use tried and true data models from existing sources. If you don’t have hotshot data modelers, look at Len Silverson’s two-volume work [The Data Model Resource Book: A Library of Universal Data Models for All Enterprises][1]. Buy the two books, try to comprehend what an extensible data model looks and works like, and then hold your developers and database administrators accountable for it. If you’re building a healthcare meta model, there are even books available that cover universal meta models. Unlike a few years ago, there are books which provide de facto, well designed, data models so you’re not on your own. If a developer comes to you with a data model but can’t provide references and patterns for how he arrived at his model, tell him to use one of the ones described in a book. There’s no time to keep reinventing the wheel.

When you’re buying new systems, spend more time evaluating the database design than the application’s user interface (UI). The UI can easily be changed in the future but the data model is not a trivial change (and when the vendor changes the data model you’ll be in a world of hurt). If a vendor does not let you analyze or study their data model, don’t buy from them. That’s like a car deal selling you a car without you being able to check the engine. When you’re evaluating a data management system (and in health IT almost all systems are data management systems) then focus on the data, not the applications. You could even use the Silverston type books referenced above to make your vendor compare their data models against other well known designs.

With all the talk around “patient-centric” architecture you’d think that the vendors have a data model to support it. Of course, we all know that they don’t and we need to hold them accountable for it. And, with all the new integration needs being identified by RHIOs, NHIN, PHRs, and EHRs, data models are even more crucial. Applications will continue to be chopped up in a service oriented architecture, making the central database even more powerful.

The lesson here is simple: because applications come and go but data lives on forever, don’t ignore the data model.

_Note: This was a guest article I wrote for [Tim&#8217;s HISTalk][2] and [IBM&#8217;s HealthNex][3] blogs but due to popular demand I&#8217;ve posted it here as well so it shows up in searches on this site. Thanks to all those who suggested it._

 [1]: http://www.amazon.com/exec/obidos/redirect?tag=thehealthcitg-20%26link_code=xm2%26camp=2025%26creative=165953%26path=http://www.amazon.com/gp/redirect.html%253fASIN=0471380237%2526tag=thehealthcitg-20%2526lcode=xm2%2526cID=2025%2526ccmID=165953%2526location=/o/ASIN/0471380237%25253FSubscriptionId=1EECBSVEHWEDC3PMEA82 "View product details at Amazon"
 [2]: http://histalk.blog-city.com/guest_article__repeat_after_me_healthcare_data_models_matter.htm
 [3]: http://healthnex.typepad.com/web_log/2005/12/repeat_after_me.html