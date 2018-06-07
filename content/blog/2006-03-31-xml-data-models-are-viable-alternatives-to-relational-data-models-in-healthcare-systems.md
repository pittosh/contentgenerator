---
title: XML data models are viable alternatives to relational data models in healthcare systems
author: Shahid N. Shah
type: post
date: 2006-03-31T12:14:45+00:00
url: /2006/03/31/xml-data-models-are-viable-alternatives-to-relational-data-models-in-healthcare-systems/
oc_commit_id:
  - https://www.healthcareguy.com/2006/03/31/xml-data-models-are-viable-alternatives-to-relational-data-models-in-healthcare-systems/1478769024
views:
  - 3894
dsq_thread_id:
  - 5161846782
categories:
  - Opinion

---
I have received many comments on my recent [Data Models in Healthcare][1] series of articles and all of them have been pretty good. One of the more detailed and thoughtful responses came from Daniel Essin, a physician who is the Director of Medical Informatics at Los Angeles County Hospital and CTO of [ChartWare][2]. He wrote about using XML data models for clinical data management and in general I agree that XML is a viable persistence model for the use case he refers to. Here&#8217;s what Dan said:

> I read your article. It&#8217;s hard to object to your general conclusion although when it comes to the core of healthcare data, the electronic medical record, I have found that sometimes people spend too much time modeling and not enough time following your advice to understand the data and how it will be used.
> 
> The most striking characteristic of clinical documentation is that tends to be composed of nested sections and items. It is extremely common to see data models that attempt to address the content of these documents (i.e. discrete fields for blood pressure, units of measure, etc) while overlooking the natural structure. Indeed at least one commercial system can accept and display almost any discrete data element that you can imagine, but cannot easily present the data originating from a medical encounter as a single, readable document. Alternatively, the structure itself could form the basis of a relational model but doing so would require a deep understating of basic design patterns (such as those in the book by Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides). Very few of the people that I have met that work in healthcare IT are aware of this material.
> 
> After studying this problem for years, I concluded that the information that makes up the medical record is better represented as a simple XML structure based on nested sections rather than by a traditional relational model. I described the fundamentals of this approach in several papers in the early 1990&#8217;s and have had an EMR system that is based on this design in the field for 10+ years in a variety of different settings.
> 
> In medicine, change is ever-present. It comes from outside in the form of new medical knowledge, regulations, treatments, etc. It also comes from inside. As the users gain knowledge and experience, they use existing applications differently and develop different and more demanding expectations. It has been my experience that making major changes to a system based on a relational model, once it has been deployed and used for some time, is a costly proposition, as significant changes in the model may require that the software be modified as well.
> 
> Using an XML approach based on structure, we can accommodate ANY content from ANY specialty and it is all interoperable and viewable as single set of coherent documents. Most importantly, significant changes can be made to the content that is be placed into the pre-defined structure without breaking the most important function – the entire medical record is still viewable and queryable without having to rewrite any applications. Once one becomes comfortable with this level of simplification, it is then trivial (if necessary) to mirror portions of the content in traditional relational tables to facilitate various daily activities and workflow. The latest XML capability in SQL Server, Oracle and DB2 makes the 2-way transition from document to database even easier.
> 
> The XML approach which I pioneered has been taken up by several standards groups and forms the basis for HL7&#8217;s Clinical Document Architecture standard and the Continuity of Care Record initiative.
> 
> There are healthcare people who model (the HL7 organization has developed an extensive OO model), but all too often, people who build healthcare software don&#8217;t pay any attention to the prior art whether it be research or applied work of the type produced by the HL7 group. There is a tendency to use NIH (not invented here) thinking as a reason to ignore the fundamentals of computer science and medical informatics.
> 
> If you are interested, you can find my stuff in Methods of Information in Medicine from 1991 and in several of the IEEE New Security Paradigms workshops from the mid-90&#8217;s. 

Like Dan, I, too, have used XML models for data storage for many years. XML is a great persistence model and I do recommend it when the need is as specific as Dan mentions above; where you should be careful is that XML is not a natural model to do aggregation, consolidation, and analytics from various data sources (which is sometimes a pretty big requirement in modern health IT apps). If you do keep you data in XML format from an applications perspective, be prepared to still do some ETL and EII activities to get it into a more &#8220;analytics-friendly&#8221; format. There are also some modern XML native databases (both open source and commercial) that support querying and aggregation but they are neither popular nor ubiquitious which means tooling support is limited.

I wanted to thank Dan and others who have helped keep this topic of data modeling in healthcare topic alive; it&#8217;s very important. If you are a data modeler and would like to share your thoughts in public, I invite you to publish a guest article on my blog or others.

 [1]: http://www.health-itworld.com/newsitems/2006/march/03-22-06-news-hitw-dynamic-data
 [2]: http://www.chartware.com