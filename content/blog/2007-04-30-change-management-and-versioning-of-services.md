---
title: Change management and versioning of services
author: Shahid N. Shah
type: post
date: 2007-04-30T13:20:23+00:00
url: /2007/04/30/change-management-and-versioning-of-services/
oc_commit_id:
  - https://www.healthcareguy.com/2007/04/30/change-management-and-versioning-of-services/1478769124
views:
  - 2031
dsq_thread_id:
  - 44283737
categories:
  - Opinion

---
We&#8217;ve been having a nice discussion on the management of services and how services should be versioned on our Microsoft Architect MVP discussion list. This morning I saw a note from Martin Fowler pointing to an article on [Consumer-driven Contracts][1]. The article is definitely worth reading, and here&#8217;s the abstract:

> This article discusses some of the challenges in evolving a community of service providers and consumers. It describes some of the coupling issues that arise when service providers change parts of their contract, particularly document schemas, and identifies two well-understood strategies &#8211; adding schema extension points and performing &#8220;just enough&#8221; validation of received messages &#8211; for mitigating such issues. Both strategies help protect consumers from changes to a provider contract, but neither of them gives the provider any insight into the ways it is being used and the obligations it must maintain as it evolves. Drawing on the assertion-based language of one of these mitigation strategies &#8211; the &#8220;just enough&#8221; validation strategy &#8211; the article then describes the &#8220;Consumer-Driven Contract&#8221; pattern, which imbues providers with insight into their consumer obligations, and focuses service evolution around the delivery of the key business functionality demanded by consumers.

 [1]: http://martinfowler.com/articles/consumerDrivenContracts.html