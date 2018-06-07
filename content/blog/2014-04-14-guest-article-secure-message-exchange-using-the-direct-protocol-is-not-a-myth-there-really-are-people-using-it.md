---
title: 'Guest Article: Secure message exchange using the Direct Protocol is not a myth, there really are people using it'
author: Shahid N. Shah
type: post
date: 2014-04-14T21:44:22+00:00
url: /2014/04/14/guest-article-secure-message-exchange-using-the-direct-protocol-is-not-a-myth-there-really-are-people-using-it/
oc_commit_id:
  - https://www.healthcareguy.com/2014/04/14/guest-article-secure-message-exchange-using-the-direct-protocol-is-not-a-myth-there-really-are-people-using-it/1478770863
  - https://www.healthcareguy.com/guest-article-secure-message-exchange-using-the-direct-protocol-is-not-a-myth-there-really-are-people-using-it/1420181239
dsq_thread_id:
  - 5203174480
oc_metadata:
  - |
    {		version:'1.1',		tags: {'rachel-a-lunsford': {"text":"Rachel A. Lunsford","slug":"rachel-a-lunsford","source":{"_className":"Entity","url":"http://d.opencalais.com/pershash-1/5576df95-c9ec-39a6-b6a7-e0858bdc52ba","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/em/e/Person","name":"Person"},"name":"Rachel A. Lunsford","rawRelevance":0.628,"normalizedRelevance":0.628},"bucketName":"blacklisted","bucketPlacement":"user","_className":"Tag"}, 'director-of-product-management': {"text":"Director of Product Management","slug":"director-of-product-management","source":{"_className":"Entity","url":"http://d.opencalais.com/genericHasher-1/6634353b-2391-3d40-ae03-fc3f904a1210","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/em/e/Position","name":"Position"},"name":"Director of Product Management","rawRelevance":0.316,"normalizedRelevance":0.316},"bucketName":"blacklisted","bucketPlacement":"user","_className":"Tag"}, 'healthcare-organizations': {"text":"Healthcare Organizations","slug":"healthcare-organizations","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'secure-messaging': {"text":"Secure Messaging","slug":"secure-messaging","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'direct-messaging': {"text":"Direct Messaging","slug":"direct-messaging","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'health-information': {"text":"Health Information","slug":"health-information","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'health-information-exchange': {"text":"Health Information Exchange","slug":"health-information-exchange","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'direct-project': {"text":"Direct Project","slug":"direct-project","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'medical-informatics': {"text":"Medical informatics","slug":"medical-informatics","source":{"url":"http://d.opencalais.com/dochash-1/3bb3f0ea-34f7-3fc2-954d-4dc9791103fe/SocialTag/4","subjectURL":null,"type":{"url":"http://s.opencalais.com/1/type/tag/SocialTag","name":"SocialTag","_className":"ArtifactType"},"name":"Medical informatics","makeMeATag":true,"importance":1,"_className":"SocialTag","normalizedRelevance":1},"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}}	}
categories:
  - Events
  - Implementation
  - Information Assurance (IA) and Security
  - Meaningful Use
tags:
  - Direct Messaging
  - Direct Project
  - Health Information
  - Health Information Exchange
  - Healthcare Organizations
  - Medical Informatics
  - Secure Messaging

---
<i style="line-height: 1.5em;">I recently chaired a couple of conferences and my next <a href="https://www.imn.org/health-impact/conference/Health-Impact-East/Home.html">HealthIMPACT</a> event is coming up <a href="https://www.imn.org/health-impact/conference/Health-Impact-East/Home.html">later this month in NYC</a>. At each one of the events and many times a year via twitter and e-mail I am asked whether the <a href="http://directproject.org/">Direct Project</a> is successful, worth implementing in health IT projects, and if there are many people sending secure messages using Direct. To help answer these questions, I reached out to Rachel A. Lunsford, Director of Product Management at <a href="http://amida-tech.com/">Amida Technologies</a>. Amida has amassed an impressive team of engineers to focus on health IT for patient-centered care so their answer will be well grounded in facts. Here’s what Rachel said when I asked whether Direct is a myth or if it’s real and in use:</i>

Despite wide adoption in 44 States, there is a perception that Direct is not widely used. In a recent conversation, we discussed a potential Direct secure messaging implementation with a client when they expressed concern about being a rare adopter of Direct messaging.  While the team reassured them that their organization would in fact be joining a rich ecosystem of adopters, they still asked us to survey the market.

In 2012, the Officer of the National Coordinator for Health Information Technology (ONC) awarded grants to State Health Information Exchanges to further the exchange of health information. There are two primary ways to exchange information: directed and query-based. ‘Directed’ exchange is what it sounds like – healthcare providers can send secure messages with health information attached to other healthcare providers that they know and trust. The most common type of ‘Directed’ exchange is Direct which is a secure, scalable, standards-based way to send messages. Query-based is a federated database or central repository approach to information exchange which is much harder to implement and growth in this area is slower.  Thanks in part to the grants and also in part to the simplicity of the Direct protocol, 44 States have adopted Direct and widely implemented it. And yet the myth persists that Direct is not well adopted or used.

As with other new technologies, it may be hard to see the practical applications. When Edison and Tesla were dueling to find out which standard – direct or alternating current – would reign supreme, many were unsure if electricity would even be safe enough, never mind successful enough, to replace kerosene in the street lamps. It was impossible for people to foresee a world where many live in well-lit homes on well-lit streets, and none could have imagined using tools like the computer or the Internet. Thankfully, the standards debate was sorted out and we continue to benefit from it today.

There are two groupings of data we can look towards for more detail on use of Direct. The first are the States themselves; they self-report transaction and usage statistics to the ONC. It was [reported][1] in the third quarter of 2013 that the following were actively exchanging some 165 million ‘Directed’ messages:

  * 20,376 Ambulatory entities (Entities/organizations that provide outpatient services, including community health centers, independent and group practice, cancer treatment centers, dialysis centers, etc.)
  * 738 Acute Care Hospitals (Hospitals that provider inpatient medical care and other related services for surgery, acute medical conditions or injuries)
  * 157 Laboratories (Non-hospital clinical)
  * 16,329 other health care organizations (Home health care, long-term care, behavioral health programs/entities, psychiatric hospitals, payers, release of information vendors, health care billing services, etc.)

Another organization collecting data on Direct implementation is [DirectTrust.org][2]. [Charged by ONC][3], DirectTrust.org oversees development of the interoperability framework and rules used by Direct implementers, works to reduce implementation costs, and remove barriers to implementation. Additionally, DirectTrust supports those who want to serve as sending and receiving gateways known as health information service providers (HISPs). By DirectTrust.org’s count, the users number well over 45,000 with at least 16 organizations accredited as HISPs. Further, over two million messages have been exchanged with the roughly 1,500 Direct-enabled sites. With Meaningful Use encouraging the use of Direct, we can expect even more physicians and healthcare organizations to join in.

As more doctors are able to exchange records, everyone will benefit. When a provider can receive notes and records from other providers to see a fuller, more complete view of her patient’s health, we have a greater possibility of lowering healthcare costs, improving health outcomes, and saving lives.  Once we open up the exchange to patients through things like the [Blue Button personal health record][4], the sky is the limit.

&nbsp;

&nbsp;

 [1]: http://healthit.gov/policy-researchers-implementers/active-directed-exchange-organization-type
 [2]: http://www.directtrust.org/
 [3]: http://healthit.gov/policy-researchers-implementers/exemplar-hie-governance-entities-program
 [4]: http://www.va.gov/bluebutton/