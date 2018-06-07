---
title: 'Guest Article: Techniques for matching patient record data across disparate EHRs and other systems'
author: Shahid N. Shah
type: post
date: 2012-02-09T04:04:32+00:00
url: /2012/02/08/guest-article-techniques-for-matching-patient-record-data-across-disparate-ehrs-and-other-systems/
oc_commit_id:
  - https://www.healthcareguy.com/2012/02/08/guest-article-techniques-for-matching-patient-record-data-across-disparate-ehrs-and-other-systems/1478770784
dsq_thread_id:
  - 5163223883
categories:
  - Engineering
  - Patient Association

---
_Some of the most frequent questions I receive these days surround data interoperability and integrating multiple health IT systems. One of the biggest problems in connectivity is matching patient record data and ensuring that the same patient data in different systems is linked properly. Given how many times this topic comes up, I reached out to Cameron Thompson, [Acxiom Healthcare Group][1] Managing Director. Acxiom has an interesting method of patient data matching, called persistent links, and when I saw what they were doing for matching consumer records in non-healthcare settings (e.g. marketing) I thought some of you might want to learn about it. Here’s what Cameron had to say about the various techniques for matching patient data:_

The promise of secure and seamless exchange of patient healthcare information is powerful. As payers, providers, Health Information Exchanges (HIXs) and Accountable Care Organizations (ACOs) move rapidly toward the full deployment of electronic medical records, healthcare IT professionals are grappling with a fragmented network of systems and data silos. These disparate systems and databases often house redundant copies of patient medical data in multiple formats, which limits the ability to see a true 360-degree view of the patient. The benefits from connected patient data are many, including:

  * Reductions in inaccurate coverage determinations.
  * Intelligent information sharing for clinical decision making.
  * Honoring patient consents and preferences consistently and accurately.
  * Minimizing risks of data breach with a unique health identifier that allows the transfer of patient information but NOT personally identifiable information such as name and address.
  * Reduction in time and effort in administrative processes including billing or claims inaccuracies.
  * Avoiding costly duplication or unnecessary testing.

To reduce these inefficiencies and solve the underlying problem, the new healthcare ecosystem needs an accurate means of identifying and matching patient record data to the correct individual across internal and external healthcare systems, including collaborative care delivery models.

Multiple systems across the healthcare enterprise produce duplicate patient records that are not easily recognizable as matches. Recognizing that Mary Jane Smith at 123 Elm Road in the 2009 clinical laboratory system is also Mary Collins of 78 Oak Street in the 2011 patient registration system is a challenge for any organization. Identifying a solid method for distinguishing patient information across multiple data systems and combining the data accurately will be pivotal to the effective adoption of Electronic Health Records (EHRs) and successful implementation of Health Information Exchange (HIE). 

As organizations take on this challenge, several methods have been identified and considered to recognize an individual. Three leading methods can to be explored to achieve your business goals of continuity and cost reduction. These are:

**1.** **Algorithm or String-Based Matching**

An organization can develop an algorithm with string-based matching using identifiers in the existing data to uniquely identify individuals. The benefits of string-based matching include:

  * Recognizable practice – This is a well-known practice and resources capable of creating these programs are plentiful.
  * Options for processing – Algorithms can be created internally and run without sending data outside the organization or an external organization can be identified to conduct the match on the organization’s behalf. 

Some of the challenges with this strategy include:

  * Inherent challenges in string-based matching – String-based matching relies on consistencies in reported names and addresses, which tend to change often.
  * Ensuring the accuracy of the data used in the algorithm – Manually entered names and addresses are often laden with inexactness. This makes string-based matching more difficult.
  * Absorbing the costs to develop and enable this identifier across systems – Costs would need to be incurred to develop, maintain and put the identifier into use across systems. 

**2.** **State-Issued Number**

An organization can use another state-Issued number such as a state of issuance and birth certificate number. Benefits of this method include:

  * Development cost savings – using existing assigned identifiers would save costs on development of a new identifier.
  * Availability &#8211; an organization could select an identifier that is already available in many systems.

Some challenges with this strategy include:

  * Inconsistent data fields and record lengths – if state issued numbers are of different lengths this could create difficulty for the programmer creating the data field.
  * Protecting personal information from fraudsters – using a state-issued number could raise concern over identity theft with the proliferation of stolen Social Security numbers. Whether real or perceived, this information being made available opens the door for fraudsters to invade an individual’s privacy.

**3.** **Persistent Links**

Healthcare organizations should consider the use of highly accurate match technology that delivers knowledge-based persistent linking. This match technology delivers a set of persistent links a company uses to recognize their patients across a fragmented network of systems and data silos. Persistent Link match technology is regarded as the most precise match technology available to accurately resolve patient identity (such as AbiliTec, the linking technology offered by my company, Acxiom). The link provides a consistent, client-specific ID, across data variations, and it can be applied at all touch points and databases within an organization.****

The use of persistent links, created from knowledge-based match technology, can provide:

  * More accurate patient recognition and identity resolution.
  * Greater control and governance around the patient data because each healthcare entity receives a dedicated set of encoded links, specific to their enterprise. This facilitates link transactions, minimizing the amount of personal identifiable information exchanged, aligning with the need for HIPAA compliance. Further, when multiple entities interact (e.g. an Accountable Care Organization between provider and payer) a unique link reconciliation can be processed by the provider in batch or real time.
  * A minimized amount of personal information that a healthcare entity needs to store as they use encoded links to integrate data and recognize patients. 
  * Eliminate an upfront investment to develop and maintain identifiers. The first two options I mentioned – algorithms/string-based matching and state-issued numbers – require healthcare entities to develop and maintain the identifiers. 
  * · Creation of a refresh cadence based on specific business needs, say monthly or quarterly, reducing non-matching exposure to the cadence latency. 

There are also some challenges related to using persistent links:

  * Persistent link application and maintenance will be more costly and an organization needs to be willing to look at the investment in higher quality.
  * The healthcare organization needs to be willing and able to transmit records with personally identifiable information in a privacy compliant manner, such as encryption.

As healthcare organizations move forward by adopting technology to improve patient experience they will find that the accuracy of the data will drive their success. Organizations should consider each of these methods for recognizing patients, each have their benefits and select the method that best meets specific organizations needs. 

The foundation of an effective provider and payer relationship depends on recognizing the patient throughout the continuum of patient care. If the healthcare community can provide accurate patient information, billions of dollars can be captured yearly and patient healthcare would become much more efficient, inevitably leading to improved outcomes.

 [1]: http://www.acxiom.com/Industry-Solutions/Healthcare/