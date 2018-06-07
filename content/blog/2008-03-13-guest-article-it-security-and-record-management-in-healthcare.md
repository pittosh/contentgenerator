---
title: 'Guest Article: IT Security and Record Management in Healthcare'
author: Shahid N. Shah
type: post
date: 2008-03-13T19:49:31+00:00
url: /2008/03/13/guest-article-it-security-and-record-management-in-healthcare/
oc_commit_id:
  - https://www.healthcareguy.com/2008/03/13/guest-article-it-security-and-record-management-in-healthcare/1478770399
views:
  - 2
  - 2
ratings_users:
  - 5
ratings_score:
  - 25
ratings_average:
  - 5
dsq_thread_id:
  - 5216783789
categories:
  - Opinion

---
_Many of my readers have been asking about security, privacy, and HIPAA these days. I thought I would reach out an expert &#8212; Dr. Zachary Peterson. Zachary is a Senior Security Analyst at_ [_Independent Security Evaluators_][1] _a computer security consulting firm in Baltimore, MD. Dr. Peterson earned his Ph.D. in Computer Science at The Johns Hopkins University, where his dissertation was on new technologies to meet regulatory compliant storage system. He also has a Masters in Security Informatics and a Masters in Computer Science. Independent Security Evaluators, started by Johns Hopkins Professor, Dr. Avi Rubin, is a small team of security experts that specialize in evaluating, designing and building secure systems. ISE&#8217;s client list includes MasterCard, Verdasys, WebEx, and PGP &#8212; they know what they&#8217;re doing._

_ISE is expanding its services to include developing and implementing the correct policy and technology solutions required to meet regulatory compliance._

_Here&#8217;s Zachary&#8217;s posting:_</p> 

With the introduction of computers to the health care system, paper medical records have given way to their electronic counterparts, allowing information to be easily accessed, shared and modified. Systems for managing electronic records are now commonplace in all major and health care related institutions. They increase productivity, disappear geographic boundaries, and improve quality of service. It is not all good news, however. 

The same features of electronic records that make them beneficial can also be used for malicious purposes. Duplicate records can be made instantaneously and clandestinely, threatening privacy. The loss of 26.5 million veteran medical records by the VA is a notable example. Electronic records are also extremely malleable, leaving open the possibility of forgery and falsification &#8212; a physician involved in a malpractice suit may wish to alter the record. 

Indeed, the importance of securing and authenticating electronic records transcends health care, and has led legislators to create an ever increasing body of electronic record management legislation. There now exists many federal, state and local pieces of legislation that govern the management of electronic records, requiring corporations and government agencies alike to rethink their current electronic record systems. This is particularly true for health care entities with the passage of the Health Insurance Portability and Accountability Act (HIPAA).

As we all know, HIPPA requires "covered entities," which include hospitals, insurance companies, billing agencies, and even individual physicians, to provide privacy and security guarantees for a patient&#8217;s electronic records. Despite the lack of specificity in the legislation, computer system vendors have quickly identified the large market opportunity for "HIPAA compliant storage". Many of these products, however, fail to meet the requirements of HIPAA, mostly adding policy enhancements to existing storage platforms. There is a growing consensus among computer security experts, such as those at [Independent Security Evaluators][2], that health care entities should understand the true requirements mandated by HIPAA and adopt appropriate technologies to ensure compliance. 

**The Law** 

The Health Insurance Portability and Accountability Act, enacted in 1996, was intended to improve the efficiency and effectiveness of the health care system by making individual&#8217;s medical information easily transfered between insurers. As part of the Act, legislators addressed the privacy and security implications of sharing sensitive patient data. HIPAA includes two provisions, the Privacy Rule and the Security Rule, that require covered entities to address the security and privacy of "protected health information" (PHI). 

The HIPAA Standards for Privacy of Individually Identifiable Health Information, or _Privacy Rule_, addresses the use and disclosure of PHI. One of the key components of the Privacy Rule requires covered entities to implement, access control and error correction</ i> procedures, allowing an individual to manage how their personal information will be used, including limiting the marketing of their PHI. 

The HIPAA _Security Rule_ acts as a complement to the Privacy Rule, requiring a covered entity to ensure the confidentiality, integrity and availability of all electronic PHI that is created, received, maintained or transmitted by a covered entity. The entity must protect against reasonable threats and hazards, as well as protect against any reasonably anticipated misuse or unauthorized disclosure. 

**The Technology** 

The requirements set out by HIPAA are broad, complex and very often, ambiguous. To worsen matters, the penalties for failure to comply may be steep. Fortunately, the requirements fall into three broad categories. In general, HIPAA requires electronic records to be available, private and confidential, and authentic. 

  * Available means that all records must be accessible in real-time &#8212; accessing tape archives from a distant warehouse is unacceptable. This may require an organization to manage their own on-site storage system, and furthermore, retain a staff who knows how to manage it. 
  * Private and confidential means data is accessed with fine-grain controls and that data are protected from unauthorized disclosure and use &#8212; both in transit between provides and at rest on an entity&#8217;s system. Most existing compliance systems achieve this by providing only a policy-based interface, but can make no guarantees should data become lost or stolen. Systems must provide privacy and confidentiality through encrypted storage and data transmission. By correctly using encryption, systems may meet both the explicit encryption requirement of the HIPAA Security Rule and the access control requirements of the HIPAA Privacy Rule. Further, encryption can be used to permanently delete data, for example, when a patient requests a redaction under the HIPAA Privacy Rule. 
  * Lastly, systems must also employ authentication, meaning data are accurate and modifications are impossible to dispute. The HIPAA Security Rule requires a verification of the "accuracy" and "integrity" of electronic records. While encryption provides privacy from unauthorized intrusion and disclosure, it alone cannot guarantee the accuracy or integrity of the data. Without authentication, there is no way to verify that the result of a decryption is the same as original, unencrypted data. Authentication can also provide a way to bind an individual to their data modifications, making repudiation impossible. 

Requirements must be met with cryptographically strong technologies, providing irrefutable evidence of compliance with regulations. Understanding and properly implementing the required technology to meet HIPAA compliance is a difficult and continually evolving process. 

Entity compliance will be eventually be defined by the best practices of peer entities, an entity&#8217;s intent, and ultimately, decided by the courts. We assert that adopting the best security technologies, as understood by the computer security community, is a first step in the right direction. While it may be possible to achieve compliance without these technologies, systems that implement availability, privacy and confidentiality, and authenticity allow an organization to make a strong statement of compliance and able to provide irrefutable evidence of the same. In the future, were these technologies to become widely deployed as best practices, it may no longer be possible to be compliant without them.

 [1]: http://www.securityevaluators.com/
 [2]: http://www.securityevaluators.com