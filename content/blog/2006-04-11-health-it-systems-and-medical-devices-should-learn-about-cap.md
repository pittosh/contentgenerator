---
title: Health IT systems and medical devices should learn about CAP
author: Shahid N. Shah
type: post
date: 2006-04-11T13:26:46+00:00
url: /2006/04/11/health-it-systems-and-medical-devices-should-learn-about-cap/
oc_commit_id:
  - https://www.healthcareguy.com/2006/04/11/health-it-systems-and-medical-devices-should-learn-about-cap/1478769031
views:
  - 1620
dsq_thread_id:
  - 44283481
categories:
  - Opinion

---
The [Common Alerting Protocol (CAP)][1] and Emergency Data Exchange Language (EDXL) are two standards that have been promoted by organizations that need to transfer information to each other during times of emergencies (natural disasters, terrorist incidents, etc). There are lots of vendors supporting CAP but I haven&#8217;t seen much use within health IT or medical devices so I thought I&#8217;d blog about what CAP and EDXL are so that our CIO and CTO readers out there can help their own teams understand why it might be important to learn about the standards.

Here&#8217;s is CAP&#8217;s purpose:

  * Simple and standardized format for exchanging alerts and warnings over various types of networks
  * Compatible with legacy and emerging “transport” methods, such as NOAA National Weather Radio specification and Web Services
  * Flexible geographic targeting
  * Phased and delayed effective times and expirations
  * Message update and cancellation features
  * Facility for including inline digital images and audio

As you can see, the most important purpose of CAP is to allow exchanging of alerts and warnings. Given that hospitals and ambulances are first responders we would assume there is some strategy in hospital IT departments to allow reading and writing of CAP messages. At first glance, it seems like there is not much reason for health IT or medical software to know about or share CAP messages. However, if the software we write gets smarter about diseases and clinical decision making we could use something like CAP to help inform CDC and FDA for hazards, infections, etc. Medical device manufacturers could use CAP to report adverse events to their own internal IT systems and CAP gateways could help route important messages outside the hospital.

There are lots of implications of CAP and EDXL. If you have started using these standards or feel like they are not applicable to health IT systems, share your thoughts with your colleagues by dropping a comment here.

 [1]: http://www.incident.com/cookbook/index.php/A_Roadmap_to_Emergency_Data_Standards