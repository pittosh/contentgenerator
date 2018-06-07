---
title: 'Guest Article: Rich Internet Applications for Improved Healthcare App User Experience'
author: Shahid N. Shah
type: post
date: 2007-10-15T14:32:16+00:00
url: /2007/10/15/guest-article-rich-internet-applications-for-improved-healthcare-app-user-experience/
oc_commit_id:
  - https://www.healthcareguy.com/2007/10/15/guest-article-rich-internet-applications-for-improved-healthcare-app-user-experience/1478769150
views:
  - 3300
ratings_users:
  - 3
ratings_score:
  - 9
ratings_average:
  - 3
dsq_thread_id:
  - 5159033092
categories:
  - Opinion

---
</p> 

_I&#8217;m a huge fan of thin-client systems but the thinner the client, the less functionality it seems to support. A pretty smart colleague of mine, François Jean, is an engineer at Cardinal Health working on a bed side information system and he has some suggestions for healthcare IT systems that need to stay thin for deployment but remain just as functional as a desktop app. François has more than 10 years of experience in the computer science field and is interested in simplifying and improving the quality of software for a faster time to market while maintaining a stellar customer experience. He&#8217;s in Cardinal&#8217;s Operational Excellence program where he&#8217;s training to become a Lean/Six-Sigma Green Belt. François has a master&#8217;s in Artificial Intelligence, a baccalaureate in philosophy and another one in computer science/mathematics. All that means he&#8217;s very well qualified and you should take his advice. :-). He writes:_ 

Shahid, [your article about SaaS][1] was very interesting. I’m a big fan of web based applications for the following reasons: available from almost everywhere, do not necessitate any installation on the client side, are always up to date and the client does not have to worry about backup or hardware maintenance. However, your article highlights two very important issues related to these types of applications: availability and privacy. Both of them are VERY important in healthcare and we should address them in every implementation of SaaS. 

A very good but often undervalued option for SaaS applications is the RIA ([Rich Internet application][2]) model. RIA can be used to bridge the gap between the rich API interface provided by the SaaS application and desktop-style user experience. RIA are basically web applications that have the features and functionality of traditional desktop applications. In other words, you experience the feeling of a desktop application in a web based application. Freely available examples of this include&nbsp;Google mail, New Yahoo! Mail, Google docs, Google Maps, etc. 

Different frameworks are available to develop these applications; currently at my company we are exploring [OpenLaszlo][3]. We&#8217;ve use it to create Flash applications but it can also be used to create “lighter” applications (DHTML) for less powerful devices. OpenLaszlo can seamlessly generate applications supporting a wide array of browsers (including the [safari browser on the iPhone][4]!). 

In our case, we wanted to replace a very simple JSP based application with a more RIA based solution to improve the user experience, we wanted the ability to refresh the content of a page without reloading it, have drag and drop functionality, have a fast response time on the client and more important to be free from any HTML and JavaScript limitation. 

Since our OpenLaszlo application was able to talk to our backend using standard SOAP Web Service calls; no effort was lost in updating our backend. There is a learning curve before becoming efficient with the OpenLaszlo framework but the productivity gain from this framework rewarded the effort we put into. 

Our application succeeds in delivering a desktop like experience to the user. In fact, once the application is running in full screen, you cannot tell it’s a Web application. There are many advantages: 

  * No need to install anything on the client; 
  * The client has always the most recent version of the application; 
  * Very light weight (compare to a Java applet); 
  * Fast and no flickering while updating the content of a page (unlike many web based application). 
  * Run everywhere in almost every browser; 

Some disadvantages: 

  * A network problem could stop everyone (but desktop application tends to depend more and more on networks);&nbsp;
  * Data are stored remotely, privacy issue must be addressed;&nbsp;
  * Requires a solid backend infrastructure to prevent any downtime; 

In our case, we could also have used the Adobe Flex framework to develop our Flash application. We choose OpenLaszlo mainly because it enables us to deliver our application on a variety of platforms (I must admit that we only deliver our application under Flash). 

You would like to add multimedia, video conference or voice chat to your RIA? OpenLaszlo support it through the “red5” open source Flash Server. We had no use for it in our application, but we did some tests and were able to have a video chat application running in our browser in less than one day. 

I personally believe in RIA for healthcare applications and our experience shows us that we can create a web application with a very good user experience. The user experience in health care is very important; we must be able to give the best feedback possible to the user and let him do his task the most naturally possible. The interface should never be an obstacle between the healthcare personnel and the reality they try to describe/comprehend through the interface they have between them and the data.

 [1]: https://www.healthcareguy.com/index.php/archives/392
 [2]: http://en.wikipedia.org/wiki/Rich_Internet_application
 [3]: http://www.openlaszlo.org/
 [4]: http://weblog.openlaszlo.org/archives/2007/09/iphone-application-development-step-by-step/