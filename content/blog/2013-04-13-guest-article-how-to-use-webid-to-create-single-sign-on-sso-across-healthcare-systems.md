---
title: 'Guest Article: How to use WebID to create Single Sign On (SSO) across Healthcare Systems'
author: Shahid N. Shah
type: post
date: 2013-04-14T00:25:23+00:00
url: /2013/04/13/guest-article-how-to-use-webid-to-create-single-sign-on-sso-across-healthcare-systems/
oc_commit_id:
  - https://www.healthcareguy.com/2013/04/13/guest-article-how-to-use-webid-to-create-single-sign-on-sso-across-healthcare-systems/1478770825
dsq_thread_id:
  - 5158492312
categories:
  - Uncategorized

---
_I have been speaking and writing often these days about how single sign on (SSO) technologies are probably one of the most important components of health IT data integration. To help figure out how to integrate multiple systems using standards-based SSO approaches I reached out to Shahid Qadri, a Data Scientist and Software Developer for <a href="http://appliedinformaticsinc.com/" target="_blank">Applied informatics Inc.</a> Qadri works on health data integration and semantic web and when I heard that he created a solution (which won second place) for an ONC single sign on challenge I thought he’d be the perfect engineer to help the rest of us. Here’s what Qadri had to say about WebID:_

The [Simple Sign-on challenge][1] sponsored by the ONC through the Health 2.0 challenge was an exciting opportunity for us to learn about a sophisticated technology protocol and then being able to hack several open source system to implement a single sign on solution based on the protocol. This was a challenge that was truly a “challenge” for me, but an exciting and rewarding one (our solution was the second place winner!). 

The challenge involved using the W3C [WebID][2] protocol to enable a single sign on across different systems used by the HealthData.gov Platform (HDP). The eventual goal of the HDP is to allow various administrators, contributors and even machines to be authenticated and authorized to access different open source systems. In a nutshell, our solution, OneLogin creates a “wrapper” over each of the systems (Drupal, Ontowiki, Virtuoso, Tomcat) that programmatically creates users within these systems with a given role and associates a given WebID with these users. Each tool’s wrapper is independent of the system and can be configured across different machines. The source code for OneLogin is [available][3] on GitHub.

[<img title="clip_image002" style="border-top: 0px; border-right: 0px; background-image: none; border-bottom: 0px; padding-top: 0px; padding-left: 0px; border-left: 0px; display: inline; padding-right: 0px" border="0" alt="clip_image002" src="/img/uploads/2013/04/clip_image002_thumb.jpg" width="524" height="379" />][4]

In rest of the blog post, I will describe the background and technical details of the solution.

WebID is a W3C open standard for identity and password-less login on the Web. WebID is designed to alleviate the difficulty (and pain) of remembering different logins, passwords and settings for different websites. WebID in itself is essentially a URL pointing to a description of yourself in FOAF format. [FOAF][5] stands for Friend Of A Friend and is essentially an [RDF][6] vocabulary which allows you to describe your social web) combined with a self-signed X.509 certificate. [X.509 certificates][7] (X-men like sounding terms) are the certifications used to verify the identity of web servers via the SSL protocol. It is a secure authentication protocol utilizing FOAF profile information as well as the SSL security layer available in virtually all modern web browsers. Operationally, once you have a WebID with private key stored in your browser, logging into a website is as simple as selecting your WebID and clicking "log in”. Additionally, there are other benefits of creating a WebID. Other people can to reference you and declare social relations on the web (such as that you are their friend, colleague, parent, etc.) even when their profile is hosted on a different web server than yours. Thus the WebID can be a trusted and verified way to enable the Social Web, i.e., social networks between individuals, citizens, companies, universities, governments, while allowing each player to remain in control of their data they publish.   
     **  
How Does WebID Work?**   
As mentioned before, the WebID is a URL, which points to a FOAF file. Now if you want to log into some site you simply provide the WebID which means to select a certificate from a list in your web browser. The server will then fetch the FOAF, extract the 

certificate’s public key from it, and then ask you to prove your identity. Since you are the only one having the private key of the certificate that is easily done. And that’s it. From a high level point of view it is very simple, but getting to the nuts and bolts of it can be a challenge.   
[<img title="clip_image004" style="border-top: 0px; border-right: 0px; background-image: none; border-bottom: 0px; padding-top: 0px; padding-left: 0px; border-left: 0px; display: inline; padding-right: 0px" border="0" alt="clip_image004" src="/img/uploads/2013/04/clip_image004_thumb.png" width="522" height="300" />][8]

