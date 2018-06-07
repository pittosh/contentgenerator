---
title: 'Guest Article: How to do real clinical interoperability right now'
author: Shahid N. Shah
type: post
date: 2009-03-09T01:55:12+00:00
url: /2009/03/09/guest-article-how-to-do-real-clinical-interoperability-right-now/
oc_commit_id:
  - https://www.healthcareguy.com/2009/03/09/guest-article-how-to-do-real-clinical-interoperability-right-now/1478770458
  - https://www.healthcareguy.com/index.php/archives/4921236563767
ratings_users:
  - 1
ratings_score:
  - 5
ratings_average:
  - 5
oc_metadata:
  - '{    version:1.0,    tags: {}  }'
dsq_thread_id:
  - 44284002
categories:
  - Opinion
  
---
_Last week I asked Charlie Harp to explain what clinical interoperability is – in plain english. Charlie is the CEO and founder of_ [_Clinical Architecture_][1] and _has spent the last twenty years designing and developing software solutions in the healthcare industry.&#160; Here’s what he had to say in his third part of a series I’ve be doing on interoperability. In this last article he presents some techniques that can be used right now to do real clinical interoperability. Enjoy his third installment._

As mentioned in the first article in this series, two critical parts of Clinical Interoperability are physical and syntactic interoperability. These two are essentially the first and second of what I consider to be the four laws of interoperability dynamics.

In order for two applications to exchange high fidelity information about a patient, there must be:

1. A physical transport mechanism and the low level protocols that physically move the information from one system to another.

2. An understanding of how the information is packaged for transport by the sender so that the receiver can extract the information. 

3. A common terminology (or translation mechanism) for the relevant, codified patient information so that the receiving application can ‘understand’ the information once extracted.

4. Equivalent functionality in both applications.

This article focuses on the first two of these.

**Physical Interoperability**

What is interesting about the physical transport of critical information is that people outside of healthcare probably think that our industry is dominated by the electronic data transactions. I am not sure that is the case. One example of this is prescriptions. According to NACDS, of the 3.5 million prescriptions filed in 2007, only 2.1% were processed via electronic messaging. Keep in mind that the medication prescription area is one of the most advanced, in terms of electronic messaging, in healthcare. So, today, when we talk about physical interoperability, we are talking about transport mechanisms that include ‘sneaker-net’, faxing, file transfers as well as pure electronic processing. This works today because there are people that are acting as interoperability adapters. They are interpreting the data, transforming it and entering it into the receiving system. This ‘chair to keyboard interface’ approach is very inefficient, error prone and, technically, does not qualify as ‘high fidelity’.

When we talk about the physical transport mechanisms in the future, what are we looking for? A combination of existing networking technology, communication protocols and data exchange software (commercial or home grown) are fairly ubiquitous. The reason for the low adoption is not a reflection of a lack of readiness on the physical side of things. We have the plumbing to support good clinical interoperability, so what is the problem? Perhaps we don’t have good standards for message syntax. 

**Syntactic Interoperability**

If this were a treatise on healthcare messaging standards, it would be much much longer than an article and written by someone other than me. Back in the early days of my career (right after we eliminated the dinosaur problem), I was involved in the business of laboratory interfaces. In the beginning, most interfaces between applications, or applications and devices, were complete custom endeavors. The two parties would negotiate a format and write their respective parts. After a while, standards began to emerge. The first I was involved in was the ASTM standard for laboratory information exchange, which went on to become what is now Health Level 7 (HL7). It wasn’t perfect, but it served our purpose and saved us from reinventing the wheel. So we adopted it.

Today, there are several standard messaging formats that play a role in healthcare interoperability. Their scope and maturity are proportional to their drivers and adoption. For the purposes of this article, I will describe a few of the major formats that have significant adoption, or are in the news. 

Note: If your favorite standard is not mentioned, please feel free to throw it in the comments section. Just make sure that it is not in the standard graveyard. My rule of thumb is, if three out of four search engine links resolve to a missing page, the standard is likely not a going concern.

**<u>Electronic Prescribing</u>**

**NCPDP SCRIPT Standard**

