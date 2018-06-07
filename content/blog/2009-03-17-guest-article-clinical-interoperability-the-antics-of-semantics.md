---
title: 'Guest Article: Clinical Interoperability – The Antics of Semantics'
author: Shahid N. Shah
type: post
date: 2009-03-17T11:49:11+00:00
url: /2009/03/17/guest-article-clinical-interoperability-the-antics-of-semantics/
oc_commit_id:
  - https://www.healthcareguy.com/2009/03/17/guest-article-clinical-interoperability-the-antics-of-semantics/1478770465
  - https://www.healthcareguy.com/index.php/archives/5101237290551
oc_metadata:
  - "{		version:1.0,		tags: {'healthcare-applications': {			text:'Healthcare applications',			slug:'healthcare-applications',			source:{			url:'http://d.opencalais.com/genericHasher-1/ea461c6b-861e-3b7c-b584-9cf9f7c5b191',			type:{			url:'http://s.opencalais.com/1/type/em/e/IndustryTerm',			iconURL:'',			name:'IndustryTerm'		},			name:'Healthcare applications',			nInstances:1		},			bucketName:'current'		},'natural-language-processing': {			text:'natural language processing',			slug:'natural-language-processing',			source:{			url:'http://d.opencalais.com/genericHasher-1/dc73ae3e-e6ad-379e-999e-164b85454e6f',			type:{			url:'http://s.opencalais.com/1/type/em/e/IndustryTerm',			iconURL:'',			name:'IndustryTerm'		},			name:'natural language processing',			nInstances:1		},			bucketName:'current'		},'first-data-bank': {			text:'First Data Bank',			slug:'first-data-bank',			source:{			url:'http://d.opencalais.com/comphash-1/d125d516-d2d1-3235-a293-c608e8bfdb03',			type:{			url:'http://s.opencalais.com/1/type/em/e/Company',			iconURL:'',			name:'Company'		},			name:'First Data Bank',			nInstances:1		},			bucketName:'current'		},'clinical-architecture': {			text:'Clinical Architecture',			slug:'clinical-architecture',			source:{			url:'http://d.opencalais.com/comphash-1/da093f3f-33fe-3198-a388-8eb65e956173',			type:{			url:'http://s.opencalais.com/1/type/em/e/Company',			iconURL:'',			name:'Company'		},			name:'Clinical Architecture',			nInstances:1		},			bucketName:'current'		},'national-library-of-medicine': {			text:'National Library of Medicine',			slug:'national-library-of-medicine',			source:{			url:'http://d.opencalais.com/genericHasher-1/60391889-3a19-347d-8dd9-719a31e9c502',			type:{			url:'http://s.opencalais.com/1/type/em/e/Facility',			iconURL:'',			name:'Facility'		},			name:'National Library of Medicine',			nInstances:1		},			bucketName:'current'		}}	}"
dsq_thread_id:
  - 5167470231
categories:
  - Opinion
tags:
  - Clinical Architecture
  - First Data Bank
  - Healthcare Applications
  - National Library of Medicine
  - Natural Language Processing

---
_In this fourth installment explaining clinical interoperability in plain English, Charlie Harp talks about semantics or the “meaning of data”. Charlie is the CEO and founder of_ [_Clinical Architecture_][1] and _has spent the last twenty years designing and developing software solutions in the healthcare industry.&#160; Here’s what he had to say in his final part of a series I’ve be doing on interoperability._

**Clinical Interoperability – The Antics of Semantics**

Semantic interoperability deals with the actual “language” contained in the conversation between applications. Solving the syntactic interoperability issue by using a standard message format does not mean that the terms used by one application are the understood by the other.

<figure id="attachment_513" style="width: 121px" class="wp-caption alignleft"><img src="http://healthcareguy.blueserf.com/uploads/2009/03/charlie_harp_bunny.png" alt="Applications can&#039;t see the bunny" title="Bunny Cloud" width="121" height="190" class="size-full wp-image-513" /><figcaption class="wp-caption-text">A computer can't understand this</figcaption></figure>**Applications Can’t See the Bunny**

In healthcare to have a meaningful exchanges we require a ‘language’ that can describe characteristics about a given situation with as little ambiguity as possible. The human brain is designed to process and recognize patterns. It’s why clouds look like bunnies and that potato chip looks like Elvis. This is why we can read “Tummy ache” and translate it on the fly to “abdominal pain” or even “gastric distress”. We are built to process ambiguity. Software applications do not share our gift for interpretation, at least not yet, so they need another way, to accurately and consistently describe the characteristics of a healthcare situation, hence the proliferation of codes.

