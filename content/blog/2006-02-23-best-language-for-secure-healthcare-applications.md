---
title: Best language for secure healthcare applications
author: Shahid N. Shah
type: post
date: 2006-02-23T01:18:42+00:00
url: /2006/02/23/best-language-for-secure-healthcare-applications/
oc_commit_id:
  - https://www.healthcareguy.com/2006/02/23/best-language-for-secure-healthcare-applications/1478769006
views:
  - 2041
dsq_thread_id:
  - 5160484129
categories:
  - Opinion

---
I got an email from a reader recently, asking:

> I have a quick question &#8211; I was wondering if there is a programming language that is viewed as &#8216;more secure&#8217; for patient data compared with others? I am building a program to collect patient health info, and am in the very early stages of planning. I used Java previously that worked well for a very sophisticated algorithm to mine data, but this new application is very simple (basically a questionairre) and I have heard .NET would be best. 

Given that the question is quite common based on all the startups I advise and speak with, I thought answering here might be helpful to you.

When it comes to .NET versus Java (or really any language) neither is &#8220;more secure&#8221; than the other with respect to patient data. They are pretty much equal if your engineers are highly qualified and your architecture and design is sound. If you have good software developers, they will almost always create a solid architecture and good design which will make the language selection play a small role in the general quality of your product.

It boils down to what your developers know best and what will make the fewest defects with – for example, if your guys know C# very they will make less errors and therefore fewer security holes. If they know Java better, then of course they&#8217;ll make fewer errors in that language. There is no &#8220;best choice&#8221; for everyone, it&#8217;s really dependent on experience, tools, and platforms.

If you want to run on different platforms and don&#8217;t have very rich UI needs, Java is a good choice. If it only needs to run best on Windows and has rich UI requirements, .NET is a good choice. That&#8217;s a simplistic view but pretty applicable in the general case. Also, give Ruby and Rails a try (see my [earlier article][1] about that).

One mistake that I see people making over and over again is choosing a language first then deciding what to build and going out to hire engineers. What you really should do is to be sure you know what you&#8217;re building, who your customer is, how your application will be used by them, and all the other &#8220;soft&#8221; issues related to the utility of what you&#8217;re creating. Then, get a good software architect to lay out a proper architecture, get some good designs and algorithms in place, and finally choose a language. Once you have done the up front work your choice of lanugage becomes clearer because you really, really want to choose people and architecture first then choose a language. It&#8217;s not easy to find bright architects and engineers who can really build things &#8212; once you have the right folks the language isn&#8217;t as important.

By the way, &#8220;just outsource it to India&#8221; is not the right approach either :-).

 [1]: https://www.healthcareguy.com/index.php/archives/59