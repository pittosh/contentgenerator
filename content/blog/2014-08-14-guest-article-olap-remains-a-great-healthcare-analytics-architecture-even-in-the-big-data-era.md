---
title: 'Guest Article: OLAP remains a great healthcare analytics architecture, even in the Big Data era'
author: Shahid N. Shah
type: post
date: 2014-08-14T08:29:54+00:00
url: /2014/08/14/guest-article-olap-remains-a-great-healthcare-analytics-architecture-even-in-the-big-data-era/
oc_commit_id:
  - https://www.healthcareguy.com/2014/08/14/guest-article-olap-remains-a-great-healthcare-analytics-architecture-even-in-the-big-data-era/1478770886
  - https://www.healthcareguy.com/guest-article-olap-remains-a-great-healthcare-analytics-architecture-even-in-the-big-data-era/1420536594
oc_metadata:
  - |
    {		version:'1.1',		tags: {'olap': {"text":"OLAP","slug":"olap","source":{"_className":"Entity","url":"http://d.opencalais.com/genericHasher-1/e5e82d58-5d58-35dd-8fa6-5c3943e34bb2","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/em/e/Technology","name":"Technology"},"name":"OLAP","rawRelevance":0.77,"normalizedRelevance":0.77},"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'ehr': {"text":"EHR","slug":"ehr","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'big-data-tools': {"text":"Big Data Tools","slug":"big-data-tools","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'data-management': {"text":"Data Management","slug":"data-management","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'health-informatics': {"text":"Health Informatics","slug":"health-informatics","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'healthcare-data-infrastructure': {"text":"Healthcare Data Infrastructure","slug":"healthcare-data-infrastructure","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'online-analytical-processing': {"text":"Online Analytical Processing","slug":"online-analytical-processing","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}}	}
dsq_thread_id:
  - 5160396972
categories:
  - Cloud Computing
  - Telehealth
  - Telemedicine
tags:
  - Big Data Tools
  - Data Management
  - EHR
  - Health Informatics
  - Healthcare Data Infrastructure
  - OLAP
  - Online Analytical Processing

---
_I&#8217;ve been getting many questions these days about big data tools and solutions, especially their role in healthcare analytics. I think that unless you&#8217;re doing large scale analysis of biomedical data such as genomics, it&#8217;s probably best to stick with traditional tried and true analytics tools. Online Analytics Processing (OLAP) can be invaluable for medical facilities to use when interpreting data and health informatics because most of that data is in relational, key-value, or hiearchical databases (such as MUMPS). I reached out to Ron Vatalaro, who works with the [University of South Florida Morsani College of Medicine][1] and writes about health informatics, to summarize which commercial tools are good to consider for modern OLAP architectures. Here&#8217;s what he said:_

Online Analytic Processing (OLAP) is used in computing to quickly respond to multi-dimensional analytical queries. It is a subset of business intelligence, which also includes report writing, relational database, and data mining. OLAP tools make it easy to analyze data from multiple perspectives through one of its following three basic operations: consolidation (roll-up), drill-down, and slicing and dicing.

OLAP and data warehousing are interacting with and shaping health informatics by allowing for [new analytical opportunities][2], in addition to the customary statistical approaches. It is one thing to collect vast amounts of data, but gaining insights as to how to best use the data to save lives and dollars is where the rubber meets the road. It is up to informatics professionals to glean meaningful information from the data sets and OLAP tools make it easier to breakdown and analyze big data.

Clinicians and [hospital administrators][3] can analyze the data for both individual patient care and to make optimized decisions to better serve all patients undergoing treatment at the facility. Dimension tables can be vital to testing hypothesis using textual, non-numerical data. For instance if administrators what to determine if the colors of walls or views from the window in patient’s rooms correlate to stay durations, nurse calls or return rates &#8211; these tools can assist in drawing such conclusions.

**EHR and OLAP**

EHR and OLAP work hand-in-hand to deliver across-the-board improvements in world-wide health reform. It is important to understand the role data plays in the healthcare business model, and in what ways EHR systems are capturing and relaying this data. When it comes to the massive amounts of information coming into the healthcare data infrastructure, the use of comprehensive analysis becomes invaluable. Thus when the output from EHRs can be meaningfully dissected the results can lead to the following benefits: better continuity of care, increased patient participation, enhanced practice efficiencies/cost savings, better accuracy, reduction of errors and more convenience for patients and healthcare providers.

The story your data is telling can present a double-edged sword. One of the benefits of being able to slice-and-dice down [big data][4] is to root out inefficacies; however, these same inefficiencies can lead to loss income due to meaningful use and pay-for-performance (P4P) policies. That being said, it is important to have comprehensive analytics to track and root out potential problems proactively, and to know what data third parties, such as insurers, are also looking at.

There is also the data healthcare providers cannot control, for instance, the decisions among patients to maintain their own health and well-being. There are government and insurance provider-backed incentives that reward “good behavior” among individuals who prioritize their health (not to mention the benefits of a healthy lifestyle). Categorizing and engaging individuals who do not care to advocate for their own benefit through unhealthy behaviors, (such as poor diet, alcohol abuse or tobacco use) and identifying any external factors that may exacerbate these issues (such and geographic, ethnic or socio-economic) can enrich lives and benefit the overall environment of healthcare. In these circumstances [EHR][5] and OLAP work together to the mutual benefit of society and the healthcare industry.

**OLAP and Pharmacy Systems**

To aid in pharmacological data management OLAP can play a major role in using the vast amounts of information from managed care organizations (MCO) management information systems (MIS) in a meaningful way. Information regarding member/provider functions, claims administration, clinical management, rebate administration and financial details are managed by systems generally referred to as online transaction processing systems (OLTP). Such systems have allowed the collection of billions of prescription records year-over-year. However, with the need for massive amounts of data to enable more effective drug therapy treatments, pharmacy management systems can fall short of the necessary processing power. That’s where OLAP systems step in to make decision support tools from the OLTP systems. These tools can interact with the data by making changes to the OLTP system, extracting data from the patient population and the prescribers of the medication.

**OLAP Iterations**

OLAP systems are classified by the following groupings:

  * **Multi-dimensional (MOLAP):** Known as the classic form of OLAP, this iteration is often denoted as simply OLAP. Instead of storing data in a relational database, MOLAP uses optimized multi-dimensional array storage. It relies on pre-computation and storage of information in the cube. Tools typically employ a pre-calculated data cube, including all possible responses to a certain range of questions. These tools have a very quick response time and can quickly write back data into the data set. They are useful for data sources that are static, therefore more useful for analyzing information from medical devices, since they operate on pre-determined parameters and are subject to less variability. It also works well for data that is more latent, or less frequently processed.
  * **Relational (ROLAP):** In this iteration, base data and dimension tables are stored as relational tables and new tables are generated to store the aggregated information. It relies on a specialized schema design that manipulates the data stored in the relational database to make it appear to have traditional OLAP functionality. Rather than using pre-calculated data, tools pose the query to the standard ROLAP database and its tables to bring the necessary data back to answer the question. As this methodology is not limited to the contents of a cube, tools have the functionality to ask any question. This type of analysis is good for information that is dynamic or frequently changing using its star scheme. Therefore, this type of analytic processing is good for information such as patient data, which has many variables and is subject to frequent changes and fluctuations.
  * **Hybrid (HOLAP):** The hybrid iteration is somewhat of a broad term, with a number of different interpretations, but all agree that a database will separate data between specialized and relational storage. HOLAP combines the capabilities of MOLAP and ROLAP to address their weaknesses. Tools can also use relational data sources and pre-calculated cubes. HOLAP tools can help to understand how patients and devices interact together, especially over time.

**5 OLAP Tools Strengths and Weaknesses** 

There are a wide-variety of data management tools available to assist healthcare organizations in online analytics processing. There are

  * **Microsoft:** The company’s Microsoft Analysis Services support MOLAP, ROLAP and HOLAP. However, it can only run on a Windows operating system, so organizations using Linux, UNIX, or z/OS won’t be able to use it.One of the benefits to healthcare professionals using the system is that it integrates well with widely used software, such as Excel, that may be more comfortable to use among those with more of a healthcare background than a technical background.
  * **Oracle:** Oracle offers two OLAP servers ─ Essbase and Oracle Database OLAP Option. In addition to supporting MOLAP, ROLAP and HOLAP, they also support semi-additive measures, write-back, and partitioning. Oracle Database OLAP Option is compatible with Windows, Linux, UNIX, and z/OS, but Essbase cannot run on z/OS. Oracle offers the Service-oriented architecture (SOA) as a part of its data analytics service, which is specifically designed for healthcare integration.
  * **IBM:** Cognos TM1 is IBM’s OLAP server. While IBM Cognos offers MOLAP, ROLAP, and HOLAP data storage modes, IBM TM1 only offers MOLAP storage. TM1 is compatible with Windows, Linux, and UNIX, but not z/OS. IBM offers an assortment of assistance tools for healthcare data such as DB2 Intelligent Miner, industry specific guides, along with third party support form Blue Line.
  * **SAP:** The SAP NetWeaver BW is the SAP OLAP server. Semi-additive measures, write-back, and portioning features are supported, but only MOLAP and ROLAP storage modes are offered. SAP offers support tutorials for using their NetWeaver tools for health insurance claim eligibility and health checks such as cholesterol levels.
  * **MicroStrategy:** The MicroStrategy Intelligence Server offers MOLAP, ROLAP, and HOLAP data storage modes, in addition to MicroStrategy Office and Dynamic Dashboards offline capabilities. It is compatible with Windows, Linux, and UNIX, but not z/OS. MicroStrategy is positioning itself as the go-to platform for healthcare business intelligence, leveraging its mobile capabilities as an asset.

**How OLAP fits with ‘Big Data’ Hype**

As Shahid mentioned in his introduction, there has been a growing buzz around Big Data in IT (generally). Due to the massive influx of consumer information being shared openly over a variety of platforms, there has been a great deal of demand among businesses to capture that information to try and gain market insights and create customer profiles. This flood of information has many implications in healthcare, as tele-health and interoperability are gaining prominence. However, data quality is not the same a data quantity, and quantity (as the name suggests) is essentially what Big Data is all about.

Being able to capture standardized and actionable insights from large sets of data is the important distinction that OLAP brings to the table. Without the insights that structured data can bring, what you are left with is merely a technology (Big Data), rather than architecture (OLAP). That being said, there are differing schools of thought as to what role OLAP will play in the future of data management. It can be said that OLAP cubes lack the agility that a Big Data solution offers, although the presence of one does not mutually exclude the other.

 [1]: http://www.usfhealthonline.com/
 [2]: https://www.healthcareguy.com/2013/04/13/guest-article-crawl-walk-and-then-run-towards-analytics-and-big-data-in-healthcare/
 [3]: https://www.healthcareguy.com/2011/10/30/guest-article-policy-management-software-for-hospitals-and-clinics-helps-with-change-management/
 [4]: https://www.healthcareguy.com/2014/02/17/keeping-medical-device-designs-relevant-in-a-big-data-world-migrating-to-outcomes-driven-payment-models/
 [5]: http://www.usfhealthonline.com/resources/healthcare/5-ways-ehrs-are-transforming-healthcare/