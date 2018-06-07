---
title: 'Guest Article: Selecting or Designing iPhone and Mobile Software for Physicians'
author: Shahid N. Shah
type: post
date: 2009-07-21T21:32:02+00:00
url: /2009/07/21/guest-article-selecting-or-designing-iphone-and-mobile-software-for-physicians/
oc_commit_id:
  - https://www.healthcareguy.com/2009/07/21/guest-article-selecting-or-designing-iphone-and-mobile-software-for-physicians/1478770499
dsq_thread_id:
  - 5174128919
categories:
  - Opinion

---
_I get a lot of questions asking for advice on how to build mobile software and one of the most popular questions is about how and where to save data on a mobile device (because of HIPAA and privacy rules). I reached out to Adam Kenney, a software engineer [pMDsoft][1] who leads a team of developers focused on mobile charge capture. Adam and his team have been building medical apps for mobile platforms and his insights arise from direct experience managing the design, development, and support of native applications for the Palm, BlackBerry, and iPhone. Here&#8217;s what Adam wrote.
  
_ 
  
Any physician who spends time in the hospital setting understands the importance of &#8220;taking it with you&#8221;. Web-only software is great; but even now, when many hospital rooms have a terminal on hand, the overhead of logging in and logging off for each patient can be intolerable for busy physicians who are already spending too much time on administrativia.

This is where mobile software comes in. Doctors were among the first adopters of mobile devices such as Palms. With the rise of smartphones, and with government initiatives such as e-prescribing, mobile software is more appealing than ever. But it&#8217;s challenging to make software that fits the constraints of a mobile platform yet is fast, fun, and friendly to use; and only usability will allow you to save time and achieve 100% adoption within your organization.

One of the biggest factors in the usability of mobile software is how data gets onto and off of the device. Here are a few of the most common approaches that mobile software companies take, with the pros and cons:

**Option 1: &#8220;What happens on the device stays on the device&#8221;**

The simplest applications are native (i.e. installed on the device) and have no way to exchange information with outside systems. In some cases &#8211; such as a drug reference, calorie counter, medical calculator, or a personal to-do list &#8211; this may be all that&#8217;s needed. This type of software is fast to develop and easy to support because there is no shared data, either between users or between the device and a server; so the range of possible scenarios is narrow.

There are some downsides to this approach that make it unsuitable for complex or mission-critical applications. For one thing, there is no ability to exchange information between users, so any situation that requires shared data &#8211; such as an EMR or rounding list &#8211; is beyond the capabilities of a standalone app. Additionally, if the software stores sensitive patient information on the device, it must both encrypt (scramble) that information; and also use a logout mechanism to prevent anyone who picks up the device from seeing it. Finally, if anyone loses or breaks their smartphone, you have no recourse except to hope that there&#8217;s a recent backup. Otherwise, the data is gone.

**Option 2: &#8220;Your information is out there somewhere&#8221;**

Mobile-optimized Web sites and native applications whose data are stored entirely &#8220;in the cloud&#8221; have enjoyed great popularity recently. Mobile Web browsers have become increasingly capable, and we live in the golden age of cloud computing, where software is increasingly being liberated from local environments and stored instead on a third-party hosted server. It&#8217;s an appealing approach: the data is stored and backed up at a centralized facility, so disaster recovery is simplified. You can access it from anywhere, as long as you&#8217;re connected.

That&#8217;s the kicker, though. If an application doesn&#8217;t store any data locally, or stores only a subset of the data it needs, then the user experience is terrible whenever the device doesn&#8217;t have a strong signal. Hospitals have notoriously poor cell phone reception and spotty WiFi coverage. Indeed, we hear horror stories about a duct-taped &#8220;X&#8221; on the floor marking the only spots that can get a signal. This scenario is so common that it&#8217;s crucial to design for it, otherwise the users will have to waste a lot of time searching for a signal just to get their job done.

With growing support for emerging Web technologies such as AJAX and HTML 5, it&#8217;s increasingly possible for Web applications to provide a satisfying offline experience. The line between Web applications and native (installed) applications is blurring. But it&#8217;s still a lot faster to use an application that&#8217;s installed on the device, assuming it&#8217;s well-designed.

For example, iPhone and BlackBerry users can access a webmail site &#8211; sometimes a highly-optimized one such as GMail &#8211; using the Web browser on their phones. But, they&#8217;ll almost always prefer to use the built-in email software instead, because it can combine emails from various personal and work addresses; it allows them to tell when new messages have arrived; it has a user interface that was designed from the ground up for that device; they don&#8217;t need to have network coverage to read and compose emails; and they are never logged out of it. Similar advantages hold true for many kinds of medical software.

Even Web applications that contain sensitive patient information must take certain precautions to ensure that the data is kept safe. Secure sites must use the HTTPS protocol &#8211; the same method of communication used by bank Web sites &#8211; to encrypt data while it&#8217;s being transmitted. When creating Web-based software, it&#8217;s necessary to enforce strong passwords, since an attacker can use any computer to try to gain access to a user&#8217;s account. Finally, even mobile Web sites can end up storing some sensitive data on the device in the form of cached pages. Web browsers automatically store copies of pages that you&#8217;ve visited, to speed up page loading in the future; but unless your site explicitly disables this behavior, or you put a password lock on the entire device, it can be a security risk.

**Option 3: &#8220;Your information is everywhere you are&#8221;**

An application that uses two-way synchronization combines either the best or the worst aspects of the above approaches. It&#8217;s notoriously hard to do sync right &#8211; and when it&#8217;s done wrong, you can end up with data that&#8217;s trapped on the device; frustration and wasted time trying to sync; users who are missing information that they expect and need; or, worst of all, data loss.

But having a fully-functional offline mode is rightly considered the holy grail of mobile user experience. If all of your data is stored on the device, then you can use the software anywhere, whether or not you have a signal. The app will start quickly and respond instantly to your actions, yet your changes are safely uploaded to the cloud as well, where they are out of harm&#8217;s way. And if the synchronization is wireless and happens seamlessly in the background, then updates from other users in the group can appear almost magically during use, and users can stay informed throughout the day.

It all comes down to the quality of the engineering. A well-designed and well-executed application syncs transparently, letting you know when you&#8217;re working offline without interrupting you. And it syncs efficiently, sparing your battery life by avoiding many of the data requests that a Web site needs to operate.

As you might expect, applications that synchronize need to address some of the security and HIPAA concerns of both other approaches. They must use encryption for any sensitive data that they store; must also restrict access on the device using a password; and must use HTTPS or another secure protocol when exchanging potentially sensitive information. At least they don&#8217;t have to worry about browser caching, since the Web browser is not needed to use these apps!

**What&#8217;s right for you?**

Usability &#8211; and specifically, data storage and synchronization &#8211; is just one of many factors to keep in mind when selecting or designing software. It is the most important single factor that distinguishes great mobile software from mediocre mobile software, but your organization may have additional requirements relating to HIPAA compliance, type of device (e.g. BlackBerry versus iPhone), and must-have features.

The important thing is to anticipate what it will really be like to use an application. Will it save time, or impose additional burdens on physicians? Will they love it, or want to throw their smartphones out the window? Taking the time to understand a solution well before you buy it can prevent headaches and remorse down the road.

 [1]: http://www.pmdsoft.com/ChargeCapture/ "pMDsoft mobile charge capture"