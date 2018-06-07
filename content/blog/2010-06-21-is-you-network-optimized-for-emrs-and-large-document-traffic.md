---
title: 'Guest Article: Is your network optimized for EMRs and large document traffic?'
author: Shahid N. Shah
type: post
date: 2010-06-21T13:54:32+00:00
url: /2010/06/21/is-you-network-optimized-for-emrs-and-large-document-traffic/
oc_commit_id:
  - https://www.healthcareguy.com/2010/06/21/is-you-network-optimized-for-emrs-and-large-document-traffic/1478770589
dsq_thread_id:
  - 5161849150
categories:
  - Uncategorized

---
_In the rush to install EMRs tech folks often forget that you need to make sure that your network can handle the (usually significant) load that medical records automation will add to your network infrastructure. I invited Jon Mills of of [Plixer International][1], Inc., a Maine-based software development company that specializes in network traffic analysis using NetFlow and other flow-based monitoring technologies to talk about network optimization.  Here&#8217;s what Jon had to say about optimizing network traffic for EMRs:_

As more and more healthcare facilities leave behind the decidedly un-green data storage methods of forms and files for a more 21<sup>st</sup> century approach, the importance of monitoring and managing that data flow has grown exponentially. Although the adoption rate of such paperless EHR (Electronic Health Record) systems has not exactly been staggering, the American Recovery and Reinvestment Act (ARRA) of 2009 may be enticing an ever growing number of healthcare organizations into taking advantage of this economic stimulus for the Healthcare IT industry.

In a facility like a hospital, many wired and wireless devices pass secure and often time-sensitive information. Traffic monitoring solutions are a necessity for keeping the congestion levels and bottlenecks to a minimum. If the staff can’t get the information they need immediately, it could be the patient who suffers.

Using flow-based technologies make it easier to implement traffic monitoring solutions. Cisco Systems’ [NetFlow][2] takes the important information about any given data exchange on the network and delivers the pertinent information about that conversation—which hosts participated in the conversation, how much data was passed, how long the conversation lasted, etc. Several other hardware vendors have introduced NetFlow or a variation of it into their switches, routers and, most recently, firewalls.

Using flow technologies to monitor the health of the network and watch for issues like congestion, bottlenecks, misuse and incorrectly configured hardware and software applications is much easier and more cost-effective than relying on more labor intensive packet analysis. While providing much of the same information, flow devices are typically already found on the network in the form of Cisco hardware, or some other supporting vendor.

Any Electronic Medical Record (EMR) system will certainly demand a good deal of bandwidth to stay at an acceptable level of speed and accuracy. Maintaining that level of available bandwidth starts with knowing how much bandwidth the organization has available to it and where that bandwidth is being dispersed. Just ask Stan DeFreese of [Mercy Hospital][3], who uses a NetFlow analysis solution to receive and display his NetFlow data. “The solution sees disparate applications, top talkers and how much bandwidth each one is using—all from a much more detailed application/packet level perspective. It answers questions like ‘Which device is taking up bandwidth and utilization of application servers?’ Basically, it gives us a level of control and analysis that we’ve never had before.”

There will undoubtedly be times when extra details are required to solve a network issue. But once the high level pictures have been taken by the flow-based systems, a packet analyzer can go even deeper to get to the heart of the problem. Even in these situations, a NetFlow or sFlow application can help narrow in on the problem that much quicker.

Having a patient’s medical records at your fingertips in microseconds could realistically mean the difference between life and death. In a society based on instant gratification, these resources must be made available at little to no cost in effectiveness from past methods. Network latency and stability of course play into this. The healthcare IT organization that invests heavily (using government stimulus funds or not) in making the transition to paperless systems—without protecting the investment with some form of traffic monitoring system—is setting itself up for failure at the expense of its patients. Networks need health insurance, just like the rest of us.

 [1]: http://www.plixer.com/
 [2]: http://en.wikipedia.org/wiki/Netflow
 [3]: http://www.mercyhospital.org/content/Default.htm