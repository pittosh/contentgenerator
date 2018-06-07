---
title: 'Guest Article: Shakespeare in Namespace, or why Blue Button took off as fast as it did'
author: Shahid N. Shah
type: post
date: 2013-06-15T15:05:24+00:00
url: /2013/06/15/guest-article-shakespeare-in-namespace-or-why-blue-button-took-off-as-fast-as-it-did/
oc_commit_id:
  - https://www.healthcareguy.com/2013/06/15/guest-article-shakespeare-in-namespace-or-why-blue-button-took-off-as-fast-as-it-did/1478770836
  - https://www.healthcareguy.com/guest-article-shakespeare-in-namespace-or-why-blue-button-took-off-as-fast-as-it-did/1420433705
dsq_thread_id:
  - 1403498297
oc_metadata:
  - |
    {		version:'1.1',		tags: {'namespace': {"text":"Namespace","slug":"namespace","source":{"_className":"SocialTag","url":"http://d.opencalais.com/dochash-1/4b40c6c5-0edd-3171-82c1-d7eedf58cb37/SocialTag/3","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/tag/SocialTag","name":"SocialTag"},"name":"Namespace","makeMeATag":true,"importance":1,"normalizedRelevance":1},"bucketName":"blacklisted","bucketPlacement":"user","_className":"Tag"}, 'lithography': {"text":"lithography","slug":"lithography","source":{"_className":"Entity","url":"http://d.opencalais.com/genericHasher-1/3d59bca3-fc12-3784-9660-82bdca678531","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/em/e/Technology","name":"Technology"},"name":"lithography","rawRelevance":0.427,"normalizedRelevance":0.427},"bucketName":"blacklisted","bucketPlacement":"user","_className":"Tag"}, 'john-wilbanks': {"text":"John Wilbanks","slug":"john-wilbanks","source":{"_className":"Entity","url":"http://d.opencalais.com/pershash-1/1a10a9a0-6e3d-3094-84c8-57074f9122ff","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/em/e/Person","name":"Person"},"name":"John Wilbanks","rawRelevance":0.164,"normalizedRelevance":0.164},"bucketName":"blacklisted","bucketPlacement":"user","_className":"Tag"}, 'peter-levin': {"text":"Peter Levin","slug":"peter-levin","source":{"_className":"Entity","url":"http://d.opencalais.com/pershash-1/b6a2f7a2-8d0b-39d3-9b0d-b3e83939dc0a","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/em/e/Person","name":"Person"},"name":"Peter Levin","rawRelevance":0.74,"normalizedRelevance":0.74},"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'data-management': {"text":"data management","slug":"data-management","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'data': {"text":"data","slug":"data","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'blue-button': {"text":"blue button","slug":"blue-button","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}}	}
categories:
  - Engineering
  - Open Source
  - Telehealth
  - Telemedicine
tags:
  - blue button
  - Data
  - Data Management
  - Peter Levin

---
_I had the privilege of working with [Dr. Peter Levin][1] as an outside technology strategy adviser while he was the Chief Technology Officer (CTO) of Veterans Affairs during the first Obama Administration. Peter&#8217;s a hard-charging, fast-moving, take-no-prisoners style senior technical executive; he was an entrepreneur, professor, and engineer long before he came into government so it was no surprise that he was able to accomplish a great deal during his tenure as the CTO of VA. Two of his most enduring accomplishments that affect the healthcare world writ large are his inaugural deployment of the [Blue Button][2] at the VA and helping spin out the VistA EHR source code into [OSEHRA][3]. He’s too modest to say it himself but I like to refer to him as the “father of the [Blue Button][2]” because I don’t think it would have taken off the way it did without his design leadership and his ability to knock heads together (including mine) both in and outside the VA to make it happen. Recently I asked him why he thought, beyond the obvious reasons of high value to veterans and other patients, that Blue Button took as fast as it did. Here’s what Peter had to say:_

One of my favorite books is “[Too Big to Know][4]”, by Harvard University’s [David Weinberger][5].  If you have a chance, jump to page 145, under the heading “when scientists disagree with scientists”, which is a brilliant exposition on the enormous technical impact and societal (yes, I mean everybody’s) benefit of a very simple concept called “the namespace”.

While Veterans Affairs was struggling with the nuances of the implementation of the [Blue Button personal health record][6], and while the VA and the Pentagon are wrestling the [Health Data Dictionary][7] to the ground, we lived – and lived through – the hell of multiple rigid conventions described in Weinberger’s book.

The rock soup of medical databases is born of three bitter ingredients:  first, the natural human tendency, especially among scientists and technologists, and fully bloomed in the healthcare industry, to a) believe you’re right at all times and b) to defend your turf at all costs against all comers, including those just meandering by, with no intention of spending the night.

Second, the “standards bodies” were more corporeal than standard.  In contrast to, say, the world of semiconductor manufacturing (which created a multi-hundred billion dollar industry based on standard lithography techniques) and electric power distribution (the plug-and-socket distribution system that has worked so well) to name just two of my many favorites, there is scant little agreement between hospitals, between vendors, and between systems about how to get medical data from one place to another.  Still.  Today.  And let’s save for another time about what we’re doing &#8211; and not doing &#8211; to keep the digital pipes clean of cybersnoops and other digital detritus.

Finally, we had not heard of, and were a little slow to embrace, the concept of a namespace.  This crazy simple idea is the Shakespearean notion – sorry, there’s no other way to say it – that we do not need to agree on the names of things to agree on what they are.  Weinberger, for example, quotes [John Wilbanks][8], formerly head of science at Creative Commons, in a gentle explanation that I love to share: “There may be fifty or sixty names referring to any particular gene.  A database of yeast genes has a lot in common with a database of fish genes, but they were written by different people who gave them different names.  If you want to retrieve everything we know about a gene, you can’t . . . unless someone tells the computer that all those different labels refer to the same thing”.

Exactly.  Like what we mean by first name, last name, place, medicine, allergy, and problem.  Regardless of how you code yours and I code mine.  A rose is a rose by any other name.

In fact, it is a rose in all languages, and we should quit wasting time, money, and lives arguing about it.  To quote Weinberger again, “[n]amespaces enable people to disagree about how to classify and name things, while allowing computer programs to pull information together from both of them, so long as the computer knows how to map names from one namespace to another”.  Now, I do not mean to trivialize how easy it is to do that.  But it’s not rocket science either.  We just have to sit down and get started.

My good friend Roger Baker is fond of saying, “there’s nothing that wins an argument quite like customer facing software”; Levin’s corollary is “delivered on time and below budget”.  It’s why ideas like email, lithography, and the ubiquitous household socket and, yes, Blue Button took off:  we spent our time figuring out how to connect the protocols and databases to each other, and saved our shekels for applications – for instance computer chips and kitchen toasters – not make-believe standards that everybody wanted but nobody had.

 [1]: http://en.wikipedia.org/wiki/Peter_L._Levin
 [2]: http://en.wikipedia.org/wiki/The_Blue_Button
 [3]: http://www.oshehra.org
 [4]: http://ebookbrowse.com/too-big-to-know-weinberger-en-16803-pdf-d435286193
 [5]: http://cyber.law.harvard.edu/people/dweinberger
 [6]: http://www.va.gov/bluebutton/
 [7]: http://www.hddaccess.com/
 [8]: http://sciencecommons.org/about/whoweare/wilbanks/