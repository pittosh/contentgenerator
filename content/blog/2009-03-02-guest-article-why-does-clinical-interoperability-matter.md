---
title: 'Guest Article: Why does clinical interoperability matter?'
author: Shahid N. Shah
type: post
date: 2009-03-02T15:23:34+00:00
url: /2009/03/02/guest-article-why-does-clinical-interoperability-matter/
oc_commit_id:
  - https://www.healthcareguy.com/2009/03/02/guest-article-why-does-clinical-interoperability-matter/1478770456
  - https://www.healthcareguy.com/index.php/archives/4901236007414
oc_metadata:
  - "{		version:1.0,		tags: {'health-networks': {			text:'health networks',			slug:'health-networks',			source:{			url:'http://d.opencalais.com/genericHasher-1/14cf4813-11d1-311c-9a77-8a6ba3eb0510',			type:{			url:'http://s.opencalais.com/1/type/em/e/IndustryTerm',			iconURL:'',			name:'IndustryTerm'		},			name:'health networks',			nInstances:1		},			bucketName:'current'		},'healthcare': {			text:'healthcare',			slug:'healthcare',			source:{			url:'http://d.opencalais.com/genericHasher-1/456f7843-b46a-3245-b537-49661db4c976',			type:{			url:'http://s.opencalais.com/1/type/em/e/IndustryTerm',			iconURL:'',			name:'IndustryTerm'		},			name:'healthcare',			nInstances:1		},			bucketName:'current'		},'charlie-harp': {			text:'Charlie Harp',			slug:'charlie-harp',			source:{			url:'http://d.opencalais.com/pershash-1/117c9b2f-abee-3e71-b331-037ac4afcf09',			type:{			url:'http://s.opencalais.com/1/type/em/e/Person',			iconURL:'',			name:'Person'		},			name:'Charlie Harp',			nInstances:1		},			bucketName:'current'		},'clinical-architecture': {			text:'Clinical Architecture',			slug:'clinical-architecture',			source:{			url:'http://d.opencalais.com/comphash-1/da093f3f-33fe-3198-a388-8eb65e956173',			type:{			url:'http://s.opencalais.com/1/type/em/e/Company',			iconURL:'',			name:'Company'		},			name:'Clinical Architecture',			nInstances:1		},			bucketName:'current'		},'e-prescribing': {			text:'e-prescribing',			slug:'e-prescribing',			source:{			url:'http://d.opencalais.com/genericHasher-1/2cc9727f-67cc-3517-abb7-ca05212e95a6',			type:{			url:'http://s.opencalais.com/1/type/em/e/IndustryTerm',			iconURL:'',			name:'IndustryTerm'		},			name:'e-prescribing',			nInstances:1		},			bucketName:'current'		}}	}"
dsq_thread_id:
  - 5187370446
categories:
  - Opinion
tags:
  - Charlie Harp
  - Clinical Architecture
  - e-Prescribing
  - Health Networks
  - Healthcare

---
_Last week I asked Charlie Harp to explain what clinical interoperability is – in plain english. Charlie is the CEO and founder of_ [_Clinical Architecture_][1] and _has spent the last twenty years designing and developing software solutions in the healthcare industry.  Here’s what he had to say in his second part of a series I’ll be doing on interoperability._

Now that we have a documented definition for clinical interoperability and its macro components, the next reasonable question is: “Why is clinical interoperability important?”

Before continuing, please consider the following interoperability scale.

[<img style="border: 0pt none; display: inline;" title="clip_image002" src="http://healthcareguy.blueserf.com/uploads/2009/03/clip-image002-thumb.jpg" border="0" alt="clip_image002" width="365" height="54" />][2]

This scale represents the potential signal loss when information is exchanged between systems through a computer interface. The line represents the clarity of the information as the level of interoperability improves. This is also relevant, as the Certification Commission for Healthcare Information Technology, or [CCHIT][3], has defined interoperability as _“__the **high fidelity exchange** of information between an EHR system and other healthcare IT systems.”_

Isolated systems cannot exchange clinical information about a patient, so the amount of signal loss between them is 100%.

