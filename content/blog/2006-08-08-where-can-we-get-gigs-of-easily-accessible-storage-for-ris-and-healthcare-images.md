---
title: Where can we get gigs of easily accessible storage for RIS and healthcare images?
author: Shahid N. Shah
type: post
date: 2006-08-08T01:45:46+00:00
url: /2006/08/08/where-can-we-get-gigs-of-easily-accessible-storage-for-ris-and-healthcare-images/
oc_commit_id:
  - https://www.healthcareguy.com/2006/08/08/where-can-we-get-gigs-of-easily-accessible-storage-for-ris-and-healthcare-images/1478769055
ratings_users:
  - 1
ratings_score:
  - 4
ratings_average:
  - 4
views:
  - 1609
dsq_thread_id:
  - 44283553
categories:
  - Opinion

---
If you&#8217;re looking for Inter-Enterprise storage of large files such as RIS images (where images need to be securely shared between organizations), check out [Amazon Simple Storage Service (Amazon S3)][1]. This inexpensive service may have the right mix of price, performance, and scalability take care of your requirements. Here&#8217;s what Amazon says about it:

  * Write, read, and delete objects containing from 1 byte to 5 gigabytes of data each. The number of objects you can store is unlimited.
  * Each object is stored and retrieved via a unique, developer-assigned key.
  * Authentication mechanisms are provided to ensure that data is kept secure from unauthorized access. Objects can be made private or public, and rights can be granted to specific users.
  * Uses standards-based REST and SOAP interfaces designed to work with any Internet-development toolkit.
  * Built to be flexible so that protocol or functional layers can easily be added. Default download protocol is HTTP. A BitTorrent(TM) protocol interface is provided to lower costs for high-scale distribution. Additional interfaces will be added in the future. 

Pricing is very reasonable since you only pay only for what you use. There is no minimum fee, and no start-up cost. 15 cents per GB-Month of storage used. 20 cents per GB of data transferred.

 [1]: http://www.amazon.com/b/ref=sc_fe_l_2/103-2433493-3963019?ie=UTF8&node=16427261&no=15879911&me=A36L942TSJ2AJA