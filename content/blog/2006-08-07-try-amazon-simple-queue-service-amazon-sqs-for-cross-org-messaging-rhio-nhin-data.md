---
title: Try Amazon Simple Queue Service (Amazon SQS) for cross-org messaging, RHIO, NHIN data
author: Shahid N. Shah
type: post
date: 2006-08-07T12:30:13+00:00
url: /2006/08/07/try-amazon-simple-queue-service-amazon-sqs-for-cross-org-messaging-rhio-nhin-data/
oc_commit_id:
  - https://www.healthcareguy.com/2006/08/07/try-amazon-simple-queue-service-amazon-sqs-for-cross-org-messaging-rhio-nhin-data/1478769054
views:
  - 3931
ratings_users:
  - 1
ratings_score:
  - 4
ratings_average:
  - 4
dsq_thread_id:
  - 44283552
categories:
  - Opinion

---
One of the foremost requirements of an Inter-Enterprise data interoperability (sending data _between_ organizations) solution like a RHIO or even NHIN is to have a solid messaging service or technology. Buying a messaging engine for inside the interprise is fairly easy but setting one up for cross-organizational use is not trivial.

One of the services that Amazon offers, called the [Simple Queue Service (Amazon SQS)][1], is a great option for multiple organizations that want to share data but don&#8217;t know how to do reliable messaging. Here&#8217;s what Amazon says about it:

> Amazon SQS offers a reliable, highly scalable hosted queue for storing messages as they travel between computers. By using Amazon SQS, developers can simply move data between distributed application components performing different tasks, without losing messages or requiring each component to be always available. Amazon SQS works by exposing Amazon&#8217;s web-scale messaging infrastructure as a web service. Any computer on the internet can add or read messages without any installed software or special firewall configurations. Components of applications using Amazon SQS can run independently, and do not need to be on the same network, developed with the same technologies, or running at the same time. 

The pricing is pretty reasonable, too: no startup costs and just 10 cents per 1,000 messages queued plus 20 cents per GB of data transferred. Not bad at all.

[Check it out][1] and start interoperating without all the hosting headaches.

 [1]: http://www.amazon.com/gp/browse.html/ref=aws_nl_17aSqsdp?node=13584001