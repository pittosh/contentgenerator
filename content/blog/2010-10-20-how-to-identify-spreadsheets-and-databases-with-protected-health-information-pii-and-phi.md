---
title: How to identify spreadsheets and databases with protected health information (PII and PHI)
author: Shahid N. Shah
type: post
date: 2010-10-20T14:19:22+00:00
url: /2010/10/20/how-to-identify-spreadsheets-and-databases-with-protected-health-information-pii-and-phi/
oc_commit_id:
  - https://www.healthcareguy.com/2010/10/20/how-to-identify-spreadsheets-and-databases-with-protected-health-information-pii-and-phi/1478770710
dsq_thread_id:
  - 5197542740
categories:
  - Uncategorized

---
The nice folks from IBM&#8217;s developerWorks group asked me to write an intermediate-level set of instructions (with a little code) for how technical teams can identify and find databases and spreadsheets that might contain personally identifiable information (PII) and protected health information (PHI).

[The article is now available on IBM&#8217;s developerWorks][1], here&#8217;s the abstract:

> Identity theft and medical fraud are growing problems. They are so big the U.S. government is spending billions of dollars securing its own computer systems and has written thousands of pages of new regulations that you must follow to help protect your customer and employee data. To comply with new regulations and properly secure data, you will need to find personally identifiable information (PII) and protected health information (PHI) in your databases and documents. Both PHI and PII are conceptually easy to understand but very difficult to track in the thousands of relational data stores, files, and spreadsheets that make up a typical organization&#8217;s IT environment. This article describes some methods to automatically identify and inventory PII, PHI, and other sensitive data with databases and spreadsheets using Java™ technology and the Apache Ant build tool.

Don&#8217;t forget that there are open source and commercial scanning tools start with similar functionality but add more features. When you look for third-party tools, consider automated discovery (the tools automatically find databases and record sources with PII/PHI), configurable templates (you add your own rules), broad coverage (all files, databases, and network transfers are covered), content scanning, and auditing.

Please check out [my developerWorks article][1] and comment either directly on the IBM site or drop me some notes here about what you think about it.

 [1]: http://www.ibm.com/developerworks/industry/library/ind-findpii/index.html