---
title: 'The downside of health IT: seeing fewer patients'
author: Shahid N. Shah
type: post
date: 2006-04-14T14:13:07+00:00
url: /2006/04/14/the-downside-of-health-it-seeing-fewer-patients/
oc_commit_id:
  - https://www.healthcareguy.com/2006/04/14/the-downside-of-health-it-seeing-fewer-patients/1478769031
views:
  - 1472
dsq_thread_id:
  - 44283482
categories:
  - Opinion

---
Military.com posted an interesting article last week on how the Defense Department’s electronic medical record-keeping system,[AHLTA, has reduced patient access to many military outpatient clinics and has lengthened workdays for many doctors][1].

A few notable quotes from the article:

> &#8220;It takes on average two to four times more time to document in AHLTA than it did when we used paper,&#8221; Nelson said. &#8220;For a simple visit like pink eye, patient time can take as little as three to four minutes to diagnose and explain to parents. On a good day [it] takes another three to four minutes to document in the computer.&#8221;
> 
> &#8220;We are so far behind…we officially no longer have routine checkups for infants and toddlers, or annual checkups for older children. 

While the folks in charge acknowledge the system is slow and are putting in fixes to improve performance, the explanation for performance problems should be a lesson for all of us in clinical engineering/software architecture and design:

> AHLTA is slow, in part, for the same reason it is seen as revolutionary: information on millions of military patients is being stored in a single clinical data repository. But also the system &#8220;is single threaded,&#8221; said Marinkovich. &#8220;That means that for any particular transaction run for a particular user, you have to wait for that to finish before you can start another transaction.&#8221; It was designed &#8220;so as not to lose data,&#8221; Hendricks explained. 

The article is worth reading.

 [1]: http://www.military.com/features/0,15240,93457,00.html