---
title: 'Guest Article: Standardizing Computer Interfacing to Medical Devices'
author: Shahid N. Shah
type: post
date: 2006-01-09T15:30:27+00:00
url: /2006/01/09/guest-article-standardizing-computer-interfacing-to-medical-devices/
oc_commit_id:
  - https://www.healthcareguy.com/2006/01/09/guest-article-standardizing-computer-interfacing-to-medical-devices/1478768984
views:
  - 5212
ratings_users:
  - 1
ratings_score:
  - 5
ratings_average:
  - 5
dsq_thread_id:
  - 5230057701
categories:
  - Opinion

---
_This is a guest article, written by Nicholas Cain, CEO of [Cain Medical][1]. Cain Medical is the developer of CMSense, a solution for integrating multiple medical devices into legacy or modern health IT applications. I invited Nicholas to share his thoughts about connecting to medical devices because there are more and more specialty medical devices entering our organizations and all those devices generate excellent clinical data that should be captured and managed by our existing applications._

The first medical devices with the means to pass data to a computer appeared in the 1970&#8217;s. Of course in those days there weren&#8217;t many computers to actually connect to the devices, but this rapidly changed with the advent of the PC. However despite the increased availability of computers there was still limited use in connecting a computer to a medical device as there weren&#8217;t many applications to send the data too. It had still become essential for medical devices to provide a means to connect a computer though. If a medical device didn&#8217;t have a computer interface it would appear less sophisticated, and the interface became a required component even though only a minority of researchers wished to use it. Most hospitals today are still using paper charting and record storage rather than using computers.

However, today the computer revolution in hospitals is well and truly under way, and in the last few years a desire to include medical device data in patient records, computer charting, and computer aided diagnosis has arisen. So, after all these years of medical devices having computer interfaces, there is now a real demand (plus the clinical system vendors working quickly to supply the infrastructure to cater for that demand) surely it&#8217;s just a matter of plugging them in and using the data.

However, even though the interfaces have existed for many decades it has not meant that they exist in a mature, usable form. In fact the lack of desire to use them has meant the opposite case. Every medical device computer interface is different – they require different connectors, different cables, and each requires software to be developed to acquire the data. Occasionally the manufacturers supply software (or can provide it on demand), but the software is usually a demonstration on how to develop your own software, and more typically the manufacturer only supplies a document (a protocol) describing the interface. Consequently there exists a vast chasm between what is wanted from medical devices, and what a user can currently achieve.

Almost fifteen years ago there was already awareness of this problem, and work began on a standard to make all devices communicate in a common manner. Initially called the Medical Interface Bus (MIB), it became IEEE 1073 (and now also ISO 11073), and is still an ongoing project. IEEE 1073 is massively comprehensive, but can be broken down into three areas;

  1. Physical connections
  
    Cabling and the plug and socket are defined. Having the same cable for every medical device would simplify the installation and management of devices immensely. IEEE 1073 goes much further than this though, and considers the practicality and safety of connecting to devices. For example utilizing connectors that attach effectively and securely (the serial port connector on your PC has fiddly screws to attach firmly, and without tightening them it doesn&#8217;t take much to knock the cable out), and then defining optical isolation for protecting the patient from electrical risk.
  2. Lower Level Protocol
  
    The commands for the computer to talk to the device are described in the standard. Clearly an application developer doesn&#8217;t want to write new software for every device their application might wish to connect to. Again, the IEEE 1073 goes further than just defining a few commands. The lower level protocol (LLP) defines the ability to detect what device is connected automatically, giving a plug &#8216;n play capability. The LLP then also allows the computer and device to negotiate the fastest speed to communicate.
  3. Upper Level Protocol
  
    Once the computers are talking, IEEE 1073 describes how the medical parameters should be described (the nomenclature). This is essential to a truly comprehensive standard, but is also the most challenging area. However, the IEEE are not the only group trying form a nomenclature standard, and so considerations need to be made towards standards such as LOINC and SNOMED.

So, has a decade been enough time to create a standard? Technically the standard seems complete enough to implement, and probably has been for a long while now. However looking at the device market today it would appear it&#8217;s not ready, as there aren&#8217;t any compliant devices. I&#8217;ve encountered some devices that touch on some of the concepts, such as negotiating communication speeds, and have used some of the medical parameter identifiers from the upper level protocol, but each device still required software writing for each specific device. So what&#8217;s going on?

What are the barriers to medical device manufacturers adopting this standard?

To start with it&#8217;s not clear what version of the standard industry should be using. There&#8217;s no obvious grand approved 1.0 version, only a proliferation of drafts, approval of workgroups and ballots and general confusion. There seems to be a distinct lack of tools or examples to guide through not just the learning process, but also an implementation (if you were to attempt one). This leads easily to the reasons most commonly given by device manufacturers as to why they&#8217;ve not adopted the standard – too complicated and too expensive. It would seem that IEEE 1073 is trying to be too comprehensive, and is creating barriers to early adopters because of it.

So the future looks bleak for IEEE 1073. Other standards such as HL7 and DICOM have flourished due to market forces creating sophisticated products that need to interoperate. IEEE 1073 differs from these by encompassing more than just digital communication, and including hardware recommendations. Maybe if they concentrated on releasing a complete standard just for the upper and lower level protocols (i.e., only the software recommendations), and then encouraged someone to create the tools to help design and develop the medical device firmware, then smaller companies would use the standard. The groundswell support would lead to more innovative products that require device connectivity. The industry would benefit even if the standard wasn&#8217;t taken up in it&#8217;s entire form. There has been a huge amount of effort and thought put into the standard by many experienced people, and all device manufacturers should read the implementation details of the standard to avoid their interfaces falling foul of the common pitfalls.

As an endnote, if you&#8217;ve checked out who I am and what my company does, you might be wondering why I would be keen to see a standardized medical device interface? At this very moment we are in the beginnings of an explosion in healthcare informatics. Clinical systems are now at affordable prices for large scale implementation, standards like HL7, DICOM etc are easily mature enough for companies to rely on them and create highly sophisticated products. I&#8217;m prepared to be part of this wave of innovation, and I&#8217;m looking forward to using our device connectivity expertise and create new and exciting products in the future. I&#8217;m just happy that our current products are going to give us a headstart while everyone else is still waiting for a standard like IEEE 1073 to be truly accepted.

 [1]: http://www.cainmedical.com/