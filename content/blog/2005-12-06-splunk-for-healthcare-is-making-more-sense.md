---
title: Splunk for Healthcare is making more sense
author: Shahid N. Shah
type: post
date: 2005-12-06T20:43:10+00:00
url: /2005/12/06/splunk-for-healthcare-is-making-more-sense/
oc_commit_id:
  - https://www.healthcareguy.com/2005/12/06/splunk-for-healthcare-is-making-more-sense/1478768950
views:
  - 739
dsq_thread_id:
  - 44283232
categories:
  - Opinion

---
A little while ago I wrote about using [Splunk][1], a nice IT systems log aggregator and search engine, in the healthcare sector. I just spoke with the product manager in charge of the tool at Splunk and I liked what I heard even more: they have a solid design, good APIs, and an open approach to accepting almost any kind of ASCII data and creating a searchable index and relationships between data. I spoke to them about how they might be able to support ASC X.12, HL7, and other healthcare data formats and it seems like it&#8217;s not only possible, but fairly straightforward.

I was thinking about a system for hospitals or other large healthcare institutions that would be able to act as a data sink for all data: financial, administrative, clinical, medical device, PACS, etc. All those data streams could be tagged, tokenized, and stored in the Splunk server. Then, we&#8217;d be able to do searches like &#8220;show me all data dealing with Physician X&#8221; and the system could do a full text Google-style search on the Splunk data and pull back information in one view with time and system information about where it was created.

A master person/patient index would even be pretty easy to setup if we could do a bit of de-duplication of data on the way in. I think the biggest benefit of something like this would be to use it as a data crawler and pull together everything in one place so that we could do forensics on who saw what & when, get all related documents dealing with a legal case, or use it for aggregating patient data in one place.

The piece that I&#8217;m still thinking about is how the data storage (which is plain text) would affect privacy and security but I think that could be worked out if we could come up with some good use cases.

Anybody interested in working with me to give this a shot at their premises? Comment or [contact me anonymously][2]. Let me know if this is a crazy idea or something worth considering.

 [1]: http://www.splunk.com
 [2]: mailto:shahid@shah.org?subject=Your Splunk idea is interesting