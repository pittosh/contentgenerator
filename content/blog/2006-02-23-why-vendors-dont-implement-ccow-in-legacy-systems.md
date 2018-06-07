---
title: Why vendors don’t implement CCOW in legacy systems
author: Shahid N. Shah
type: post
date: 2006-02-23T14:07:38+00:00
url: /2006/02/23/why-vendors-dont-implement-ccow-in-legacy-systems/
oc_commit_id:
  - https://www.healthcareguy.com/2006/02/23/why-vendors-dont-implement-ccow-in-legacy-systems/1478769007
views:
  - 5670
dsq_thread_id:
  - 5157887912
categories:
  - Opinion

---
Wheelybop, A HIStalk reader, [recently posed a question][1]:

> Can you or your blogger network describe to me what vendors have to do to make their legacy products CCOW compliant and why some refuse to do so, what are pros/cons, etc. Would love a CCOW primer or be pointed to such. 

First, lets tackle the primer. The acronym CCOW stands for &#8220;Clinical Context Object Workgroup&#8221;, a reference to the standards committee within the HL7 group that developed the standard. CCOW is a standard designed to allow information sharing between clinical and health IT applications. It uses a basic technique called &#8220;context sharing&#8221; that allows multiple clinical applications to &#8220;switch contexts&#8221; simultaneously. A &#8220;context&#8221; is a computer science term that could mean a patient&#8217;s data screen or an encounter form. Multiple CCOW compliant applications can simultaneously change their screens to see the same patient&#8217;s data when any of the other participating applications do so. For example, if a hospital can get their labs, EMR, and CPOE vendors to become CCOW compliant they can share to share patient context instead of the user having to log in and out of each application separately.

Ok, that&#8217;s the intro. There&#8217;s more at CCOW vendor (like NeoTool, [Sentillion][2], etc) websites you can read but the above is pretty much what you&#8217;ll get there as well.

Now, to answer the reader&#8217;s original question: why don&#8217;t legacy vendors support it? The simple answer is that CCOW provides no real value to _them_. Legacy vendors rarely benefit from migrating and supporting new standards, regardless of what it is. CCOW is good for new entrants into the health IT field &#8212; for example, if I&#8217;m a startup and I write a new app I would definitely want to be CCOW compliant because CIOs won&#8217;t like me unless I&#8217;m interoperable with their legacy systems. However, legacy vendors have neither the inclination nor the customer outcry necessary to become interoperable with new software. They are already in the customer&#8217;s shop and don&#8217;t need to support the new standard to make more sales. The larger you are, the more entreanched you are in your customers&#8217; shops, the less you need to &#8220;play nice&#8221; with other vendors.

Of course, there are many benefits to becoming CCOW compliant. However, none of those benefits apply to the vendor itslef. The benefits are all for the user and for the IT shop that can help users streamline their work.

So, don&#8217;t expect CCOW compliance from the legacy vendors anytime soon. 🙂

 [1]: http://histalk.blog-city.com/monday_morning_update_022006.htm
 [2]: http://www.sentillion.com/solutions/product.html