---
title: 'HL7 Interface Documentation: 6 Questions Hospital CIOs and IT Directors Should Be Asking Vendors'
author: Shahid N. Shah
type: post
date: 2011-01-12T00:42:42+00:00
url: /2011/01/11/hl7-interface-documentation-6-questions-hospital-cios-and-it-directors-should-be-asking-vendors/
oc_commit_id:
  - https://www.healthcareguy.com/2011/01/11/hl7-interface-documentation-6-questions-hospital-cios-and-it-directors-should-be-asking-vendors/1478770716
dsq_thread_id:
  - 5161509367
categories:
  - Uncategorized

---
_With healthcare IT integration tasks finally taking off because of Meaningful Use and other care collaboration requirements, HL7 interfaces will become even more important. After being involved in dozens of interfacing efforts over the past decade or so, I have found one of the most time-consuming aspects of integration is HL7 interface documentation: nobody has time to do it and it&#8217;s almost always treated as a &#8220;nice to have&#8221;. Given my experience I was thrilled to find that someone was finally putting together some solutions to make conformance specifications easier to document. I was even happier when it was a friend of mine, Jean-Luc Morin from [Caristix][1], working on a solution. Like me, Jean-Luc has felt that pain of integrations acutely so I asked him to give us all some advice. Here&#8217;s what Jean-Luc wrote about what CIOs and IT Directors should be asking their vendors and partners about documentation when creating HL7 interfaces._

## 50-100 Interfaces per Hospital

A quick HIMSS survey from 2008 stated that 60% of hospital CIOs are faced with juggling over 100 applications in their information systems. 85% are dealing with over 50 interfaces, while 60% are faced with more than 100. The HIMSS survey may be informal, but it confirms a major connectivity issue in our industry: there are a lot of interfaces out there. Interfacing and integration concerns aren’t going away anytime soon, especially with Meaningful Use as a driver.

Clearly, interfacing is a hot technical topic for CIOs and their integration teams. Yet this is just the beginning. There’s another strategic issue that &#8212; thus far &#8212; has stayed under the radar.  That issue is interface documentation.

## Interface Documentation Practices and Project Success

At first glance, documentation doesn’t seem like a CIO-level concern. In a typical implementation cycle, the team gets a few specs from a vendor. Someone signs off on an interface configuration document. Then you implement and go-live. The role of documentation in the larger scheme of things? Seems like a project management checkbox at best.

But it isn’t.

Your vendor’s interface documentation practices can have a major impact on the speed and success of implementation and on the maintainability of your new system after go-live.

With that in mind, we’ve prepared a list of questions for CIOs and IT directors to ask their vendors before signing on the dotted line.

  1. **Which HL7 2.x version are you using?** This question is a no-brainer. But ask it anyway. This question lays the groundwork for the next one.
  2. **Within your HL 7 2.x based interface, can you tell me which elements and values are configurable?** You need the details. If they can’t provide details on configurability, you might be facing a longer test cycle than anticipated. Trial-and-error interface validation can slow down implementation.
  3. **How often do you update your interface specification?** This will tell you how frequently you’ll be facing a bi-directional interface upgrade. Check on the interface maintenance contract, and be sure to build any extra expenses into your budget cycle.
  4. **When you send us the interface spec for sign-off, do we get a fully documented list of gaps and exceptions for specific data values and data elements?** You want a full list, or you’ll be facing a lengthy validation process, waiting for super-users and clinical testers to flag bugs in the test system.
  5. **Do you provide a list of your interface customizations?** No interface specification works perfectly out of the box.  It has to be customized to your environment. You need a list of those customizations for troubleshooting and maintenance, or your interface analysts will be waiting on vendor trouble tickets while clinician calls are piling up on the hospital IT help desk.
  6. **How do you document changes and upgrades throughout the lifecycle of the interface? Do you automatically provide us with updated documentation?** If there’s anything worse than missing documentation, it’s partial or out-of-date documentation. What you get at go-live will not be usable two years out. Make sure the responsibility for documentation updates is handled clearly.

## Avoiding Death by a Thousand Paper Cuts

These questions may seem highly detailed and technical for a single set of interfaces for a single new product. But multiply these details over the course of a hundred interfaces. With that many interfaces to manage, poor documentation can fuel a productivity and deliverability nightmare for CIOs, as team members scramble to play catch-up.

Clarify these issues upfront with your vendors, so you can mitigate risk down the road.

 [1]: http://www.caristix.com