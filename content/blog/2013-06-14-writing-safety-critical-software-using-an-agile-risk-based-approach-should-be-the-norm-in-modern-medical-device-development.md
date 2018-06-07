---
title: Writing safety critical software using an agile, risk-based, approach should be the norm in modern medical device development
author: Shahid N. Shah
type: post
date: 2013-06-15T02:55:51+00:00
url: /2013/06/14/writing-safety-critical-software-using-an-agile-risk-based-approach-should-be-the-norm-in-modern-medical-device-development/
oc_commit_id:
  - https://www.healthcareguy.com/2013/06/14/writing-safety-critical-software-using-an-agile-risk-based-approach-should-be-the-norm-in-modern-medical-device-development/1478770835
  - https://www.healthcareguy.com/2013/06/14/writing-safety-critical-software-using-an-agile-risk-based-approach-should-be-the-norm-in-modern-medical-device-development/1425378479
dsq_thread_id:
  - 5160712885
oc_metadata:
  - |
    {		version:'1.1',		tags: {'mhealth': {"text":"MHealth","slug":"mhealth","source":{"url":"http://d.opencalais.com/dochash-1/ffcc4a1e-014b-32cf-b622-33730a462300/SocialTag/12","subjectURL":null,"type":{"url":"http://s.opencalais.com/1/type/tag/SocialTag","name":"SocialTag","_className":"ArtifactType"},"name":"MHealth","makeMeATag":true,"importance":1,"_className":"SocialTag","normalizedRelevance":1},"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'healthcare-technology': {"text":"healthcare technology","slug":"healthcare-technology","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'medtech': {"text":"medtech","slug":"medtech","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'risk-management': {"text":"risk management","slug":"risk-management","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'medical-softwares': {"text":"medical softwares","slug":"medical-softwares","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}}	}
categories:
  - Engineering
  - FDA
  - Medical Devices
  - Telehealth
  - Telemedicine
tags:
  - Healthcare Technology
  - medical softwares
  - Medtech
  - MHealth
  - risk management

---
I first started using and mentoring developers on agile software development techniques like eXtreme Programming (XP) and Scrum over a decade ago. Often called “lightweight” methodologies, agile software development lifecycles have been generally misunderstood as lacking enough rigor and sophistication to be used in safety-critical systems. Many have erroneously assumed that Agile, Scrum, and related methodologies can’t really be implemented in risk-focused “important” industries like medical devices because they believe only classic waterfall will be accepted by the FDA.

Recently I ran across a great presentation by the folks at [Pathfinder Software][1] entitled “_[Agile Development for FDA Regulated Medical Software][2]._” Pathfinder’s engineers help explain why the FDA doesn&#8217;t know or really care about what software methodology you use as long as you ensure that the output of your development approach results in high quality, safe, reliable software. The explanation that Michael and Tavi from Pathfinder gave about “formal” versus “casual” is quite effective and it reminded me about how often I&#8217;ve had to give the same lecture. I&#8217;ve been involved in the development of Class I/II/III devices since 1995 and I’ve had to clarify confusion about the use of agile and non-waterfall software development methodologies in almost all of my projects. The confusion has only increased with the introduction of MDDS and the proliferation of mHealth and modern mobile software performing roles traditionally performed by dedicated medical devices.

The FDA’s 21 CFR Part 820 Quality System Regulations (QSR) and the numerous other regulations that derive from it (in both the USA and other countries that follow the FDA) does dictate quite a bit but detailed software development approaches are neither described nor prescribed in the QSR. Waterfall, one of the original plan-driven methodologies, became the standard not because the FDA prescribed it but because that was the norm in the latter half of the 20<sup>th</sup> century when developing extensible software was expensive and time consuming. It was a time when hardware and software were tied together and programming languages, frameworks, components, and platforms offered little forgiveness when requirements changed. This was world in which everything was custom – from purpose-built operating systems written for specific devices as well all other software components needed by a medical device. Back then it was believed that unless you wrote everything yourself you couldn’t test and depend on the code.

Much of that changed in the 90’s and then upended even further in the early part of the 21<sup>st</sup> century; we should no longer weighed down by the baggage of the past.These days even our hardware is agile and extensible, real-time operating systems are plentiful, software platforms are malleable, mHealth is well established, and programming languages are sophisticated so we need to be open to reconsidering our development approaches, especially risk-based agile.

Why should we use “risk-based” agile? Because not every single line of code in software can or should be treated equally – some parts of our medical device software can kill people, many parts merely annoy people, but most other parts simply aren’t worth the same attention as the safety-critical components. When you treat every line of code the same (as is often true in a plan-driven approach) and you have a finite amount of resources and time you end up with lower quality software and less reliable medical devices. It&#8217;s not fair to blame the FDA for our own bad practices.

Our focus in safety-critical systems is high reliability with a short time to market and excellent functionality that meets ever increasing sophistication of design. In an age when even NASA uses agile techniques to get spacecraft reliably into orbits of planets millions of miles from earth, we need to recognize that agile has a place in medical device and FDA regulated environments.

 [1]: http://www.pathf.com/
 [2]: http://www.slideshare.net/pathf/agile-development-for-fda-regulated-medical-software