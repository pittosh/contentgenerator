---
title: How to manage HIPAA security in a way that actually enhances security and not just fills in documentation
author: Shahid N. Shah
type: post
date: 2011-09-18T20:59:20+00:00
url: /2011/09/18/how-to-manage-hipaa-security-in-a-way-that-actually-enhances-security-and-not-just-fills-in-documentation/
oc_commit_id:
  - https://www.healthcareguy.com/2011/09/18/how-to-manage-hipaa-security-in-a-way-that-actually-enhances-security-and-not-just-fills-in-documentation/1478770766
dsq_thread_id:
  - 5159656377
categories:
  - Uncategorized

---
I get lots of questions about HIPAA security these days; especially as EHR firms, hospitals, payers, and startups alike are being asked about their HIPAA policies.

My general recommendation is that **you should forget about HIPAA at first** (it&#8217;s a toothless, generally unenforceable, regulation that will never improve security because it is a bureaucratic compliance tool). Instead, you should concentrate on good security practices, good security policies, follow recommended NIST guidance, and then come back and tie in the HIPAA regulations to make sure you don&#8217;t miss anything from the privacy side.

Also, don&#8217;t worry about finding &#8220;HIPAA auditors&#8221; initially &#8212; instead, focus on finding white hat hackers that can help you with penetration testing and hack attempts to truly focus on your threats and not on perceived HIPAA threats. Once you get beyond HIPAA as a security goal you&#8217;ll end up with much better security and then you can tie HIPAA into your privacy policies to make sure you&#8217;re not missing any major regulations.

Here&#8217;s how to proceed:

  1. Get a security policy in place &#8212; start with <http://www.informationshield.com/> or [http://www.instantsecuritypolicy.com][1]. Both of these sites help you think about all the really difficult questions and options you have and help you construct a single document that would come out better than you can do on your own (initially). You can generate a pretty decent document within about 30 to 40 hours of work.
  2. As you&#8217;re getting your security documentation in place, take a look at the [NIST 800-53 Information Security Policies for Federal Agencies][2] guidance document. Why a federal agency guidance document? Because it&#8217;s thorough; most of it will be applicable to healthcare and is worth reviewing to make sure you don&#8217;t miss anything when you&#8217;re laying out your security policies and controls. Another reason to know about it is that there are lots of consultants out there that know NIST 800-53 and can help you out. Set aside about 8 to 12 hours to really get a good overview of this guidance document.
  3. Just to complete your understanding of the NIST security guidance, check out the [other NIST special publications][2].
  4. Armed with a starter document from step #1 and a basic understanding of the NIST guidance, contact guys who are not HIPAA guys but are security policy experts (contact me privately and I can put you in touch with some) that can review your document. In less than 8 hours of work you can have the document improved in ways that you never imagined (assuming you&#8217;re talking to a _security expert_, _<span style="text-decoration: underline;">not</span> a compliance person_).
  5. With a proper policy document now in place, get in touch with a security company that can help you with penetration testing and evaluating your policies _in excruciating detail_. HIPAA auditors are not what I mean here; I mean guys that can try to break into your system and tell you whether the policies will work and what holes you need to fill in &#8212; the &#8220;white hat&#8221; crowd. This might take as little as 20 to 30 hours or hundreds of hours, depending on the state of your security policies and actual security tools in place.
  6. Go back to the tools in step #1 and plug in all your real security holes with either policies or security tools recommended by the testing firm(s) and consultant(s) and iterate over your document.
  7. With a near-final security document in place, schedule a quarterly test and evaluation and a change control process for how you will keep your documents, real security tools, and policies in good shape. You will need to review your own logs daily, weekly, and monthly and have the experts come in no later than quarterly (monthly is even better). To see one approach to how the feds recommend doing this (again, it&#8217;s completely applicable to healthcare) [check out the FedRAMP program][3].
  8. With your documentation now ready and a good change control process in place, now you&#8217;re (finally!) ready for the HIPAA auditors; they can now concentrate on the compliance activities and you won&#8217;t be fooled into thinking that HIPAA compliance means you&#8217;re more secure.

If you&#8217;ve got other thoughts that can help the health IT community, drop us some comments here.

 [1]: http://www.instantsecuritypolicy.com/
 [2]: http://csrc.nist.gov/publications/nistpubs/800-53-Rev3/sp800-53-rev3-final_updated-errata_05-01-2010.pdf
 [3]: http://www.cio.gov/pages.cfm/page/Federal-Risk-and-Authorization-Management-Program-FedRAMP