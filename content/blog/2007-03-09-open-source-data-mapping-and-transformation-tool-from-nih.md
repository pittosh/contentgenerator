---
title: Open Source data mapping and transformation tool from NIH
author: Shahid N. Shah
type: post
date: 2007-03-08T23:12:10+00:00
url: /2007/03/09/open-source-data-mapping-and-transformation-tool-from-nih/
oc_commit_id:
  - https://www.healthcareguy.com/2007/03/09/open-source-data-mapping-and-transformation-tool-from-nih/1478769118
views:
  - 4306
ratings_users:
  - 3
ratings_score:
  - 15
ratings_average:
  - 5
dsq_thread_id:
  - 5161728752
categories:
  - Opinion

---
My friend Jeremy Hulick recently wrote to me about NIH&#8217;s [caAdaptor][1] tool, an open source product he learned about at the recent CaBIG conference. Here&#8217;s how the authors describe it:

> caAdapter is an open source tool set that facilitates data mapping and transformation among different kinds of data sources including HL7 v2 and v3 messages, Study Data Tabulation Model (SDTM) data sets, object models and data models. For HL7 v3 messages, it possesses the capability to perform vocabulary validation by integrating with NCICB caCORE components and provides web service access for easy application integration. caAdapter has a component-based architecture to support message development and reporting using standard data formats. caAdapter also provides the capability to perform vocabulary validation and integrates with NCICB caCORE components. caAdapter has a component-based architecture that offers a tool set to support data mapping and transformation, and standard data reporting. 
> 
> caAdapter Core Components 
> 
>   * CSV to HL7 v3 Mapping and Transformation Service 
>       * caAdapter Web Service 
>           * Model Mapping Service 
>               * SDTM Mapping and Transformation Service 
>                   * HL7 v2 to v3 Conversion Service </ul> </blockquote> 
>                 Jeremy was interested in HL7 2.x to 3.x mapping and he had the following to say about the pros and cons of using caAdaptor to convert an HL7 v2 CSV source file to an HL7 v3 xml file. 
>                 
>                 Pros 
>                 
>                   * Intuitive interface &#8211; easy to upload source files and the layout is easy to interpret 
>                       * Mapping source data to target elements is relatively easy 
>                           * Applying Mapping Functions is easy &#8211; ex. using&nbsp;a concatenate function&nbsp;to combine two source data&nbsp;fields into a single destination element 
>                               * Generating source into multiple formats is easy &#8211; converts to XML, CSV, or a relation data model</ul> 
>                             &nbsp;Cons 
>                             
>                               * Source&nbsp;mapping&nbsp;from HL7 v2 to v3 is manual &#8211; there were no intelligent defaults (perhaps this is the nature of the of the business domain?) 
>                                   * Needs a domain expert to properly convert from v2 to v3 
>                                       * Display&nbsp;of mapped elements does not fit on&nbsp;the screen (minor issue). It is difficult to navigate the links between source and destination elements 
>                                           * Not web enabled &#8211; uses Java Swing </ul> 
>                                         Thanks, Jeremy for sharing your review with us.

 [1]: http://ncicb.nci.nih.gov/NCICB/infrastructure/cacore_overview/caadapter