---
title: De-identifiying protected health information (PHI)
author: Shahid N. Shah
type: post
date: 2006-01-31T19:54:01+00:00
url: /2006/01/31/de-identifiying-personal-health-information-phi/
oc_commit_id:
  - https://www.healthcareguy.com/2006/01/31/de-identifiying-personal-health-information-phi/1478768998
views:
  - 2660
dsq_thread_id:
  - 44283386
categories:
  - Opinion

---
A number of clients have been asking me about protected health information (PHI) solutions so I thought I&#8217;d put out a general call for help from my esteemed readers. What I&#8217;m looking for is a general-purpose data de-identification library (preferably open source) that I could use in both OSS and commercial systems. Even if it costs money, I&#8217;d love to hear about it.

The idea is to be able to find PHI automatically in any arbitrary data packet (HL7, e-mail, database, etc), be able to flag it, do a one-way hash, tokenize it, add it to a dictionary, etc. There are many uses for this kind of software from automatically scanning outgoing emails to protecting sensitive data within databases so data can be aggregated and shared.

A thought leader in the de-identification and data privacy space is [Dr. Latanya Sweeney][1] who teaches at CMU. She has some really nice stuff, though I don&#8217;t think it&#8217;s open source or available online.

A commercial firm that does this stuff is called [De-ID][2]. NIH&#8217;s [National Cancer Institute][3] uses them for their projects, too, so it&#8217;s probably pretty good.

Please drop me some comments here if you know of other researchers that might have some stuff available that they can share. While finished products would be great, even research projects are welcome.

 [1]: http://lab.privacy.cs.cmu.edu/people/sweeney/
 [2]: http://www.de-id.com/
 [3]: http://news.taborcommunications.com/msgget.jsp?mid=471538&xsl=story.xsl