---
title: 'Buyer beware: encryption does not mean application security'
author: Shahid N. Shah
type: post
date: 2005-11-08T13:10:15+00:00
url: /2005/11/08/buyer-beware-encryption-does-not-mean-application-security/
oc_commit_id:
  - https://www.healthcareguy.com/2005/11/08/buyer-beware-encryption-does-not-mean-application-security/1478768900
views:
  - 1207
dsq_thread_id:
  - 44283048
categories:
  - Opinion

---
It&#8217;s funny that most of my time during a review or evaluation of web based healthcare IT systems when I bring up the issue of security the salesperson almost always says &#8220;yes, we use SSL.&#8221;

There&#8217;s a great of deal of growth in EMRs, EHRs, and other healthcare applications that will be web hosted over a WAN like the Internet or via a VPN. One thing that all IT community members and architects should be very clear about in our world is that SSL (encryption) is not the same thing as application security. You can have the best encryption in the world and still have a healthcare application full of holes that allows sensitive medical data to be released without your knowledge.

SSL encryption is great for making sure that data transfer is safe and that passwords and other sensitive health information is not passed in clear text over the wire. However, application security is much more than encryption and when choosing and installing modern applications ask the vendors about the following major security threats:

  * **SQL Injection** &#8211; how does the vendor ensure that the end users of applications can not send arbitrary SQL into the database? Don&#8217;t take simple answers and ask for specific techniques, QA mechanisms, etc. SQL injection is a _very common_ problem in most web based applications and is difficult to catch without code inspections.
  * **Cross Site Scripting (CSS)** &#8211; how does the vendor make sure that an end user can&#8217;t just inject JavaScript into forms and fields and take over the application? Like SQL injection, CSS is a terribly common and easy to overlook but it can allow non technical users to break into your healthcare data.
  * **Parameter Tampering** &#8211; many vendors poorly manage URL parameter validation meaning end users can simply tinker with URLs and gain more privileges or circumvent security.
  * **Buffer Overflows** &#8211; these are the standard attacks but can be overcome pretty easily using modern languages like C# and Java in many cases.
  * **Using excessive privileges** &#8211; sometimes roles and permissions are overgranted. Ask the vendor for a security document that describes all permissions and roles in the system and risks associated with each one of them.
  * **Insecure coding practices** &#8211; unless the vendor has a coding security practices/policy document in place it&#8217;s likely the software may be full of holes they may not even know about. Demand to see the QA and security plans associated with software development.

Your application vendor should be able to speak to the following major security issues. Ask them to elaborate on all of them and if anything sounds fishy, probe further.

  * Identification &#8211; what identity management system is in use?
  * Authentication &#8211; what governs how an application authenticates as user?
  * Authorization &#8211; what governs the rules for authorizing valid users to specific tasks and keeping them away from others?
  * Integrity &#8211; how does the application ensure that information will not be changed, altered, or lost in an unauthorized or accidental manner?
  * Confidentiality &#8211; how can the application validate that no unauthorized party or process can access or disclose the information?
  * Auditing &#8211; are all transactions recorded so that problems can be analyzed after the fact?
  * Non-repudiation &#8211; does the system provide a way to ensure that parties are able to provide legal proof to a third party that the sender did send the information, and the receiver received the identical information? 

Just remember, security is more than just &#8220;using SSL&#8221;.