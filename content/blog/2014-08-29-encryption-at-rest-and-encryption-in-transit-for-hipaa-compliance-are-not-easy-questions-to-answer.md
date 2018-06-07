---
title: Encryption at rest and encryption in transit for HIPAA compliance are not easy questions to answer
author: Shahid N. Shah
type: post
date: 2014-08-29T08:24:01+00:00
url: /2014/08/29/encryption-at-rest-and-encryption-in-transit-for-hipaa-compliance-are-not-easy-questions-to-answer/
oc_commit_id:
  - https://www.healthcareguy.com/2014/08/29/encryption-at-rest-and-encryption-in-transit-for-hipaa-compliance-are-not-easy-questions-to-answer/1478770881
  - https://www.healthcareguy.com/encryption-at-rest-and-encryption-in-transit-for-hipaa-compliance-are-not-easy-questions-to-answer/1420536241
oc_metadata:
  - |
    {		version:'1.1',		tags: {'healthcare-institutions': {"text":"healthcare institutions","slug":"healthcare-institutions","source":{"_className":"Entity","url":"http://d.opencalais.com/genericHasher-1/2f0ba821-5aae-3e14-8bb4-97a2a81619b3","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/em/e/IndustryTerm","name":"IndustryTerm"},"name":"healthcare institutions","rawRelevance":0.333,"normalizedRelevance":0.333},"bucketName":"blacklisted","bucketPlacement":"user","_className":"Tag"}, 'law': {"text":"law","slug":"law","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'hipaa': {"text":"HIPAA","slug":"hipaa","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'health-insurance-portability-and-accountability-act': {"text":"Health Insurance Portability And Accountability Act","slug":"health-insurance-portability-and-accountability-act","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'privacy-law': {"text":"Privacy Law","slug":"privacy-law","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'privacy': {"text":"Privacy","slug":"privacy","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, '-healthcare-institutions': {"text":" healthcare institutions","slug":"-healthcare-institutions","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}}	}
dsq_thread_id:
  - 5160287786
categories:
  - Government Regulations
  - Information Assurance (IA) and Security
  - Patient Self-Management
tags:
  - Health Insurance Portability And Accountability Act
  - healthcare institutions
  - HIPAA
  - law
  - Privacy
  - Privacy Law

---
Given the number of breaches we&#8217;ve seen this Summer at healthcare institutions, I&#8217;ve just spent a ton of time recently on several engineering engagements looking at &#8220;HIPAA compliant&#8221; encryption (HIPAA compliance is in quotes since it&#8217;s generally meaningless). Since I&#8217;ve heard a number of developers say &#8220;we&#8217;re HIPAA compliant because we encrypt our data&#8221; I wanted to take a moment to unbundle that statement and make sure we all understand what that means. Cryptology in general and encryption specifically are difficult to accomplish; CISOs, CIOs, HIPAA compliance officers shouldn&#8217;t just believe vendors who say &#8220;we encrypt our data&#8221; without asking for elaboration in these areas:

  * Encryption status of data at rest in block storage (the file system that the apps, databases, VMs, are stored on)
  * Encryption status of data at rest in virtual machine block storage
  * Encryption status of data at rest in archived storage (backups)
  * Encryption status of data at rest in the Oracle/SQL*Server/DB2/MySQL/Postgre/(your vendor) databases (which sits on top of the file system)
  * Encryption status of data in transit from database to app server
  * Encryption status of data in transit from app server to proxy server (HTTP server)
  * Encryption status of data in transit from proxy server to end user’s client
  * Encryption status of data in transit from API servers to end user’s clients (iOS, Android, etc.)
  * Encryption status of server to server file transfers
  * Encryption key management in all of the above

When you look at encrypting data, it&#8217;s not just &#8220;in transit&#8221; or &#8220;at rest&#8221; but can be in transiting or resting in a variety of places.

If you care about security, ask for the details.