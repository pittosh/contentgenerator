---
title: Single sign on (SSO) solutions in healthcare
author: Shahid N. Shah
type: post
date: 2007-01-14T18:13:17+00:00
url: /2007/01/14/single-sign-on-sso-solutions-in-healthcare/
oc_commit_id:
  - https://www.healthcareguy.com/2007/01/14/single-sign-on-sso-solutions-in-healthcare/1478769092
views:
  - 2850
ratings_users:
  - 2
ratings_score:
  - 8
ratings_average:
  - 4
dsq_thread_id:
  - 5194020662
categories:
  - Opinion

---
Based on my recent discussions with numerous CIOs, they each mention that SSO is something that&#8217;s on their radar screens as an important or high priority requirement. Given that most users deal with multiple IT systems during the day and they&#8217;re getting tired of re-authenticating themselves for each system, it&#8217;s understandable.

While the commercial vendors already tout their own (pretty good in some cases) solutions I thought I&#8217;d bring some of you up to speed on one open source solution that you may not be aware of: the [Central Authentication System][1] (CAS). CAS is an authentication system originally created by Yale University that allows applications written in Java, .Net, PHP, Perl (and other languages) to authenticate a user against a central directory or multiple directories.

An important feature of CAS is that it&#8217;s an open protocol with a solid set of implementations in multiple languages. This means that you can write your own implementation and continue to use the CAS protocol/standard across your various products. And, since it&#8217;s open source, you can have your vendors use it without buying per user or application licenses. It&#8217;s already in [active use][2] in decent size campuses so you don&#8217;t have to worry about being an early adopter.

Have your folks check out CAS, it&#8217;s something I&#8217;ve analyzed personally and it&#8217;s a great option for many organizations looking for a reduced or sign sign on solution.

 [1]: http://www.ja-sig.org/products/cas/
 [2]: http://www.ja-sig.org/products/cas/community/deployers/index.html