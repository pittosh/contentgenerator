---
title: Phreesia is a great example of consumer driven healthcare technology done right
author: Shahid N. Shah
type: post
date: 2005-12-08T00:28:28+00:00
url: /2005/12/08/phreesia-is-a-great-example-of-consumer-driven-healthcare-technology-done-right/
oc_commit_id:
  - https://www.healthcareguy.com/2005/12/08/phreesia-is-a-great-example-of-consumer-driven-healthcare-technology-done-right/1478768951
views:
  - 3757
ratings_users:
  - 2
ratings_score:
  - 10
ratings_average:
  - 5
dsq_thread_id:
  - 5161220383
categories:
  - Opinion

---
One of my favorite pastimes as a health IT pundit is reviewing new technology before it hits the streets or becomes popular. Last week I had the pleasure of speaking with the founders of [Phreesia][1], a company focused on improving the patient experience in Doctors&#8217; offices waiting rooms. The idea is simple but effective: instead of reading a magazine while they&#8217;re waiting, healthcare cosumers (some people call them patients) are handed a _free_ Phreesia WebPad where they can provide their demographics, chief complaints, and other very basic registration information and based on what they tell the WebPad it will show them web pages and drug information related to their symptoms. Did I mention the device is _free_ for the Physicians? Advertisers (mostly drug companies for now) are paying for the devices and service. Here&#8217;s what the device looks like:

![][2]

You can also [see a demo][3] of their medical history input screens.

What I really liked about the device is that it&#8217;s specially made for the task &#8212; the CTO of the firm, Evan Roberts, walked me through how they tried various form factors like laptops and tablet PCs but through their tests they said they found those kinds of devices too complex for patients to handle. Instead of concentrating just on software they did the right thing by designing the entire system to improve the user experience. They did their own designs and are having it custom manufactured to their specifications. Truly innovative.

I&#8217;ve seen many devices like this come and go but this one might have some legs because it&#8217;s not designed for computerizing the physician&#8217;s work &#8212; instead, it&#8217;s focused on improving the patient&#8217;s experience in the physician&#8217;s waiting room. Chaim Indig, the CEO, indicated in our conversation that Phreesia is totally transparent to the physician because the registration information provided by the patient can just be printed out and provided to the doctor when the patient begins the visit. Chaim said that they wanted to be able to put the Phreesia devices into the doctor&#8217;s offices without affecting anything in their normal workflow but patient flow is improved because the chief complaint is gathered earlier. Evan did mention that all the data entered in to the device is available as XML so it can also be connected to a PPMS if necessary. I asked them about theft and they said their research has not shown theft to be a big issue since people don&#8217;t often steal from their doctors. Of course, that might be true for magazines but a web pad might be different. Their point also was that their device is specialized so nobody would steal it because there&#8217;s no way to fence it (it&#8217;s not a general purpose computer).

I really like their back end design as well. It&#8217;s a pure thin-client approach and the devices are easy to manage for the offices. There is no administration of devices, they are treated almost like cell phones. When one breaks, the Phreesia techs just replace it. The architecture on the server side (Internet or VPN connectivity from a doc&#8217;s office to the Phreesia data center is required) is simple but effective. At this time the Phreesia folks are not doing full data management of clinical or financial data for patients so their design is fine; if they decided to gather more data they&#8217;d just need to beef up the connectivity software and improve the databases. For now, they are more a content provider (based on user preferences) than a transaction provider.

While I like the web pads and the back end architecture is reasonable for the scale they are working on, I do question how fast they can scale their business given the fact that they need patient eyeballs in doctors&#8217; offices for them to make money on the drug detailing side. Having been in a business that sold technology to doctors during the dotcom era for many years, I know how hard it is to get stuff into a doc&#8217;s office even if the devices are free. With that being said, if the word of mouth spreads (via patients or doctors) they may be able to get the devices into the offices. Of course, Pharma companies doing direct to consumer type of drug detailing could also help push the devices but that will almost never happen since the drug sales folks are good at pushing drugs, not technology.

I suggested to them that they might want to create a specific set of screens for other waiting rooms like blood donations. If blood donors at American Red Cross could do their blood donation record (BDR) data entry using this kind of tool it would give the Pharma guys and advertisers even more ways to get their messages to consumers. They were pretty open to new ideas so if you&#8217;ve got some, they&#8217;ll be willing to listen.

If you&#8217;re running a clinic or are a doctor please do yourself a favor and give these guys a call. It won&#8217;t cost you anything to try it out and your patients (customers) may actually come out of your office thinking &#8220;wow, my doc is _cool_.&#8221; Oh, and by the way, the founders are pretty bright and built all of this on their own (no VC money). If you&#8217;re a VC and want to get in on the action you may want to get them while their young.

 [1]: http://www.phreesia.com/
 [2]: /resources/phreesia-device.png
 [3]: http://www.phreesia.net/medhistorydemo/defaultdemo.asp?ID=11723