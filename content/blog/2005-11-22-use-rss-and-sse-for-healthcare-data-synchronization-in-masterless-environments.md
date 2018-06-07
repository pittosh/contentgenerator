---
title: Use RSS and SSE for healthcare data synchronization in masterless environments?
author: Shahid N. Shah
type: post
date: 2005-11-22T15:16:43+00:00
url: /2005/11/22/use-rss-and-sse-for-healthcare-data-synchronization-in-masterless-environments/
oc_commit_id:
  - https://www.healthcareguy.com/2005/11/22/use-rss-and-sse-for-healthcare-data-synchronization-in-masterless-environments/1478768930
views:
  - 1423
dsq_thread_id:
  - 44283165
categories:
  - Opinion

---
[RSS][1] is a means to syndicate content unidirectionally &#8212; for example, when I create a new article here and you subscribe to my feed you will get news about my new publication in your feedreader. Microsoft&#8217;s Ray Ozzie (inventor of Lotus Notes and Groove) announced that Microsoft has extended the standard with [SSE][2], which is a â€œspecification that extends RSS from unidirectional to bidirectional information flows.â€? Some elaboration on the technology comes from Ray:

> For example, SSE could be used to share your work calendar with your spouse. If your calendar were published to an SSE feed, changes to your work calendar could be replicated to your spouseâ€™s calendar, and vice versa. As a result, your spouse could see your work schedule and add new appointments, such as a parent-teacher meeting at the school, or a doctorâ€™s appointment.
> 
> SSE allows you to replicate any set of independent items (for example, calendar entries, lists of contacts, list of favorites, blogrolls) using simple RSS semantics. If you can publish your data as an RSS feed, the simple addition of SSE will allow you to replicate your data to any other application that implements the SSE specification.
> 
> SSE can also be used to extend other formats such as OPML. 

After thinking somewhat about the technology (which is described by [a draft specification][3] and elaborated on by [an FAQ][4]) I think it can easily be applied to the medical record and biomedical information synchronization problem inherent in healthcare IT. What we&#8217;ve needed is a really simple and ubiquitous synchronization protocol and while SSE still has to prove itself, I think it may work. The problem is that it won&#8217;t be transparent in legacy applications (the applications would need to know about SSE to utilize it) but all healthcare IT application managers should look at SSE and see how it might be applicable to their environments.

Lets see how it might work: assume that the scheduling application you bought has been upgraded to use SSE. Then, whenever anything &#8220;new&#8221; happened (an appointment was added, an appointment was cancelled, etc) anyone subscribing to the SSE feed would be notified and update their own information based on what&#8217;s new (and send back their affected changes). Assume that a medical record in the labs department was updated &#8212; a synchronization message could be sent using the protocol and the medical record in another department could be updated, and if anything required change propogation then the message would respond with its changes.

Now, in real life things are _much more difficult_ than I&#8217;ve alluded to here but we&#8217;ve got to start somewhere. What if SSE could be used to carry payloads (attachments) of HL7 and X12 data? Then we could have the best of both worlds: RSS, XML, SSE for synchronization publish/subscribe and broadcasting while the messages themselves stay similar to what they are today. We still have to work out the sematics and homogenization problems but that&#8217;s a different story.

If RSS, XML, and SSE can be used together they would form a potent combination of the basic protocols necessary for synchronizing data (with some semantic meaning) across medical and clinical systems without every system having to use a centralized database (a holy grail no less).

It&#8217;s time to put your thinking caps on and talk to your vendors to see how they can help some of these modern, but very very simple, protocols to help alleviate some of the medical information sharing burdens that are shouldered by the healthcare IT community.

Oh, by the way, SSE is open source. It&#8217;s published under the Creative Commons license.

There&#8217;s a related [_SSE won&#8217;t work_][5] column over at Daily Buzz. I don&#8217;t agree with him completely, but he&#8217;s got some good points. What I don&#8217;t agree with is that all the problems he cites has to be taken care of in the spec &#8212; it&#8217;s possible to get started and use it for simple synchronizations and replace proprietary means. Then, as the spec grows it will become more useful for general sync.

 [1]: http://en.wikipedia.org/wiki/RSS_(protocol)
 [2]: http://spaces.msn.com/members/rayozzie/Blog/cns!1pyct_cYtbBtOBPDVAumMEdw!175.entry
 [3]: http://msdn.microsoft.com/xml/rss/sse
 [4]: http://msdn.microsoft.com/xml/rss/ssefaq/
 [5]: http://www.subcoded.com/2005/11/22/why-sse-wont-work/