Systems with a translational relationship exchange information, but not in a way that a software application can take advantage of. An example of this is when systems can exchange notes about a patient or systems that can exchange free text patient information. It requires a human to translate the information and take any action or decision support.

Interoperable systems can exchange information, and a percentage of the information can be put to coded, productive use. This type of relationship usually has established syntactic interoperability, but less than ideal semantic interoperability. In other words, it is getting messages but some of the information must be translated as free text for a human to interpret.

Compatible systems are leveraging established syntactic and semantic interoperability mechanisms with a high percentage of useful exchange. An example of this is two systems exchanging HL7 messages operating on the same terminology.

Integrated systems (as the name implies) operate on a common framework. An integrated relationship is driven by strict adherence to a common standard and a common or well-correlated set of terminologies.

It is not uncommon for people to say they have an interface between systems, even if the interface is translational and provides limited value to the consuming application. I offer this scale to provide a vocabulary to further describe the capabilities and utility of an interface in the interoperability dialog and to further refine our question to “Why is **High Fidelity** Clinical Interoperability Important?”

There are two answers to this question. One explains why interoperability has been important and the other tells why interoperability will become even more important in the near term future.

Interoperability has been important to the Healthcare End users for at least the last decade for the following reasons:

**Data Exchange with trading partners**

A system’s ability to provide high fidelity information to its trading partners during a commercial transaction is imperative to supporting high-volume data exchange, as well as ensuring the accuracy of the information itself. Some examples of this are: reference laboratory testing, e-prescribing and drug formulary compliance.

**Data Exchange between Co-Mingling Applications within a Healthcare Institution**

Many institutions have a core application that is responsible for the current patient information. They may also have additional niche applications, like an Emergency or ICU specific application, that comes from another application vendor. In this situation, the disparate applications are not integrated, but the need to exchange the patient’s information is as relevant as if they were.

**Data Exchange between Co-Mingling Applications within a Network of related healthcare Institutions.**

There has been much consolidation in the healthcare industry as health networks merge and grow through acquisition. When this happens, it is often the case that the new siblings do not use the same core applications. In this situation, there is still a need to exchange a patient’s information when they move from venue to venue, without the effort and risk associated with manual data entry.

**Data Aggregation and Biosurveillance**

With the advent of PHRs and RHIOs, there is a desire to move patient information to repositories so that the aggregated, centralized data can be put to use to the benefit of the patient and/or the healthcare industry at large.

All of these and more are reasons why the end users of healthcare IT have been rending their garments and gnashing their teeth. These are the reasons that solutions interoperability is better now than it was ten years ago, even though it is not yet where it needs to be.

Healthcare IT is changing. It has been recognized that for the industry to evolve and improve, it must begin movement toward convergence. The road to convergence is paved with interoperability.

Enter the Certification Commission for Healthcare Information Technology, mentioned earlier, whose mission is _“to accelerate the adoption of robust, **interoperable** health information technology by creating a credible, efficient certification process”._

There is, and will continue to be, growing pressure on application vendors to become CCHIT certified. While CCHIT certification is more than just interoperability, there are 39 requirements statements that relate directly to clinical interoperability in the ambulatory system certification and 22 in the inpatient system certification requirements.

The need-driven interoperability of the last decade was really about the exchange of information between distinct applications, often limited to an operational transaction. In other words, it was sending an HL7 records to perform some discrete task or it was passing a complete patient context to a system it was tightly coupled to through a specific translational process.

By contrast, the CCHIT driven interoperability is more focused on general/holistic interoperability, requiring an accepted message format and terminology set.

CCHIT interoperability does not require that I know about my partner. I should be able to exchange a patient’s clinical context with anyone who is CCHIT certified.

Whether you are an HIT application vendor looking to share data with business partners, cooperate with high performance niche applications and support your client’s acquisition-related issues, or are concerned about being left behind because you can’t put a mark in the CCHIT compliance check box, high fidelity clinical interoperability IS important.

The next question is how to make it happen. That is the subject of another article.

 [1]: http://www.clinicalarchitecture.com/
 [2]: http://healthcareguy.blueserf.com/uploads/2009/03/clip-image002.jpg
 [3]: http://www.cchit.org