---
title: 'The Looming Problem in Healthcare EDI: ICD-10 and HIPAA 5010 migration'
author: Shahid N. Shah
type: post
date: 2009-10-10T16:26:40+00:00
url: /2009/10/10/the-looming-problem-in-healthcare-edi-icd-10-and-hipaa-5010-migration/
oc_commit_id:
  - https://www.healthcareguy.com/2009/10/10/the-looming-problem-in-healthcare-edi-icd-10-and-hipaa-5010-migration/1478770513
ratings_users:
  - 2
ratings_score:
  - 9
ratings_average:
  - 4.5
dsq_thread_id:
  - 44284099
categories:
  - Opinion

---
On Jan. 15, 2009 the United States Department of Health and Human Services released the [final rules][1] for the updated X12 Electronic Data Interchange (EDI) transaction definitions, version 005010 to be used in conjunction with HIPAA and completed by January 2013. At the same time, the International Classification of Diseases (ICD) standard has been bumped from ICD-9 to ICD-10 with a compliance date of October 2013. These aggressive compliance mandates, coupled with the close relationship between HIPAA transaction sets that can directly refer to ICD-9 or ICD-10 codes have health industry IT professionals scrambling. A huge fiscal burden has been placed on payers and providers as they look to redesign business processes and systems to handle hundreds of thousands of new codes at an estimated cost of more than $14 billion.

From the viewpoint of the people who use the data, there are many good reasons for this change. HIPAA 4010 and 5010 compliance has taught us a lot about who needs what data and when. However, the actual changes to the data format are more of the evolutionary and not revolutionary type.

The ICD-9 to ICD-10 change is truly a radical step:

  * It&#8217;s been 30 years since the ICD-9 list was first developed. ICD-9 is embedded much deeper into systems. The 36 years from 1977 to 2013 means that a junior programmer who wrote ICD-9-related code at the start of his career is probably now the CTO facing the consequences of a change he never planned for. 
  * The list for ICD-10 is far more detailed, at almost 10× the length. The numbering system has changed, the number of diagnostic codes increased, individual codes are more detailed. 
  * There are generally no 1:1 mappings between ICD-9 and ICD-10. Although some codes in the old classification map directly to codes in the new, most don&#8217;t. Sometimes there are a series of codes, sometimes there are alternatives that will take external information to choose from, and sometimes there are no direct alternatives. 

There are several challenges for those working with these standards, and since the “HI” segment of several HIPAA transaction sets can directly refer to ICD-9 or ICD-10 codes, these problems actually intersect. How can we account for the changes when data has been moved, or where new data must be extracted from other sources to augment the existing feed?

The hardest part about writing a book is that first sentence. It is similar with data conversion projects. When there is so much to convert, where do you begin? Transforming data in HIPAA 4010 X12 files and translating ICD-9 codes has been covered by blogs like [XML Connections][2]. Now, software developers and architects can consult the [HIPAA/ICD Upgrade Toolkit][3], created by the XML and data integration experts at [Progress DataDirect][4]. The kit includes the following information:

  * XQuery source for upgrading each of the 10 transaction sets from the 4010 version to the equivalent 5010 version
  * 50 sample 4010 files to use with the above
  * The ICD-9 to ICD-10 maps
  * A sample tool to compare the changes between ICD-9 codes and their closest ICD-10 analogs, with HTML output
  * An XQuery program which will read a HIPAA file containing ICD-9 codes and report on any potential conversion troubles with ICD-10 
  * An XQuery program to read a HIPAA EDI file, and convert it from 4010 to 5010 and from ICD-9 to ICD-10 simultaneously 

What does XQuery have to do with HIPAA? Well, EDI to XML converter technologies make EDI behave like XML. And XQuery is really good at augmenting, splitting and rearranging XML. The two together let a relatively small XQuery program do big things. The XQuery programs including in the HIPAA/ICD Upgrade Toolkit are sufficient to convert all of the samples that come with the 4010 documentation into valid 5010 files.

Your mileage may vary, but the examples available in the HIPAA/ICD Upgrade Toolkit provide a good starting point. No doubt your specific application will need some tweaking, but isn&#8217;t it a whole lot easier to change a working program than to start from scratch?

 [1]: http://edocket.access.gpo.gov/2009/pdf/E9-740.pdf
 [2]: http://blogs.datadirect.com/category/xml-connections
 [3]: http://www.datadirect.com/downloads/main-registration-form/mainregform/index.ssp?&atc=DDT_Demo_HCToolkit
 [4]: http://www.datadirect.com/