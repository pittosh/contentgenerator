---
title: Consider MySQL ‘Archive’ storage engine to store large amounts of med device structured or waveform data
author: Shahid N. Shah
type: post
date: 2011-03-03T16:47:29+00:00
url: /2011/03/03/consider-mysql-archive-storage-engine-to-store-large-amounts-of-med-device-structured-or-waveform-data/
oc_commit_id:
  - https://www.healthcareguy.com/2011/03/03/consider-mysql-archive-storage-engine-to-store-large-amounts-of-med-device-structured-or-waveform-data/1478770721
dsq_thread_id:
  - 5158065464
categories:
  - Uncategorized

---
I&#8217;ve been working on med device integrations for the many years now and one of the most common questions that arises when doing those integrations is &#8220;what&#8217;s the best way to save sensor waveform and analog to digital values?&#8221; Given the complexity of medical devices, there&#8217;s no single or simple answer but one approach that&#8217;s worked well for me in the past is to assume that whatever the data is, when it comes into digital format, it&#8217;s likely structured in some manner. If so, putting it into a database probably makes more sense in many cases than just dropping it into flat files (which is a common and very reasonable approach).

If you want to store your data easily and without much hassle, give (free) open source MySQL a shot. Most of us who have been in the medical device world for even a little while tend to think that SQL is too heavyweight, but MySQL supports various storage engines that have different behaviors and storage goals.

For instance, the standard InnoDB storage engine is an ACID compliant engine that allows full CRUD operations and is actually good when data integrity is crucial. Another storage engine is the &#8216;Archive&#8217; engine &#8212; this is very useful when you want to just insert compressed, structured, data into the database and you want to pull data out at some point through a SQL SELECT clause. Archive engines do not have the ability to update or delete data but that&#8217;s OK for most of our med device data storage needs where we want continuously store and monitor data coming in through the system but won&#8217;t be modifying it.

To learn more about MySQL&#8217;s Archive engine, [check out the documentation on the MySQL site][1]. Here is some relevant detail from that page that might save you some reading time:

> <div id="_mcePaste">
>   <strong>Storage</strong>: Rows are compressed as they are inserted. The ARCHIVE engine uses zlib lossless data compression (see http://www.zlib.net/). There are several types of insertions that are used: An INSERT statement just pushes rows into a compression buffer, and that buffer flushes as necessary. The insertion into the buffer is protected by a lock. A SELECT forces a flush to occur, unless the only insertions that have come in were INSERT DELAYED (those flush as necessary). A bulk insert is visible only after it completes, unless other inserts occur at the same time, in which case it can be seen partially. A SELECT never causes a flush of a bulk insert unless a normal insert occurs while it is loading.
> </div>
> 
> <div>
>
> </div>
> 
> <div>
>
> </div>
> 
> <div id="_mcePaste">
>   <strong>Retrieval</strong>: On retrieval, rows are uncompressed on demand; there is no row cache. A SELECT operation performs a complete table scan: When a SELECT occurs, it finds out how many rows are currently available and reads that number of rows. SELECT is performed as a consistent read. Note that lots of SELECT statements during insertion can deteriorate the compression, unless only bulk or delayed inserts are used. To achieve better compression, you can use OPTIMIZE TABLE or REPAIR TABLE. The number of rows in ARCHIVE tables reported by SHOW TABLE STATUS is always accurate.
> </div>

 [1]: http://dev.mysql.com/doc/refman/5.1/en/archive-storage-engine.html