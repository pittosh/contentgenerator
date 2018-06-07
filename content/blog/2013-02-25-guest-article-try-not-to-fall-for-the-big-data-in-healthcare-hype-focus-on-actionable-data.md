---
title: 'Guest Article: Try not to fall for the Big Data in Healthcare hype, focus on actionable data that can improve clinical workflows'
author: Shahid N. Shah
type: post
date: 2013-02-25T14:39:16+00:00
url: /2013/02/25/guest-article-try-not-to-fall-for-the-big-data-in-healthcare-hype-focus-on-actionable-data/
oc_commit_id:
  - https://www.healthcareguy.com/2013/02/25/guest-article-try-not-to-fall-for-the-big-data-in-healthcare-hype-focus-on-actionable-data/1478770822
dsq_thread_id:
  - 1104169006
categories:
  - Uncategorized

---
_Many readers write to me regularly to ask what I think about “Big Data” in healthcare. I tell them that Big Data in our field is generally more hype than reality right now but that there’s a lot of promise and opportunity. To help elaborate on why this might be the case I’ve asked my friend Naeem Hashmi, Chief Research Officer at <a href="http://infoframeworks.com/" target="_blank">Information Frameworks</a>, to give us his thoughts. Naeem has written a number of books on the subject of informatics and analytics and been on the front lines of engineering large scale healthcare systems to generate data for clinical analytical purposes. Here’s what Naeem had to say about Big Data in Healthcare:_

The Big Data bubble in the Healthcare is just filled with the Hot Air &#8211; at least for now. Every one is talking about it but when you dig a bit deep with a pointed question, very quickly you discover that it has nothing much to do with the Big Data. We need to understand the spectrum of healthcare segments and look at each segment on feasibility of Big Data components.

I identify the following six distinct healthcare segments as:

  1. Life Sciences 
  2. Pharma 
  3. Med Device Manufacturers 
  4. Care Provider 
  5. Payers 
  6. Public Health 

I did not include Patients in the list as they are mostly content generators, consumers and have much to benefit from but they are on the mercy of other segments. Life Sciences and Pharma segments are already exploiting Big Data elements for OMICs in discovering new drugs and therapies and will discuss details in the later sections.

In this article, I will focus on realities of the Big Data in the **_Care Providers segments_** only.

To frame the discussion, let me describe what I mean by Big Data. The Big data consists of the following elements:

  * **Content Attributes**: 4 Vs (Volume, Variety, Velocity, Veracity) &#8211; widely known. 
  * **Technology Stack**: Hadoop-like stacks and Analytics Appliances 
  * **Computing Model**: Extremely Reliable Parallelism 
  * **Query Model**: Hadoop/Map-Reduce use search method (not complex query). So if the intent is to do searches against large unstructured content, the pure Hadoop/map-reduce functions are good fit. Not SQL. 
  * **Connecting the Dots**: Understanding the associative meanings of the interesting patterns hidden underneath massive content-stores. 

**<u>Care Providers:</u>**

The Healthcare Provider segment is extremely fragmented. With ongoing Healthcare reforms, there is some hope that use of EHRs may result in some meaningful use of clinical content. Most of the CIOs are too busy in addressing ICD-10 and CMS Meaningful Use 2 mandates and very few have the time or energy to invest in true Big Data platforms. Data management still remains on the Legacy platforms. So how /where does Big Data fit in the Care Providers segment and challenges?

****

**Data Jail**

EHR vendors have a lock on patient clinical content in their own proprietary &#8216;Data Jails&#8217;. In my many years as a practitioner I have found it quite difficult to access clinical content and analyze it within these proprietary systems so the Volume and Velocity needed for Big Data is not easy to obtain.

I am using the term &#8216;Data Jail&#8217; because it takes me back to the early 90&#8217;s, when &#8216;data jail&#8217; term was widely used for the ERP vendors. Then, IT folks had hard time to pull data out of ERPs for reporting and analytics. Today, ERP vendors are quite open and allow accesses to the data. EHR vendors need to learn lessons from ERPs for openness, interoperability and scalability. Opening access to their repositories is good for their customers and for Big Data.

**Complexity, Low Volumes and Static Data**

****

