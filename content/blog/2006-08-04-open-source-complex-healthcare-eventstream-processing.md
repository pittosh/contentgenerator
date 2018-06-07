---
title: Open source complex healthcare event/stream processing
author: Shahid N. Shah
type: post
date: 2006-08-04T01:39:22+00:00
url: /2006/08/04/open-source-complex-healthcare-eventstream-processing/
oc_commit_id:
  - https://www.healthcareguy.com/2006/08/04/open-source-complex-healthcare-eventstream-processing/1478769053
views:
  - 2078
dsq_thread_id:
  - 5170303579
categories:
  - Opinion

---
If you need to process business rules or triggers based on large amounts of data that stream in from one or more sources, you probably need a tool like [Esper][1]. I&#8217;ve followed their development for a while and friend of mine just reminded me about its use in healthcare. Here&#8217;s what Esper does (from their website):

> Complex Event Processing, or CEP, is technology to process events and discover complex patterns among multiple streams of event data. ESP stands for Event Stream Processing and deals with the task of processing multiple streams of event data with the goal of identifying the meaningful events within those streams, and deriving meaningful information from them.
  
> The Esper engine has been developed to address the requirements of applications that analyze and react to events. Some typical examples of applications are:
> 
>   * Business process management and automation (process monitoring, BAM, reporting exceptions) 
>   * Finance (algorithmic trading, fraud detection, risk management) 
>   * Network and application monitoring (intrusion detection, SLA monitoring) 
>   * Sensor network applications (RFID reading, scheduling and control of frabrication lines, air traffic) 

Esper could easily be used in applications that read volumes of lab, radiology, EMR, or other data streams. It can act on events that, based on certain rules, automatically trigger alerts. It can also act as a traffic cop for what data should be sent to a database for long-term storage versus an ESB for service processing or just discarded because it&#8217;s not important.

Lots of uses, and it&#8217;s free. Music to my ears.

 [1]: http://esper.codehaus.org/