---
title: Software vendors should start providing virtual machine images to help demo their wares
author: Shahid N. Shah
type: post
date: 2006-03-02T16:15:26+00:00
url: /2006/03/02/software-vendors-should-start-providing-virtual-machine-images-to-help-demo-their-wares/
oc_commit_id:
  - https://www.healthcareguy.com/2006/03/02/software-vendors-should-start-providing-virtual-machine-images-to-help-demo-their-wares/1478769009
views:
  - 2148
dsq_thread_id:
  - 44283424
categories:
  - Opinion

---
Open source software is often difficult to install and get up running so &#8220;trying it out&#8221; is not trivial. We need web servers, application servers, database servers, etc all working in tandem just to check out some software. On the commercial side things are a little better but still complicated.

My good friend Faisal Qureshi, who&#8217;s in the healthcare IT professional services and consultancy business, left a comment on one of my recent open source articles about how difficult it is to install the open source solutions and suggested that using virtual machine software like VMWare, which is now free for many licensing options, would make it significantly easier for customers to try out software.

A virtual machine (VM) engine is a piece of software (the technology dates back from the mainframe era) that allows multiple logical operating systems (a &#8220;virtual machine&#8221;) to operate on a single physical machine. Assuming you had enough memory and processor power, you could have a Linux or Windows &#8220;host computer&#8221; that would allow multiple Windows 95, 98, NT, XP, Linux, etc &#8220;client virtual machines&#8221; to run as separate windows at the same time. On my workstation I often run several virtual machines at the same time.

I&#8217;ve been advising my clients, most of which develop software for a living, to use virtual machines to help improve quality, test multiple operating systems on a single machine, produce &#8220;snapshots&#8221; of an operating environment to do installations and training, and many other uses. I&#8217;ve written so much about it before that I totally forgot about the use that Faisal mentioned.

Faisal&#8217;s idea is simple but brilliant: software vendors should create a &#8220;virtual machine image&#8221; of a system that has their software, database, network, etc all preinstalled and preconfigured. VMWare has a free version that can take a machine image and launch it on any modern computer. For Windows there would be licensing issues from Microsoft (a vendor can&#8217;t just create a virtual machine client image with Windows without licensing restrictions). However, for any software that runs on Linux that&#8217;s not a problem &#8212; just bundle the operating system fully configured to run your software along with whatever else is needed and give your customer a &#8220;single click&#8221; launch and test capability.

The folks from MedSphere, VISTA, ClearHealth, and other open source groups should take this advice. The virtual machine client model for giving a trial version would change the trial deployment model dramatically and give you leg up on your competition. You could offer a &#8220;5 minute&#8221; install regardless of how complex your software is.