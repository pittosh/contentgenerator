---
title: 'Guest Article: Google Health and HealthVault App Integration from the trenches'
author: Shahid N. Shah
type: post
date: 2009-01-27T16:41:08+00:00
url: /2009/01/27/guest-article-google-health-and-healthvault-app-integration-from-the-trenches/
oc_commit_id:
  - https://www.healthcareguy.com/2009/01/27/guest-article-google-health-and-healthvault-app-integration-from-the-trenches/1478770433
views:
  - 397
ratings_users:
  - 8
ratings_score:
  - 39
ratings_average:
  - 4.88
dsq_thread_id:
  - 5157992219
categories:
  - Opinion

---
_I liked what the folks are doing at [TrialX][1], especially their integration with HealthVault and Google Health so I invited them to write share with us what they’ve learned. Chintan Patel is a co-founder and the CTO of_ [_TrialX_][1]_, a startup that is developing social and semantic technologies to enable patients find matching clinical trials using Personal Health Records (PHRs). They’ve got some good ideas around easing patient recruitment for trials. Here’s what Chintan had to say about PHR integration from the trenches._

If you are reading this post there is a good chance that you must also be reading/hearing stories on new partnerships of [Google Health][2] (GH) and [Microsoft HealthVault][3] (MHV) with healthcare providers and software application developers. This makes one wonder about the details of integration with these application platforms. _What are the common features? What are the differences?_ _How easy or hard is the technical integration?_

In this blog, we provide a glimpse of these platforms based on our experiences at [TrialX][4], a personalized clinical trial matching application integrated with both GH and MHV platforms. 

The big plus about both GH and MHV is the availability of well-documented APIs (Application Programming Interfaces) and use of health information standards (such as ASTM CCR) to store, transfer and retrieve users’ health records. This has enabled two things:

  1. Healthcare providers can now empower patients and their family members to take control of their health information by informing them to import medical records to these platforms. 
  2. Healthcare software and device developers can develop personalized services for individual users by utilizing the patient’s health information from these platforms. 

In this new eco-system of health information providers and consumers, **information privacy and control** becomes an important issue. Both platforms have implemented the highest standard of web security into their models with use of digital certificates and end-to-end public key encryption. However, there is one important difference in terms of information control – MHV provides granular information control to users for specific data-types. For example, TrialX uses patients’ basic demographics and medical conditions data to provide relevant clinical trials, hence the user has to specifically consent TrialX to use both data elements from MHV and this prevents other data elements from being made visible to TrialX. On the other hand, GH enables querying of different sections of a single users’ medical record or across multiple user records, who have explicitly consented the use of a given application. 

In terms of **technical integration** both GH and MHV use standards-based REST and SOAP communication layers respectively. However, GH provides application development library support across multiple programming languages such Java, .NET, Ruby, Python and so on, whereas HealthVault is mainly available through .NET with a few open-source projects in Java and Ruby. At TrialX, we had to develop an in-house Python-based library to communicate with HealthVault that is now available as an [open-source toolkit, pyHealthVault][5].

With regards to **user-workflow and interaction models** there are significant differences between both platforms. As commonly explained by Microsoft folks “[Google is like Facebook and HealthVault is like PayPal][6].” The difference in the two models has important implications for an application’s visibility, user uptake and scalability. For example, when a user adds (links) a GH application to their health profile, as per GH requirements, the user has to create an additional account with the third-party application site and link this new account with their GH account. MHV on the other hand, allows users to use their Live.com username or Open ID to copy or sync the health information from the third-party site directly, without having to create a new account.

There are many other details about the similarities and differences between the two platforms and we will continue to write about [them at our blog][7]. However, these are merely technical details and are trivial compared to the big picture benefits that the platforms are hoping to drive through. 

Driven by this impending inversion of control of health information and patient empowerment that the PHRs may enable, the real winner is the consumer and ultimately the healthcare system. These sure are exciting times in healthcare IT and we at TrialX could not be more excited to be part of the next big revolution.

 [1]: http://trialx.org
 [2]: http://google.com/health
 [3]: http://healthvault.com/
 [4]: http://trialx.org/
 [5]: http://code.google.com/p/pyhealthvault/
 [6]: http://www.crn.com/healthcare/212101164
 [7]: http://blog.trialx.org/