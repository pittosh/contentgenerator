---
title: Do’s and Don’ts of hospital health IT
author: Shahid N. Shah
type: post
date: 2012-01-09T02:01:42+00:00
url: /2012/01/08/dos-and-donts-of-hospital-health-it/
oc_commit_id:
  - https://www.healthcareguy.com/2012/01/08/dos-and-donts-of-hospital-health-it/1478770778
dsq_thread_id:
  - 5175772361
categories:
  - Uncategorized

---
Last year I started a series of “Do’s and Dont’s” in hospital tech by [focusing on wireless technologies][1]. Folks asked a lot of questions about do’s and dont’s in other tech areas so here’s a list of more tips and tricks:

  * Do start [implementing cloud-based services][2]. Don’t think, though, that just because you are implementing cloud services that you will have less infrastructure or related work to do. Cloud services, especially in the SaaS realm, are “application-centric” solutions and as such the infrastructure requirements remain pretty substantial – especially the sophistication of the network infrastructure.
  * Do consider programmable and app-driven content management and document management systems as a core for their electronic health records instead of special-purpose EHR systems written decades ago. Don’t install new EHRs that don’t have robust document management capabilities. Do consider EHRs that can be easily integrated with document and content management systems like SharePoint or Alfresco.
  * Do go after virtualization for almost all apps – as soon as possible, make it so that no applications are sitting in physical servers. Don’t invest more in any apps that cannot easily be virtualized.
  * Do start looking at location-based asset tracking and app functionality; your equipment should be aware of where it’s physically sitting and be able to “find itself” and “track itself” using location-based awareness. Don’t invest heavily in systems that can not support location-based awareness (like potentially allow or disallow logins based on where someone is logging in from as well as enable / disable certain features in applications on where logins are occurring).
  * Do start implementing single sign on and common identity management with CCOW integration. Don’t invest in any systems that cannot meet common identity or SSO requirements.
  * Don’t make long-term decisions on mobile app platforms like iOS and Android because the mobile world is still quite young and the war between Apple, Microsoft, and Google is nowhere near being resolved. A platform that looks strong today may be weak tomorrow and become legacy quickly; however, HTML5 is not going anywhere and will be ultimate winner of the next 15 years just like HTML4 is the winner from 1995 to now. Do start investing in HTML 5 and CSS3 and away from HTML4. Don’t install any more apps that require IE6/7 or older browsers and don’t invest in systems that don’t have HTML5 in their roadmaps.
  * Don’t write applications on top of legacy EHR platforms; write applications with proper HL7 connectivity and platform independence. Most EHR platforms are using technologies that are either ancient or need to be replaced; by integrating deeply but remaining independent of their technologies you’ll get the best of both worlds.
  * Don’t buy any medical devices from vendors that don’t have a deep and thorough medical device to healthcare IT enterprise connectivity strategy. If a device doesn’t have wired or wireless TCP/IP access, doesn’t have data export or HL7 connectivity is not worth purchasing.
  * Don’t buy any thick-client applications that do not have thin-client “remote viewers” available.

 [1]: http://www.draeger.us/Pages/Campaigns/advances-in-wireless-technologies-for-healthcare.aspx
 [2]: https://www.healthcareguy.com/2011/12/24/healthcare-cloud-definitions-should-be-based-on-nists-definitions/