(Source: http://www.w3.org/wiki/WebID)

**Is WebID Really Secure?**   
In order to secure and protect your identity two things need to be made ensured: 

1. The FOAF file that your WebID URL points to should be under your control or that of a trustworthy entity, and 

2. Make sure nobody steals your private key! Though, if you do lose your private key, disabling the WebID is as easy as removing the public key from your FOAF profile. Importantly, and this is a useful mechanism of decoupling the public key from the WebID url, is that replacing your public key certificate with a new one will never invalidate your WebID since it stays as a permanent identifier for yourself in the semantic web, independent of the certificate.

**Building the Single Sign-on OneLogin Application**

[<img title="clip_image005" style="border-top: 0px; border-right: 0px; background-image: none; border-bottom: 0px; padding-top: 0px; padding-left: 0px; border-left: 0px; display: inline; padding-right: 0px" border="0" hspace="12" alt="clip_image005" src="/img/uploads/2013/04/clip_image005_thumb.png" width="508" height="256" />][9]

First we started with Drupal and added a [module][10] in Drupal for providing WebID authentication. But configuring that got a bit tricky as we got few errors while using the module. For example, after digging into the module code we found there was a bug in the import statements. After resolving this we wrote code to automatically create a user in Drupal with the specified role who can use the his/her specified WebID to log in to Drupal.

**WebID Provider**

Next step involved setting up our own WebID provider (the service that generates a WebID). To do this, we chose to use the open source system, [Virtuoso][11] (an enterprise grade RDF store) that we installed on one of our servers over SSL/https. It generated WebID correctly, however, the WebIDs generated from it did not pass [verification test][12]. After close inspection we found that although the certificate was generated correctly, it was not getting the FOAF data in RDF format. So we installed an [RDF mapper][13] module to fix this and then we were able to generate WebIDs correctly.

Next we worked within Virtuoso to associate its internal users with a WebID, as it had a built-in support for WebIDs. We needed to write a wrapper that can programmatically create an account in Virtuoso and associate a WebID. So we developed a wrapper in PHP and ISQL for the same (the code can be [viewed here][14]) 

After configuring Virtuoso, we installed [OntoWiki][15]. We found that this platform also supports WebID authentication though it had been disabled in the current version in favor of OpenID. So we first got it enabled. Next we wrote the code to create a user and associate a WebID to it. The WebID user creation depends on the external plugin [Erfurt][16] in OntoWiki. After solving dependencies and other things we got our code working.

[<img title="clip_image006" style="border-top: 0px; border-right: 0px; background-image: none; border-bottom: 0px; padding-top: 0px; padding-left: 0px; border-left: 0px; display: inline; padding-right: 0px" border="0" alt="clip_image006" src="/img/uploads/2013/04/clip_image006_thumb.png" width="516" height="283" />][17]

Next and last was the associating WebID with Tomcat/Solr. After basic search we found that there is a library for providing WebID authentication to Tomcat/Solr. This library was not easy to use as we needed lot changes in installation and as well as configuring this library with Tomcat/Solr, but after rigorous efforts we were able to configure it correctly (more technical details are on [our blog][14]).

In order to build the code to programmatically create users and associating a WebID we had to tweak the tomcat-users.rdf file. This is where the user list and WebID are stored as nodes. We used a PHP XML parser to append users to the RDF file ([view code][14]) .

Finally, the application was build that created users and associated a role in each system and used WebID to login to each system. Included below is a screen shot of the Application with a link to the [GitHub repository][3] of the application. A demo video is also available [here][14]. 

[<img title="clip_image008" style="border-top: 0px; border-right: 0px; background-image: none; border-bottom: 0px; padding-top: 0px; padding-left: 0px; border-left: 0px; display: inline; padding-right: 0px" border="0" alt="clip_image008" src="/img/uploads/2013/04/clip_image008_thumb.jpg" width="522" height="344" />][18]

Screenshot of the OneLogin Single Sign on System

 [1]: http://challenge.gov/ONC/375-health-data-platform-simple-sign-on-challenge
 [2]: http://www.w3.org/wiki/WebID
 [3]: https://github.com/chintanop/onelogin-webid
 [4]: /img/uploads/2013/04/clip_image002.jpg
 [5]: http://www.foaf-project.org/
 [6]: http://www.w3.org/RDF/
 [7]: http://en.wikipedia.org/wiki/X.509
 [8]: /img/uploads/2013/04/clip_image004.png
 [9]: /img/uploads/2013/04/clip_image005.png
 [10]: http://drupal.org/project/webid
 [11]: http://virtuoso.openlinksw.com/
 [12]: https://foafssl.org/test/WebId%20or%20id.myopenlink.net/ods/webid_demo.html
 [13]: http://virtuoso.openlinksw.com/dataspace/doc/dav/wiki/Main/RDFMappers
 [14]: http://appliedinformaticsinc.com/onelogin-using-the-webid-protocol-for-creating-a-single-sign-on-across-drupal-solr-ontowiki-and-other-open-source-systems/
 [15]: http://ontowiki.net/Projects/OntoWiki
 [16]: https://github.com/AKSW/Erfurt/
 [17]: /img/uploads/2013/04/clip_image006.png
 [18]: /img/uploads/2013/04/clip_image008.jpg