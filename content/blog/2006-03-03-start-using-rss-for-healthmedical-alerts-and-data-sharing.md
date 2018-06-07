---
title: Start using RSS for health/medical alerts and data sharing
author: Shahid N. Shah
type: post
date: 2006-03-03T14:44:23+00:00
url: /2006/03/03/start-using-rss-for-healthmedical-alerts-and-data-sharing/
oc_commit_id:
  - https://www.healthcareguy.com/2006/03/03/start-using-rss-for-healthmedical-alerts-and-data-sharing/1478769010
views:
  - 2357
dsq_thread_id:
  - 44283426
categories:
  - Opinion

---
As most of us bloggers already know, Really Simple Syndication (RSS), is pretty popular in the blogosphere. It&#8217;s a wonderful solution to the &#8220;how do I tell everyone I have new stuff without sending out a bunch of emails?&#8221; problem. Although it&#8217;s quite popular for syndicating content like news, blog articles, and related information I think RSS has a chance to make a huge impact on healthcare and medical data sharing.

Today medical devices send out alerts using one or more mechanims in a &#8220;push based&#8221; approach. For example, the device manufacturer has to write software to send alerts via e-mail, pager, phone, etc whenever some programmed action occurs in their device. In the healthcare IT world data sharing occurs through HL7 in a hub-and-spoke or publish/scribe model where all information is published to a broker and that broker is queried for things like new lab results, updated patient information, etc.

Well, what if all medical devices had the ability to respond to RSS requests on various channels? For critical messages the push method would be fine but for other kinds of messages we could have a channel which an IT system could poll every second, minute, or over many hours depending upon how often the system wanted an update from a device. Instead of all the devices always sending out all messages, why not put in some simple code to respond to RSS requests and separate the different message types into RSS channels? This way, the &#8220;pull based&#8221; approach allows the device to be more responsive to each client instead of having to use a broker model to send out all messages.

What if health IT systems from Cerner, Misys, McKesson, etc also had this capability? Suppose I wanted to use my mobile device (which will all have RSS feed readers installed) to be able to check on labs for a particular group of patients? I could simply subscribe to a specific channel in a Lab Management System&#8217;s RSS feed and get what I need without having to go through a broker. If I&#8217;m a doctor and I have a finite number of patients, I can simply subscribe to an RSS feed of my patient&#8217;s data in all the various IT systems and pull together my own aggreator.

Think about RHIOs and how they could use RSS to subscribe to information across multiple health IT systems.

I think with a little creativity, building in RSS publishers inside our medical devices and health IT systems like EMRs and HIS would go a long way towards helping create more interoperable systems. Of course, content and messaging standards like HL7 would not be replaced but would become the de facto standard of the payloads in the messages that RSS feeds could publish.

What do you think? Ready to start a company based on this idea? I&#8217;m game 🙂