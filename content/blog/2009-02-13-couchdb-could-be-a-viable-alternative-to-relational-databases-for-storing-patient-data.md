---
title: CouchDB could be a viable alternative to relational databases for storing patient data
author: Shahid N. Shah
type: post
date: 2009-02-13T11:50:24+00:00
url: /2009/02/13/couchdb-could-be-a-viable-alternative-to-relational-databases-for-storing-patient-data/
oc_commit_id:
  - https://www.healthcareguy.com/2009/02/13/couchdb-could-be-a-viable-alternative-to-relational-databases-for-storing-patient-data/1478770438
ratings_users:
  - 2
ratings_score:
  - 9
ratings_average:
  - 4.5
dsq_thread_id:
  - 5190941300
categories:
  - Opinion

---
A while back I wrote the [Data Models in Healthcare][1] series of articles. Beyond relational databases, which is of course my primary storage platform, one of my favorite techniques for managing the structured and semi-structure databases is to use XML. XML is a great persistence model for storage of schema-free data (and sometimes schema-fixed data).

However, XML is not a natural model to do aggregation, consolidation, and analytics from various data sources (which is sometimes a pretty big requirement in modern health IT apps) so it’s something to be avoided in certain circumstances. There are also some modern XML native databases (both open source and commercial) that support querying and aggregation but they are neither popular nor ubiquitous which means tooling support is limited. XML native databases have not really taken off but many existing databases (like Oracle, DB2, and others) are supporting schema-free XML artifacts in their databases. Until now either you went with MUMPs for a flexible database or you went to XML stored in a relational schema.

Until now.

I’ve been playing with Apache’s <a href="http://couchdb.apache.org/" target="_blank">CouchDB</a> for some time now; while I’m not drinking the kool-aid just yet, I find it a worthy platform for researching whether it can play a major role in modern and flexible healthcare data platforms. This is how the CouchDB principals describe their database:

> Apache CouchDB is a distributed, fault-tolerant and schema-free document-oriented database accessible via a RESTful HTTP/JSON API. Among other features, it provides robust, incremental replication with bi-directional conflict detection and resolution, and is queryable and indexable using a table-oriented view engine with JavaScript acting as the default view definition language.
> 
> CouchDB is written in [Erlang][2], but can be easily accessed from any environment that provides means to make HTTP requests. There are a multitude of third-party client libraries that make this even easier for a variety of programming languages and environments.

I love the fact that it’s written in Erlang (since it was created for concurrent programming) but what I like even more is that it’s native application programming interface (API) is HTTP and REST. This is a modern and refreshing design and is modeled after something that is hugely successful: the web. 

I have a basic patient management system up and running in CouchDB and I plan on open sourcing it to let others play with it as well. I really like schema-free nature of the CouchDB because almost all systems start by wanting to store certain parts of patient data only to grow other data collection requirements like weeds. CouchDB doesn’t need constant adjustment. Also, I like that it’s document-centric because most patient record systems require documents to be stored natively (and later edited directly). CouchDB gets around some of the limitations I’ve seen with XML databases while still storing XML as documents. 

So, is CouchDB ready for prime-time in an important field like healthcare? Not quite, but within a year I see it can be taking over many responsibilities that we need for flexible data storage in our applications. So, it’s a good time to look at it and maybe even participate in its evolution so that those of us who need some additional functionality for fault-tolerant applications can get it baked into the design.

If you’re interested in other modern mega-scale databases check out <a href="http://www.allthingsdistributed.com/2007/10/amazons_dynamo.html" target="_blank">Dynamo</a>, <a href="http://labs.google.com/papers/bigtable.html" target="_blank">BigTable</a>, [Cassandra][3], BerkeleyDB (BDB), Voldemort, and [dynomite][4]. 

Check CouchDB out and let me know what you guys think about using it or any others of these kinds of modern non-relational databases to handle healthcare data.

 [1]: http://www.health-itworld.com/newsitems/2006/march/03-22-06-news-hitw-dynamic-data
 [2]: http://erlang.org/
 [3]: http://code.google.com/p/the-cassandra-project/
 [4]: http://github.com/cliffmoon/dynomite/tree/master