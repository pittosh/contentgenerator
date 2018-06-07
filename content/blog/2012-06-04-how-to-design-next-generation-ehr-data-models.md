---
title: How to design next-generation EHR data models
author: Shahid N. Shah
type: post
date: 2012-06-04T14:20:46+00:00
url: /2012/06/04/how-to-design-next-generation-ehr-data-models/
oc_commit_id:
  - https://www.healthcareguy.com/2012/06/04/how-to-design-next-generation-ehr-data-models/1478770797
dsq_thread_id:
  - 5166915554
categories:
  - Cloud Computing
  - EHR
  - Engineering
  - Meaningful Use
  - Patient Self-Management

---
Today’s reality of patient management is “disjointed care” and most of the collaborators in a patient’s care team don’t know what each other is doing for the patient in real time. Knowing all the different participants in the patient’s care team (providers, payers, family members, etc.) and coordinating and integrating their electronic activities is what successful EHRs must handle with ease as they look to graduate from basic retrospective documentation systems to modern patient collaboration platforms. Current EHR apps are usually restricted to “legal entities” (e.g. a single hospital or a hospital system or single ambulatory practice). To manage integrated and coordinated care, successful EHR systems must open themselves up beyond legal boundaries but most of them have created their databases and data models to preclude that capability.

Most existing EHRs, even modern ones that were built for Meaningful Use, have traditionally done a poor job understanding and designing “multi-entity” or “multi-tenant” database models that would encourage secure, trusted, electronic collaboration between legal organizations (e.g. two hospitals or multiple clinics) and patients as they move across entities.

This is due not to the lack of availability of good design patterns but a lack of comprehension that tomorrow’s shared savings initiatives, capitated payment models, ACOs, and PCHMs require a level of coordination and amount of measurements of quality metrics that are tough to define, implement, and secure. Future EHRs cannot be seen as applications alone but as broad care coordination platforms that must allow dynamic business models that can accommodate a great deal of uncertainty and flexibility, especially with respect to legal boundaries. When you move from the certainty of supporting users inside a single organization to working with the uncertainty of multi-organization relationships and user communities, application architectures and data models must accommodate more fluid workflows that can change potentially daily or weekly based on the demands of new participants.

The healthcare IT applications development community needs to learn that data modeling is not just a technical exercise – that’s what leads to bad designs that don’t incorporate next generation business models. You can&#8217;t define a data model with a bunch of engineers and other geeks sitting around a table. Data modeling is about understanding all of the uses of the data, the relationships and attributes involved in the data, and, most importantly, how the data management approach will grow and change in the future. It&#8217;s the last part (extensibility of the database) that developers often forget when designing most systems. All this involves direct communication with end users, stakeholders, and other non-technical personnel. Too often, databases are treated as a file cabinet—just let your application toss whatever is necessary in there and then deal with organizing it later. But in the emerging world of ACOs and PCMH that won’t be possible.

Here are the <a href="http://www.ibm.com/developerworks/industry/library/ind-ehr/index.html" target="_blank">kinds of attributes that next generation EHR data models must support</a>:

  * Flexible patient-centric “person” models. Modern and extensible databases model patient (consumer), physician, nurse, staff member, administrator, contact, insurance policy holders, and related data as Person records. Instead of having a separate table for each type of person (for example, a different table for a patient versus a physician), you should try to model the different person types in a single inheritable and related table.
  * Flexible multi-facility “organization” models. The same goes for organizations. Facilities, tenants, hospitals, insurance providers, departments, clinics, administration, and related data should be grouped into something conceptually called an organization. Any entity that isn&#8217;t a Person type will likely fall into the Organization record type category—a single table with appropriate attributes should work fine.
  * Support for robust patient identification and de-duplication. When working in a multi-entity legal framework, there won’t be a single patient identifier to rule all the systems. Good data models allow an unlimited number of mappable identifiers for any entity—a primary key for internal consistency plus any number of external identifiers. Every Person record should allow an extensible set of identification values to use for both ID lookups and de-duplication requirements that crop up when integrating multiple systems.
  * Support for separation of PHI from clinical and transactional attributes. A good design is to put PHI data into one database (configured with proper security), and put the clinical, business, and other attributes into another database.
  * Support for multiple simultaneous entity roles. Each entity in the database, such as person or organization, should be able to support multiple entity roles. We have already described that a Person record should be created in a common table for patients, physicians, nurses, and so on, and why that makes sense. However, think about the scenario where a nurse at a hospital may also be a patient in the same hospital. Instead of duplicating records, the same record could take on dual roles; in this case as both a nurse and a patient.
  * Support for long-term storage and change management (revision control) of all entity attributes. When data lives for a long time, it can change. Extensible databases support long-term storage, change management of the database structures, and revision control of the data (records).
  * Support for multiple applications and devices within the same structures. When creating a database always assume that multiple applications will write to the same database. This means that for every record written you should trackwhich application wrote or changed the record and perhaps on which device.