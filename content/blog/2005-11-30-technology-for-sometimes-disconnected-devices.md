---
title: Technology for networked medical devices
author: Shahid N. Shah
type: post
date: 2005-11-30T19:21:16+00:00
url: /2005/11/30/technology-for-sometimes-disconnected-devices/
oc_commit_id:
  - https://www.healthcareguy.com/2005/11/30/technology-for-sometimes-disconnected-devices/1478768941
views:
  - 1339
dsq_thread_id:
  - 5178634970
categories:
  - Opinion

---
It is very common for networked medical applications that need to work consistently even when momentarily disconnected. I ran across an interesting technology at IBM called [FluidSync][1]. It seems to be helpful in those situations when a user needs to use an application across several devices and be able to maintain the application state across the devices seamlessly. For example, if a nurse is moving between several rooms across several computers she would be able to run the same application across the machines and see the same data across the machines while she moves.

Seems very nice for data replication. Even better for _state_ replication, which is a bit more difficult. Using FluidSync one could imagine starting a transaction on one machine and completing it on another. Neat.

 [1]: http://www.alphaworks.ibm.com/tech/fluid?open&S_TACT=105AGX59&S_CMP=GR&ca=dgr-jw17awfluid