Codes are unique values that have been assigned to represent a piece of information. They can be numbers, letters or a combination of numbers and letters. These codes can come from a content vendor, a standard public domain source or can be home spun codes created and maintained by an institution for its own purposes.

**The Problem with Code Sets**

It is important to note that there are relatively few code sets that have been created to foster interoperability. In the beginning, there were not companies that specialized in the creation and management of code sets (also known as vocabularies and terminologies). Codes were created by the organization to support the unambiguous processing of information **<u>within</u>** the organization. As applications evolved on the business side and there was a need to exchange data with trading partners, the need for third party code sets grew. Eventually, code set vendors (also known as compendia) sprang up and established proprietary code sets that could be licensed and used by both partners.

Healthcare applications have evolved. Their need to express more complex and critical clinical information has created a more extensive need for stable, granular code sets across several conceptual domains. Many code sets have evolved to support these uses and some have even evolved to help with interoperability.

Some of the domains and their code sets are as follows:

**Laboratory Tests and Observation Code Sets:**

  * [Logical Observation Identifiers Names and Codes (LOINC)][2]
  * [Systematized Nomenclature of Medicine&#8211;Clinical Terms (SNOMED-CT)][3]

**General Medical Code Sets:**

  * [International Classification of Diseases (ICD-9 and ICD-10)][4]
  * [MEDCIN point of care terminology][5]
  * [Medical Subject Headings (MESH)][6]
  * [Systematized Nomenclature of Medicine&#8211;Clinical Terms (SNOMED-CT)][3]

**Medication Code Sets (including Medication allergies):**

Public

  * [National Drug Codes (NDC)][7]
  * [NHS Read Codes][8]
  * [Health Canada Drug Product Database (DPD)][9]
  * [US Veterans Administration Drug File (NDF-RT)][10]

Commercial (in alphabetic order)

  * [First Data Bank National Drug Data File (NDDF)][11]
  * [Gold Standard (Alchemy)][12]
  * [Lexi-Comp][13]
  * [Medi-Span Master Drug Database (MDDB)][14]
  * [Micromedex DRUGDEX][15]
  * [Multum Lexicon][16]
  * [Systematized Nomenclature of Medicine&#8211;Clinical Terms (SNOMED-CT)][3]

**Units of measure:**

  * [Unified Code for Units of Measure (UCUM)][17]

Procedures:

  * [Current Procedure Terminology (CPT)][18]

Specialty Code Set Examples:

  * [Current Dental Terminology (CDT)][19]
  * [Diagnostic and Statistical Manual of Mental Disorders (DMS-IV)][20]

I will stop here, but anyone that has seen the [Unified Medical Language System (UMLS) list of sources][21] knows that I have just scratched the surface. There are over 100 terminology sources, and that’s not counting the home grown terminologies that are still in use in many institutions for various domains.

**Take the Blue Pill**

So how do you facilitate semantic interoperability when dealing with such diversity?

There are two answers to this question.

The **easy way** is to convince your exchange partner to abandon their code set and adopt yours. This means that they will have to potentially rewrite their application and convert all of their patient data, but it will certainly make your life easier. Oh yeah, you could adopt theirs – but that’s crazy talk.

The **other way** is to create a map that facilitates the translation of your codes into theirs and vice versa. This tends to be the way most people go about it.

**Fine, Hand Built Maps**

Here we engage our most expensive computing resource, the human being, who dutifully reviews each term in the source and target code sets and creates a map between them. This can be expensive, depending on the size and complexity of the code set. It should also be noted, that this is not a onetime gig. Code sets are living data; they grow, shrink and change. This means that the maps need to be tended to regularly. It also is better is done by a knowledgeable resources who you trust to make the right choices.

Over time our friends at the National Library of Medicine worked out a way to help those trying to make interoperability with the heavy lifting.

**Universal Translator**

Unified Medical Language System or UMLS was started at the National Library of Medicine in 1986 as a long term R&D project to explore how they could overcome barriers to effective retrieval of coded information.

The UMLS is comprised of three databases: Metathesaurus, Semantic Network, and the SPECIALIST Lexicon.

  * The **Metathesaurus** represents a clinical terminology clearinghouse with inherent mechanisms for normalizing terms on a conceptual basis. 
  * The **Semantic Network** is a set of files that attempt to provide a mechanism for the categorization and hierarchical organization of applicable terms.
  * The **SPECIALIST Lexicon** is a database designed to support natural language processing.

For the purposes of semantic interoperability, we will focus on the Metathesaurus which provides a conceptual backbone for the medical terminologies that participate.

The Metathesaurus by itself does not do solve the semantic interoperability problem, but it does provide the functionality of a thesaurus by relating terms from different sources that have the same or similar conceptual meanings.

Using the Metathesaurus is both simple and complex. I won’t go into the details here, but I will be releasing a whitepaper in the near future designed to help understand it. In the meantime there are a number of great sources of information starting with the NLM [provided documentation][22], which is actually pretty good. 

In a nutshell, the Metathesaurus maps the source codes provided by the creators of the different code sets to unique strings (SUIs), normalized lexical terms (LUIs) and distinct concepts (CUIs). This information lives in the primary file in the Metathesaurus, MRCONSO. The name of this file stands for Metathesaurus Relational Concepts and Sources in a quaint 1980’s limited filename sorta way.

<img src="http://healthcareguy.blueserf.com/uploads/2009/03/charlie_harp_umls_mrconso_concept_diagram.png" alt="charlie_harp_umls_mrconso_concept_diagram" title="charlie_harp_umls_mrconso_concept_diagram" width="545" height="367" class="alignnone size-full wp-image-516" srcset="/img/uploads/2009/03/charlie_harp_umls_mrconso_concept_diagram.png 545w, /img/uploads/2009/03/charlie_harp_umls_mrconso_concept_diagram-300x202.png 300w" sizes="(max-width: 545px) 100vw, 545px" />

The second most used file in the Metathesaurus is MRREL. This is the file that contains the relationships between concepts that supports the traversal of a source’s ontology.

Also included in the Metathesaurus are files that describe hierarchies, ambiguous terms, co-occurrences and attributes among other details.

For the world of medication terminologies, NLM has created a specialized subset of the Metathesaurus called [RxNorm][23]. Part of the complexity of using the Metathesaurus is the steps involved to extract a subset of sources. By focusing on medication terms, RxNorm is easier to use and update. Being focused on medication relationships, RxNorm provides an excellent source of conceptual mapping for the complex and highly utilized medication terminology subset.

****

**Leveraging the Metathesaurus**

Whether you are using the a custom subset of the Metathesaurus or RxNorm it is a useful to aid you in establishing maps between code sets in support of interoperability. I am not sure I would rely entirely on the either as a standalone source for this task. It is always important to note that the updates in the Metathesaurus can and will lag behind those form the sources. If you rely entirely on the Metathesaurus the fidelity of your interoperability is likely to suffer. 

**This Old Code Set**

It is worth noting, that if you are dealing with a homegrown code set you are pretty much on your own. This makes more work, but remember the language of healthcare is fairly distinct, especially if you know the context if use. A home grown code value associated with the word ‘acetaminophen’ can get me to an established code value for ‘acetaminophen’ if I know they are both how a patient described an ingredient they were allergic to. If you are in a position to move off of a home grown code set, you should check the Metathesaurus source list and ask around for a good public or commercial source. 

**Resources That Can Help**

There are a number of companies and tools that can help with the creation and management of maps. You can find them by googling ‘clinical interoperability’. I would also be happy to provide recommendations, so feel free to [contact me][24].

 [1]: http://www.clinicalarchitecture.com/
 [2]: http://loinc.org/
 [3]: http://www.ihtsdo.org/
 [4]: http://www.cdc.gov/nchs/icd9.htm
 [5]: http://www.medicomp.com/
 [6]: http://www.nlm.nih.gov/mesh/
 [7]: http://www.fda.gov/cder/ndc/
 [8]: http://www.connectingforhealth.nhs.uk/systemsandservices/data/readcodes
 [9]: http://www.hc-sc.gc.ca/dhp-mps/prodpharma/databasdon/index-eng.php
 [10]: http://www.va.gov/vdl/documents/Clinical/Pharm-National_Drug_File_(NDF)/psn_4_tm_r0209.pdf
 [11]: http://www.firstdatabank.com/
 [12]: http://www.alchemyrx.com/
 [13]: http://www.lexi.com/
 [14]: http://www.medispan.com/
 [15]: http://www.micromedex.com/
 [16]: http://www.multum.com/Lexicon.htm
 [17]: http://unitsofmeasure.org/
 [18]: http://www.ama-assn.org/ama/pub/physician-resources/solutions-managing-your-practice/coding-billing-insurance/cpt.shtml
 [19]: http://www.ucci.com/was/ucciweb/dentists/cdt-terms.jsp
 [20]: http://www.dsmivtr.org/
 [21]: http://www.nlm.nih.gov/research/umls/metaa1.html
 [22]: http://www.nlm.nih.gov/research/umls/meta2.html
 [23]: http://www.nlm.nih.gov/research/umls/rxnorm/overview.html
 [24]: mailto:charlie_harp@clinicalarchitecture.com?subject=Clinical%20Interoperability%20Help