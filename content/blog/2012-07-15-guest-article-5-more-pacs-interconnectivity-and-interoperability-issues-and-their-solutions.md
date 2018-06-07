---
title: 'Guest Article: 5 more PACS interconnectivity and interoperability issues and their solutions'
author: Shahid N. Shah
type: post
date: 2012-07-16T00:45:36+00:00
url: /2012/07/15/guest-article-5-more-pacs-interconnectivity-and-interoperability-issues-and-their-solutions/
oc_commit_id:
  - https://www.healthcareguy.com/2012/07/15/guest-article-5-more-pacs-interconnectivity-and-interoperability-issues-and-their-solutions/1478770805
dsq_thread_id:
  - 5215268125
categories:
  - Uncategorized

---
_Most health IT interoperability and connectivity discussions these days center around HL7, CCD, and other structured data interchange. However, the vast majority of data (in terms of size) is shared as images and documents. The DICOM and PACS standards are very successful but given the number of questions I get about them from readers it seems there’s still a lot of guidance and support needed. To help answer some of the most common technical questions, I reached out to a fellow health IT expert, Herman Oosterwijk from OTech._ 

_A few weeks ago _Herman _shared with us his [Top 5 PACS interoperability issues][1]. That list was popular enough that I&#8217;ve asked him to share his next 5 and here&#8217;s what he had to say:_

**Transfer syntax support:**

In addition to missing SOP Class support (e.g. not supporting Structured Reports from an Ultrasound or a new enhanced MRI object containing spectroscopy data), PACS systems might not support the specific encoding, i.e. transfer syntaxes such as wavelet compression. In addition, a PACS system might mishandle a Big Endian encoding from an older modality, JPEG or other non-popular compression support such as Run Length Encoding (RLE). Many PACS systems do not (yet) support the MPEG files created by endoscopy and surgery exams. Upgrading your PACS and/or “downgrading” your modality is the only solution.

**UID issues:**

Some devices create “illegal” Unique Identifiers (UID’s) which identifies an image, series, study, and/or relationships among images. The reason could be because their UID creation algorithm creates sometimes empty values or subcomponents with leading zero’s, which are invalid. Most PACS systems will either refuse these images or quarantine them. Some modalities issue a new UID when an image is resent, which requires someone to delete these duplicates at the PACS. Some modalities re-use a UID therefore requiring a PACS System Administrator to fix those as well. There are no easy solutions for these problems, except for keeping the vendors accountable to fix their software.

**Modality Worklist (MWL) issues:**

A worklist provided by the RIS, PACS or broker, should match the studies to be performed at a modality, no more and no less. Some Modality worklist providers provide too much data (e.g. all of the exams for all modalities, or all of the CR exams instead of only the ones for the ER), some provide not enough differentiation (e.g. only the bone-scans) and some provide not enough. Remedies are reconfiguring the modality worklist provider, interface engine, or sometimes changing the input data by the scheduling department.

**Burned-in Data:**

Many Ultrasound units and frame-grabber interfaces have the unfortunate side-effect that all of the information on the screen is captured, including the patient demographics. This can create major issues when the patient demographics is incorrect, which happens in most cases because a technologist forgets to select a new patient or makes an incorrect selection. Many users put “X-es” over the incorrect text, with as serious risk that a receiving application might not support these overlays, presentation states, or, even proprietary annotations. The only solution is to use “paintbrush” utilities. Note that David Clunie has an excellent free [tool][2] to do this.

**Loss of annotations:**

Many PACS systems still support proprietary solutions to store annotations. When displayed on the PACS workstations from the same vendor they appear, however, when displayed on another vendor’s workstation, such as used by a referring physician, night hawk service, or 3<sup>rd</sup> party web servers, they will disappear. The solution is to generate compatible overlays (some modalities and workstations have this option) and/or upgrade all of your devices to support the DICOM Softcopy Presentation State.

&nbsp;

These issues can be made visible and/or simulated using the appropriate tools for troubleshooting. I wanted to thank Shahid for letting me reach his talented technical audience and I&#8217;m happy to come back and discuss tools such as a DICOM sniffer, modality simulator, and DICOM validator in subsequent guest postings.

 [1]: https://www.healthcareguy.com/2012/06/22/guest-article-top-5-pacs-interconnectivity-and-interoperability-issues-and-their-solutions/ "Guest Article: Top 5 PACS interconnectivity and interoperability issues and their solutions"
 [2]: http://www.dclunie.com/pixelmed/software/webstart/DicomCleanerUsage.html