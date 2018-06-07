---
title: Getting small databases like Access and Excel under control
author: Shahid N. Shah
type: post
date: 2006-09-10T11:51:07+00:00
url: /2006/09/10/getting-small-databases-like-access-and-excel-under-control/
oc_commit_id:
  - https://www.healthcareguy.com/2006/09/10/getting-small-databases-like-access-and-excel-under-control/1478769066
views:
  - 3380
ratings_users:
  - 8
ratings_score:
  - 39
ratings_average:
  - 4.88
dsq_thread_id:
  - 5158275494
categories:
  - Opinion

---
One of the most difficult tasks I have seen my customers grapple with as I advise them on technology strategy for their information management needs is how to get a handle on those pesky Microsoft Access and Excel &#8220;files&#8221;. While we tend to treat these&nbsp;&#8220;documents&#8221; as simple file management problems they are far more than that: they are real applications and they are real databases with complete enterprise architecture impacts. I remember at one of my clients when were doing analysis of HIPAA privacy concerns related to patient information we calculated over a thousand MS Access and Excel &#8220;files&#8221; with health data that needed to be protected.

What can be done to rope in these real (small but important) databases and get them under control? First, we need to figure out why people use Access and Excel. Well, that&#8217;s simple: with those tools users are in control, they don&#8217;t need permission from the CIO to create a new app or database, they can connect to external databases, and most importantly _they get their job done_. Now, if you can give them those same capabilities but in a centralized manner, would your users use it and let you manage, secure, catalog,&nbsp;backup, and protect the data? The answer is: probably not immediate-term, but certainly yes in the medium- and long-term if you can setup appropriate policies.

So, how do you give your users those features? Well, a new class of end-user-friendly application-creators are hitting the market. There are enterprise-hosted systems like [Caspio][1] and Internet-hosted systems like [Zoho Creator][2]. Zoho Creator is currently more feature rich than Caspio but Caspio is pretty user friendly and can be installed behind your firewalls and the data goes into your own (SQL Server) databases instead of sitting on the Internet. I&#8217;ve spoken to the folks at Zoho Creator and they said they are working on an enterprise-hostable system that should be ready soon as well.

By setting up a server or service and training your users to use the new tools _instead_ of Access and Excel, they can:

  * Create applications from scratch 
      * Create applications using templates that other users (or you) can create for them 
          * Create applications by importing existing spreadsheets or databases 
              * Share applications with their colleagues and clients _without sending secure data via email_ 
                  * Get email notifications when records are added/updated but only notifications (not the data) is sent across mail 
                      * Export data in formats that be analyzed in Excel or Access</ul> 
                    Here&#8217;s what you get out of systems like these: 
                    
                      * Manage the tool and the database server and all your data is in one place instead of strewn across hundreds of spreadsheets and little databases files
                      * Secure the data and protect health information centrally
                      * Look at the kinds of applications users are creating and learn from the requirements they&#8217;re fulfilling themselves to see if your group should be doing that work instead of users creating custom apps

 [1]: http://www.caspio.com
 [2]: http://www.zohocreator.com