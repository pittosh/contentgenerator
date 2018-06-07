---
title: 'Guest Article: How to test health IT interoperability'
author: Shahid N. Shah
type: post
date: 2013-02-25T02:20:31+00:00
url: /2013/02/24/guest-article-how-to-test-health-it-interoperability/
oc_commit_id:
  - https://www.healthcareguy.com/2013/02/24/guest-article-how-to-test-health-it-interoperability/1478770821
dsq_thread_id:
  - 5163819254
categories:
  - Uncategorized

---
_One of the key tenets of both the HITECH and Affordable Care Acts has been to drive improved patient care and reduction in cost by applying technology across all healthcare entities. A bigger challenge is how do to make multiple technology purchases interoperate within a provider network and / or across provider networks.  There are solutions out there that can make it happen, but to make sure_ _interoperability_ _happens consistently, testing technology integration touch points is crucial but not easy without the right test infrastructure. I reached out to Michael Brown, a senior Health IT specialist at to [AEGIS.net][1]__ which serves__ numerous government customers, __to get some advice.  He has helped many agencies_ _as a testing consultant for several years, setting up and deploying an infrastructure for interagency information exchange so I_ _asked him to give us some advice about what_ _methods will ensure that interoperability is maintained amongst multiple systems throughout the software development lifecycle.  Here’s what Michael had to say:_

A primary element within communication, especially in the domain of Health IT is the timeliness of conveying an idea or fact while it can be used in a meaningful way. In the case of the latter example, information will need to be transferred and understood between two healthcare organizations, leading both to be able to share information, or interoperate, regarding the patient’s medical history in a timely fashion over a network. Effectively sharing this information promptly directly impacts the quality of care provided to the patient and affects the outcome of the medical episode (i.e. the emergency surgery).

The systems which facilitate interoperability do so by connecting multiple Electronic Health Record (EHR) systems through the use of Application Program Interfaces (APIs) and web services. To accelerate early adoption of EHR systems, the Center for Medicaid and Medicare (CMS) in close collaboration with the Office of the National Coordinator (ONC) implemented a set of standards and rules regarding the adaption of EHRs, deemed Meaningful Use. Many implementations of EHRs contain proprietary language and formats which are translated within APIs and transported using web service standards. The proprietary message must be converted into a standardized format readable by any EHR system. Large amounts of resources are dedicated to developing, testing, and verifying the secure exchange of healthcare information.

A method to ensure interoperability is maintained amongst multiple systems throughout the software development lifecycle is through the idea of testing early and often. This process infuses quality into the Healthcare system and limits the amount of errors encountered as a system is moved into a production environment. Open source tools, such as the Developers Integration Lab (DIL) provide a method to ensure quality throughout the development lifecycle and ensure interoperability as a system is on boarded into a production environment.

#### The Pieces of Bi-Directional Health Information Exchange

[<img style="border: 0px; background-image: none; padding-top: 0px; padding-left: 0px; display: inline; padding-right: 0px;" title="image" alt="image" src="/img/uploads/2013/02/image_thumb.png" width="499" height="124" border="0" />][2]

Referring to the above figure, an EHR vendor directly connects to an adapter, and the adapter to the gateway. The adapter is the component which transforms the EHR specific message into a standards based message. The message is then transported at the gateway layer to another gateway on another node, picked up, and processed within another EHR’s adapter. These gateways contain endpoints which are used to send various types of web service calls. This type of architecture is most often found within a bi-directional health information exchange, or BHIE. There are other architectures. For example, a messaging architecture known as Direct utilizes secure email to transfer healthcare information between providers.

The transformed message within the adapter is sent out in a standard format using Simple Object Access Protocol, or SOAP message relying on Extensible Markup Language (XML) to provide structure to the message. The SOAP message invokes a specific web service and is transported from one valid gateway to another. The message can be in either the form of a request message (seeking specific information in another health system) or a response message (responding to a request from another system to provide specific information). The SOAP message transferred between the endpoints may contain security headers to ensure only a specific endpoint can understand the message.

#### Testing Interoperability

Many systems currently onboarding at the Federal level (eHealth Exchange) or State level (various State Health Information Exchanges) utilize variations of the described architecture. Testing this architecture, the message structure, and the various system APIs is a complex undertaking requiring a robust test harness.

[<img style="background-image: none; padding-top: 0px; padding-left: 0px; display: inline; padding-right: 0px; border: 0px;" title="image" alt="image" src="/img/uploads/2013/02/image_thumb1.png" width="506" height="274" border="0" />][3]

Upgrading a component within a healthcare system may directly impact interoperability among multiple healthcare systems. As systems are updated within an organization’s ecosystem, testing must occur in a test environment which accurately simulates production use. As displayed in the above figure, a break in the connection between the Patient Database and the Health System, possibly due to a server upgrade, has severely impacted the usability of the system. The Health System can no longer exchange requested patient information with outside vendors. The figure demonstrates how upgrading a Patient Database may impact various other components and create interoperability challenges.

Recently, an open source test harness has been created for providing a method for developers and testers to actively test interoperability throughout the development life cycle. The Developers Integration Lab (DIL), an open source tool provides a large volume of Synthetic Patient information which allows a user to register endpoints and begin testing against multiple hosted systems in a simulated production environment. A general overview of the Open Source testing tool is provided here: <https://www.youtube.com/watch?v=gHVwpxpVwbQ>.

Interoperability is a fragile yet necessary component of the modern healthcare system. Patients rely on interoperability among multiple systems and organizations to properly collect and receive benefits, payouts, and overall improved quality of care. Testing interoperability must be completed in an iterative, agile fashion; ensuring bugs are found and repaired prior to a production release. Through the use of iterative, open source testing tools for healthcare interoperability, systems may maintain a high level of interoperability providing a method for healthcare providers to guarantee an increased level of care to patients, the creation of the longitudinal health record, and meeting the standards highlighted within Meaningful Use Stage 2 and beyond.

 [1]: http://www.aegis.net/
 [2]: /img/uploads/2013/02/image.png
 [3]: /img/uploads/2013/02/image1.png