---
title: Regulatory compliance officers need not fear open source software in medical devices or mission-critical healthcare IT systems
author: Shahid N. Shah
type: post
date: 2011-09-12T00:37:48+00:00
url: /2011/09/11/regulatory-compliance-officers-need-not-fear-open-source-software-in-medical-devices-or-mission-critical-healthcare-it-systems/
oc_commit_id:
  - https://www.healthcareguy.com/2011/09/11/regulatory-compliance-officers-need-not-fear-open-source-software-in-medical-devices-or-mission-critical-healthcare-it-systems/1478770764
dsq_thread_id:
  - 5163148648
categories:
  - Engineering
  - Medical Devices
  - Open Source

---
I spent the past few days in Boston at the Harvard Medical School Conference Center speaking audiences at the Medical Device Connectivity Conference (I presented lectures on how to design next-generation medical devices and gateways). Many people that attended my lectures showed a great deal of trepidation when I brought up the fact that they should use open source software (OSS) to reduce cost and potentially increase the quality of their devices; the most common excuse I heard was that the regulatory compliance folks wouldn’t allow OSS or that the FDA would disapprove.

Having taken part in numerous regulated medical device development efforts that included open source software, including the world’s largest medical devices with a 510(k), I know for a fact that the FDA doesn’t have anything against open source software in particular (as long as you can prove safety). So, the problem in most cases likely stems from a lack of experience with open source in the regulatory compliance groups within companies. I thought I’d take this opportunity to write up a quick summary of how R&D groups should properly experiment with and include open source software in safety-critical systems.

**Step 1: Understand open source licensing, remove the fear of IP loss**

Fear starts from a the lack of understanding that open source licenses allow for inclusion in your device(s) without harming intellectual property (IP) rights or proprietary claims. There’s no need to fear that somehow if you include open source you’ll accidentally relinquish proprietary IP. If you’re not sure which licenses to use, start with the Apache Software License (ASL), Mozilla Public License (MPL) or LGPL, all of which are friendly enough to use in commercial software.

**Step 2: Understand where code is coming from and what test harnesses included**

To help remove fear from your regulatory groups, keep track of precisely where you’re getting the OSS code from. Also, try and focus on incorporating OSS that already contains good test harnesses so you can prove to yourself, your QA teams, and your regulatory teams that the software works for its intended uses.

**Step 3: Get in touch with the open source developers**

If you’re going to rely on some OSS, get in touch with the developers. Most OSS developers are quite community oriented and usually helpful; in case your regulatory or QA folks have questions you’ll be able to answer them easily if you’re in touch with the original developers. Also, if you need changes, some developers will likely be available for hire for making changes or helping with validation.

**Step 4: Connect to the revision control system of the open source project**

My general recommendation is that you not download binaries for OSS projects; instead, connect directly to the Subversion, Git, CVS, Mercurial, or other revision control system (RCS) the OSS project developers are using. You should get used to various RCS systems and not just the one you’re using in your own shop. It’s much easier to know precisely what lines of code, modules, etc. are changing when you’re directly connected to the RCS.

**Step 5: Create your own binaries**

As soon as you’re connected to the revision control system of the OSS project, build your own binaries using the existing make or build scripts. If there are no make or build scripts you should not use the OSS (if you have other choices) or you can create your own.

**Step 6: Create a process to securely sign the binaries**

When you create your own binaries you’ll want to make sure you digitally sign the binaries and ensure that your devices / gateways have firmware or other software that verifies the binaries.

**Step 7: Create your own deployment packages** 

If you’re running on Windows you’ll want to create \*.msi packages; on RedHat create RPMs, on Debian / Ubuntu create \*.deb packages, etc. You will want to have a proper package management approach that your QA and regulatory folks can have confidence in and easily understand.

**Step 8: Create a process to test the binaries using code coverage tools**

This step could be done before or after step 6 but you’ll want to be sure you run the test harnesses with code coverage turned on; that way, you’ll know what test coverage you can achieve in the various OSS packages you’ll build. Try not to go to your regulatory folks and say “we can trust OSS package X” without some sort of real evidence – test harnesses and code coverage tools are good starts.

**Step 9: Keep an eye on changes coming in from the source and retest regularly**

Figure out how you’ll ensure that packages stay up to date and will be regularly tested (with code coverage); you might want to read an RSS feed, get regular e-mail notifications from forums, etc. Each time the code changes you probably don’t want to upgrade immediately but you’ll want to stay abreast of the updates.

**Step 10: Review your process with the compliance officers and get their buy in**

Share with your QA and regulatory folks your process early and often &#8212; they’ll have more confidence in your process when the process is documented, scripted, and easy to understand and follow.

**Conclusion**

If you do things “properly” and follow a good solid process then the compliance officers can (hopefully) be convinced that the code can be trusted. If you’re getting push back, put your questions here and I’ll help out as best I can. The more proprietary software we create in medical devices, the less interoperable they will be so it’s time we get our regulatory folks on board.

Comments welcome below … what kinds of questions do you get from your compliance folks?