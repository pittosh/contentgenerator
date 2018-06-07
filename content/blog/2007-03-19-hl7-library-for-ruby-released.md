---
title: HL7 library for Ruby Released
author: Shahid N. Shah
type: post
date: 2007-03-19T20:39:44+00:00
url: /2007/03/19/hl7-library-for-ruby-released/
oc_commit_id:
  - https://www.healthcareguy.com/2007/03/19/hl7-library-for-ruby-released/1478769120
views:
  - 3355
dsq_thread_id:
  - 5162895308
categories:
  - Opinion

---
Mark Guzman over at [Tech Addict][1] just announced the 0.1.23 release of an HL7 parser for Ruby. I&#8217;ve been doing a bunch of [Rails][2] stuff lately and this should come in handy when I need HL7 parsing. I haven&#8217;t tried it out yet, but here&#8217;s what Mark said is in there:

  * Flexible parsing support
  * MLLP support
  * Provides a simple DSL (domain specific language) for defining segments (Ruby style)
  * Allows for arbitrary manipulation of segment data
  * Automatic segment ordering (via sort)
  * Familiar Ruby Array/Enumerable semantics

How to get it: 

> gem install ruby-hl7

or grab the tarball from <http://rubyforge.org/frs/?group_id=3261> 

More details are&nbsp;available here: 

  * <http://hasno.info/2007/3/18/ruby-hl7-0-1-23-released>
  * <http://trac.hasno.info/ruby-hl7>
  * <http://ruby-hl7.rubyforge.org>

 [1]: http://hasno.info/2007/3/18/ruby-hl7-0-1-23-released
 [2]: http://www.rubyonrails.org