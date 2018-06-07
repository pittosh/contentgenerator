---
title: 'Guest Article: Top 5 PACS interconnectivity and interoperability issues and their solutions'
author: Shahid N. Shah
type: post
date: 2012-06-22T10:43:16+00:00
url: /2012/06/22/guest-article-top-5-pacs-interconnectivity-and-interoperability-issues-and-their-solutions/
oc_commit_id:
  - https://www.healthcareguy.com/2012/06/22/guest-article-top-5-pacs-interconnectivity-and-interoperability-issues-and-their-solutions/1478770801
dsq_thread_id:
  - 5197137869
categories:
  - DICOM
  - Engineering
  - PACS
tags:
  - DICOM
  - Interoperability
  - PACS

---
_Most health IT interoperability and connectivity discussions these days center around HL7, CCD, and other structured data interchange. However, the vast majority of data (in terms of size) is shared as images and documents. The DICOM and PACS standards are very successful but given the number of questions I get about them from readers it seems there’s still a lot of guidance and support needed. To help&#160; answer some of the most common technical questions, I reached out to a fellow health IT expert, Herman Oosterwijk from_ [_OTech_][1]_. Herman has been working in DICOM and PACS for a while and wanted to share with us his Top 5 PACS interoperability issues and answer questions that you may have. Here’s what Herman had to say:_

When teaching our PACS/DICOM classes, I always take note of the most common interoperability issues brought up by the students. The same is true when I visit an institution, I like to know what is going on in the field, and so I can subsequently talk about it (and write such as in this column). Especially when facing with upgrades and changes of a PACS system, it is important to be able to recognize these symptoms and take appropriate action.

It is commonly known that PACS system components are still not “plug and play”. Especially additions such as new modalities, as well as software changes and upgrades often pose issues which might cause disruptions, lesser functionality, and in some cases even impact patient care. Many of these issues could have been avoided or minimized by a more thorough validation by the vendors, acceptance testing and verification by the hospitals. 

Here are the top 5 PACS interconnectivity and interoperability issues:

**1. Network Issues:** 

A well defined and managed network infrastructure is essential. Dynamic IP addressing is fine as long as the router does not re-assign them to a different address, e.g. when being re-booted or replaced. A rather frequent occurrence is the incorrect setting of the switch, e.g. to half duplex or mismatching the device setting, especially when auto-negotiating is configured. Switch issues result in major performance issues and can only be made visible when using a network sniffer. Combined with “netscan” utilities to detect any IP addressing issues, these are essential tools to deal with these issues.

**2. DICOM Header Issues:**

The DICOM image header is generated through mapping RIS data, generation by a modality and manual input by a user. Either one of these sources can potentially generate incorrect and/or invalid data in the image header. Problems are unfortunately not always immediately detected. For example, an incorrectly identified study might be archived in the PACS and get “lost”, only appearing when the data is migrated, which could be years later. A header with an Institution ID exceeding the maximum length of that field might be stored by vendor A while being rejected by vendor B as an invalid image when being migrated years later. Keeping tight tabs on these issues and validate images using appropriate tools is important.

**3. Hanging Protocol Issues:**

Hanging protocols not working is almost always related to incorrect header information or the wrong interpretation of the headers. A common mismatch is related to the way CR and DR systems organize their images into series. Some create a new series for each view (e.g. a Chest PA and LAT), some group them together in a single series. Another frequent issue occurs when some modalities modify automatically series and study descriptions, not taking the values from the worklist and therefore causing these descriptions not matching the hanging protocol configurations at the view station. Sometimes, additional QA steps are required, in addition to training of technologists.

**4. CD import issues:**

These issues almost always can be traced back to non-compliance with the DICOM standard and/or corresponding IHE profile. Frequent issues are the absence of DICOM image files because the vendor is only providing their proprietary format, a missing directory file, mismatch of the so-called meta-file header with the actual data content, incorrect transfer syntaxes such as compression, and several others. In many cases, one can convert the images to an acceptable format that can be imported using additional tools; however, in some cases it is impossible to read the proprietary information, causing a repeat exam.

**5. SOP Class support:**

Modalities are eager to support new functionality, represented by the use of new SOP Classes as they contain more information and allow for better viewing and processing. The most common mismatches are due to non-support of the PACS for the enhanced CT, MRI SOP Classes and Structured reports, such as generated by CAD devices and Ultrasound units for measurements. In most cases, a modality can be “de-featured” to fall back to an older SOP Class, or alternate encoding (e.g. burn in the CAD marks into a secondary capture), in some cases, one will be stuck with the proprietary information (e.g. MRI spectroscopy).

**Troubleshooting**

I am convinced that all of the issues listed above can be made visible with the right tools and utilities. If you are not that familiar with these, I strongly recommend you get familiar with these, i.e. download the Wireshark sniffer, get the manual from Amazon, get familiar with modality simulators such as [OTDICE][2] for a demo, use the appropriate [monitoring tools][3]. If this is too overwhelming, or you are not into self-study, consider a comprehensive training class where you will get hands-on training on how to troubleshoot and use these tools.

I will share with Shahid the next five top issues in a subsequent article. In the mean time, I’d appreciate any feedback and/or like to see your most frequent problems list so it can be shared with others. Please drop a comment here on this blog posting or [send email][4] for private questions.

 [1]: http://www.otechimg.com
 [2]: http://www.otechimg.com/productDetails.cfm?id=S-100
 [3]: http://www.otechimg.com/productDetails.cfm?id=S-201
 [4]: http://www.otechimg.com/contactus.cfm