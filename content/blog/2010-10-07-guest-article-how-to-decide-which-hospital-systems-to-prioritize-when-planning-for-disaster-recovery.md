---
title: 'Guest Article: How to decide which hospital systems to prioritize when planning for disaster recovery'
author: Shahid N. Shah
type: post
date: 2010-10-07T13:24:06+00:00
url: /2010/10/07/guest-article-how-to-decide-which-hospital-systems-to-prioritize-when-planning-for-disaster-recovery/
oc_commit_id:
  - https://www.healthcareguy.com/2010/10/07/guest-article-how-to-decide-which-hospital-systems-to-prioritize-when-planning-for-disaster-recovery/1478770707
dsq_thread_id:
  - 5168223451
categories:
  - Uncategorized

---
_I recently saw BridgeHead Software&#8217;s [white paper on Healthcare Disaster Recovery][1] and found it quite useful. I invited Charles Mallio, Jr., who is currently Vice President of Business Development for [BridgeHead][2], to give us a summary of their thinking around DR in healthcare. Prior to joining BridgeHead, Charles worked for 12 years at MEDITECH, the last six of which he was responsible for worldwide customer technical support for all MEDITECH platforms. Here&#8217;s what Charles had to say about how to decide which hospital systems to prioritize when planning for disaster recovery:_

For many hospitals, data backup and recovery is a daunting task.  Their data stores are multiplying so quickly that completing a regular backup within the designated window has become a physical impossibility. However, there is light at the end of the tunnel; it is possible to develop a set of best practices for the protection and security of healthcare data and transform the backup nightmare into a workable and cost effective disaster recovery strategy.

An essential step in establishing a workable disaster recovery strategy is to prioritize the backup schedule for each system within the hospital. In order to do this, IT staff should take into consideration two parameters: the RPO, or Recovery Point Objective, and the RTO, or Recovery Time Objective.

RPO, or Recovery Point Objective, describes the acceptable amount of data lag measured in time as defined by the organization.  For example, if a hospital defines a one hour RPO, they have determined that in the event of a disaster, data must be restored to within one hour of the time the disaster occurred.  Another way to state this is “How much data can we afford to have to recreate and/or recapture?”  In this example, the answer is one hour’s worth of data.

RTO, or Recovery Time Objective, describes the duration of time in which systems must be restored to acceptable service levels after a disaster.  For example, if an organization defines a three hour RTO, they have determined that in the event of a disaster, systems must be back up and running, operational and available to end users within three hours of the time the disaster occurred.  Another way to state this is “How long can we afford to be without the system?”  In this example, the answer is three hours.

Typically, a hospital will not have a single RPO and RTO for all of its systems.  Rather, it will prioritize the criticality of systems to determine in which order they must be restored.  This prioritization is a key component of the disaster recovery as well as the overarching business continuity plan.  For example, an organization may deem the HIS its most critical application and assign it the shortest RPO and RTO.  Email may also be deemed a critical application necessary to communication in the event of a disaster, so it may also have a short RTO, but a longer RPO.

The amount and type of data on hand will impact both RPO and RTO and, thus, influence the data protection strategies employed to assure the effective disaster recovery of these systems.  Our emphasis will be on a few key clinical systems common to the majority of healthcare organizations.

**Hospital Information Systems (HIS) and Electronic Health Record (EHR) systems** are dynamic, their databases being frequently updated during the course of a day as patients are cared for.  As such, the expectation is that their RPOs will be short, as will their RTOs.  Given that the size of these systems is relatively manageable, it is not unrealistic to aim for an RPO of one to four hours, the higher end being easier and more economical to achieve.  With a four hour RPO, a full system point-in-time copy of the HIS and EHR must be created six times each day.  Where this once may have meant backing these up to tape every four hours, modern SAN infrastructure, data snapshotting and replication technology make it easier to achieve frequent disk-based systems replicas.

This also allows for quicker RTOs, as disk-based system copies do not have to be restored but are immediately ready for use.  Furthermore, the transportable nature of these copies means a secondary data center can contain complete stand-by systems, which can be made quickly operational from the most recent recovery point.

**Picture Archiving and Communication Systems (PACS) and Document Management and Imaging (DMI) systems** also require short RPOs and RTOs, although the data profile of these systems present some unique challenges.  For example, these systems may contain many TB of digital images.  One cannot quickly create a point-in-time copy of a system this large.  As a result, the RPOs would seem to be much longer, as would the RTOs, as restoring many TB of data is a time-consuming process.

However, the databases that drive PACS and DMI systems, along with their short-term data caches containing recently created data, are not so large and share similar RPO/RTO characteristics as the HIS and EHR systems.  The large quantity of data files these systems reference, the medical and document images, are what present a disaster recovery challenge.  Fortunately, these files are static in nature.  While the meta-data associated with the image may change, the image itself remains constant.  As such, making frequent point-in-time copies of this data constitutes a poor data protection strategy.  Why back up unchanging data night after night, never mind every few hours, when all you are doing is making copy upon copy of the same thing?  There is a better way.

Point-in-time copies of bulk data are useful to recover entire systems of structured data. But for large amounts of unchanging, unstructured data, archiving is a better approach.  By creating a few geographically-dispersed copies of the data on multiple media types, you are best positioned to meet your RPO and RTO for these systems.  For example, in the event of a disaster, your PACS database can be recovered as quickly as your HIS and EHR systems, and then pointed at a secondary copy of the image archive, preferably already extant on storage in a secondary data center.

It is the combination of backup and archiving that can provide an optimal DR strategy.  By understanding the nature of the data in the critical clinical systems, Healthcare IT can deliver both realistic and acceptable RPOs and RTOs to the business.

 [1]: http://www.thehsvcompany.com/HDRWP
 [2]: http://www.bridgeheadsoftware.com/