Most clinical data volumes are quite low and static because you cannot change any historical data in a clinical record. Even though you may append a new record, the rate of change is fairly low unless you’re talking about genetic or proteomic data (which is rare in most settings). Moreover, Clinical content is quite complex. Here content context and semantics are more important than the volume and velocity so you can live with standard relational databases or analytics appliances without the Big Data tools like Hadoop.

****

**Real-Time Patient Monitoring**

Real-time patient monitoring applications such as bedside heart monitors, OR monitors for anesthesia, dialysis patient monitors, etc. are being piloted in care facilities that demand use of Big Data platform to quickly consume real-time events and signal possible life threatening adverse events before occurring. Increasing use of mobile personal health monitoring devices that stream data back to the care providers also require Big Data elements to capture and predict possible health issues and alarm the care takers and patient for actions. Good candidate for Big Data driven applications.

**ACO Level Analytics**

ACO level data volumes will be quite high and Big Data will play a key role to develop analytics. The challenge will be how to pull detailed clinical EHRs for the ACO and then to harmonize content in the ACO hub to ensure content quality. Lack of data exchange standards in practical use remains a problem. Even when vendors conform to patient data exchange standard, such as CCD, the actual implementation varies significantly and makes harmonization difficult. For example, Continuity of Care Document (CCD) implementation of two vendors could result in different patient clinical content. That’s because one vendor could provide latitudinal CCD while the other provided encounter specific CCD. Both conform to the CCD specs but payload was different. Here, for the ACO Big Data repository, you need to build a high performance harmonization engine to ensure content consistency before you embark on Analytics.

**Valuing Big Data**

After going through pain of Big Data implementations, the end goal should remain how to bring valuable insight back in the clinical processes &#8211; embedded within the clinical workflows. Most people think that just displaying charts and graphs on a stand-alone dashboard will do the job but of course that’s not the case. Physicians and clinicians do not have time to hop through many screens to care their patients. We need to embed such findings within the clinical work-flows so they have the right alert at the right time for the right patient. You may be stuck with an EHR&#8217;s limitations on how open they are so you may not be able to embed non-EHR event with their clinical workflows or work-lists.

**Emerging Big Data Opportunity &#8211; Comparative Effectiveness Research**

As social animals humans they socialize and chat about their daily life stories including dealing with their health issues, families, care givers, behaviors and medications. Such social communication is a gold mine to Pharma and Clinical Outcome researchers to understand effectiveness of a specific therapy. This new field is called the Comparative Effectiveness Research (CER) and Patient Centered Outcomes Research (PCOR). Through the use of Big Data analytics, CER will significantly improve patient care through development of personalized therapies.

**Emerging Big Data Clinical Analytics providers**

Last year, I served as a judge for the Massachusetts First Health Datapalooza competition. Several Big Data driven clinical applications were part of this competition. I had good discussions with a few vendors. Though their solutions are unique and valuable, none have thought well on how their solution will fit in the clinical setting, client EHR workflows or leverage client&#8217;s clinical platform. Just about all Big Data analytics providers are start-ups coming up with innovative care solutions.

When I see in the Big Data market place, it reminds me of &#8216;dot com&#8217; era of the early 90&#8217;s. Lot of small innovative groups developing fascinating tools just like todays in the Healthcare world and unfortunately, a few will survive. My suggestion to such innovators is to keep in mind to develop their Big Data solution are interoperable with the EHRs or ACO business/clinical applications.

**Closing thoughts**

Big Data in the Clinical practice is just in its evolutionary stages. Most CIOs may be thinking about Big Data but to best of my knowledge I have not seen a pure Big Data implementation in any hospital or clinical practice. Only a handful of large global network of commercial Clinics have implemented such Big Data platforms in production.

Building a Big Data platform and having a team of skilled data scientists in a Hospital or Practice setting is not easy. It is Expensive as well. You will notice that today, only University Hospitals are starting to explore Big Data in the healthcare setting because of funded academic research programs and available pool of graduate students ready to investigate unexplored content. Same is true for the small start-ups companies to develop key healthcare analytics using the social data for public health and patient engagement applications. Today we are just taking baby steps &#8212; and we have a long road ahead of us to exploit the true value of Big Data in clinical settings.

Any thoughts or comments?