The NCPDP script standard is a collection of message formats designed for the express purpose of facilitating electronic prescribing. It was approved as a national standard in 1997 and became the official standard for pharmacy claims in HIPAA in 2000. Visit the [NCPDP website][2] for more information.

**<u>General Healthcare Information Exchange</u>**

These standards are designed to provide common formats to support a number of common transactions in a healthcare setting.

**Health Level 7 (HL7) Version 2.x**

HL7 v2.x is a collection of messaging standards including: Patient Administration, Order Entry, Information Query, Financial Management, Observation Reporting, Medical Records, Scheduling, Patient Referral, Laboratory Automation, Patient Care, Personnel Management, and Application Management to name a few. 

This is probably the most widely adopted standard in healthcare. Version 2 was first introduced in 1990 and was intended to be an ’80 percent’ solution.

**Health Level 7 (HL7) Version 3.0**

The goals of HL7 version 3.0 were much more ambitious than its predecessor. The goal of version 3.0 included: internationalization, a consistent data model, a more precise standard and freedom from any constraints that would be imposed by compatibility with version 2.x. The complexity and proscriptive nature, and associated costs, have resulted in slow adoption of Version 3.0. Visit the [HL7 website][3] for more information on both version 2.0 and version 3.0.

**<u>Application Synchronization</u>**

**HL7 Clinical Context Object Workgroup (CCOW – pronounced ‘sea-cow’)**

The CCOW standard was introduced to provide a standard to support the visual integration of healthcare applications. Providers are often required to work across multiple applications. The CCOW standard describes a collection of mechanisms that allows applications to shift focus to the same patient. Visit the [HL7 CCOW Page][4] for more information.

**<u>Electronic Health Record Information Exchange</u>**

These standards are designed to support the exchange of a patient medical record. This is different than a transaction. A transaction is sending information and instructions to facilitate some action being performed. These formats are intended to share a current snapshot of a patient’s clinical context.

**Health Level 7 Clinical Document Architecture (CDA)**

The CDA is an XML-based markup standard intended to specify the encoding, structure and semantics of clinical documents for exchange. CDA is based on the HL7 reference information model (RIM) and is part of the version 3.0 standard.

Visit the [HL7 CDA FAQ][5] for more Information.

**ASTM Continuity of Care Record (CCR)**

The CCR was created by ASTM International, the Massachusetts Medical Society (MMS), HIMSS , the American Academy of Family Physicians (AAFP), the American Academy of Pediatrics(AAP), and other health informatics vendors. It was designed to contain the most relevant and timely core health information about a patient. It has been adopted by a number of healthcare application vendors, and most notably by Google’s Patient Health Record. More information can be found [CCR Resource Site][6].

**HL7 Continuity of Care Document (CCD)**

The Continuity of Care Document is an HL7 standard whereby a patient&#8217;s current clinical context is expressed in the framework of the Clinical Document Architecture. More information on the CCD can be found on the [HL7 website][3] under CDA Release 2.

**<u>The Standards are Out there</u>**

There is likely a message format that can satisfy your need to interoperate syntactically. The important factors are what your trading partners support and which formats can you implement without re-engineering your entire application. There are also a number of businesses that provide adapters that can be bolted onto you application to make this easier as well.

A number of the formats mentioned also have specific terminologies that are ‘supported’ by the standard. Some support several and some require a common terminology. 

This brings us to the third law in interoperability dynamics. Even if you have an established physical transport and agreed upon standard message format, if you are not communicating using terms that the receiver can understand, you will not have a high fidelity exchange of coded information.

There are information sources and strategies for coping with terminology challenges. Like some medical conditions, there is currently no cure, but there may be a way we can manage it until there is. That is the subject of the next article.

 [1]: http://www.clinicalarchitecture.com/
 [2]: http://www.ncpcp.org/
 [3]: http://www.hl7.org/
 [4]: http://www.hl7.org/special/Committees/ccow_sigvi.htm
 [5]: http://www.hl7.org/documentcenter/public/faq/cda.cfm
 [6]: ht
tp://www.ccrstandard.com/