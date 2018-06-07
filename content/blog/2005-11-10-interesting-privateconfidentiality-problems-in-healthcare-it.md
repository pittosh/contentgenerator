---
title: Interesting privacy/confidentiality problems in Healthcare IT
author: Shahid N. Shah
type: post
date: 2005-11-10T14:30:48+00:00
url: /2005/11/10/interesting-privateconfidentiality-problems-in-healthcare-it/
oc_commit_id:
  - https://www.healthcareguy.com/2005/11/10/interesting-privateconfidentiality-problems-in-healthcare-it/1478768904
views:
  - 1254
dsq_thread_id:
  - 5194991765
categories:
  - Opinion

---
A student working on a Ph.d thesis on IT security sent me an email last night asking about interesting problems and industry directions for computer security in healthcare IT. He&#8217;s interested in applying his knowledge to this area and was asking specifically about privacy and confidentiality. I figured other students or readers might be interested in my answer so I&#8217;m answering the question here and others can comment if they can help out further.

In general, the answer to the security, privacy, and confidentiality lies somewhat in legacy software and a little bit in the US regulations for HIPAA. So, here&#8217;s a little rundown on HIPAA.

According to the American Health Information Management Association, **an average of 150 people will have access to a patientâ€™s private health information during a typical hospital stay of two to three days**. Private, confidential health information can sometimes be released, shared or distributed without a personâ€™s consent. Sometimes, the release is deliberate; other times, the release occurs due to poor security safeguards. The Health Insurance Portability and Accountability Act (HIPAA) was signed into law in 1996, in part, as a response to concerns regarding confidential health information. HIPAA ensures that those who have access to your health information are authorized and they will use it appropriately. HIPAAâ€™s overall purpose is to:

  * Provide continuity and portability of health benefits to people in between jobs.
  * Ensure security and privacy of individual health information.
  * Reduce administrative expenses in the healthcare system; administrative costs have been estimated to account for nearly 25% of healthcare costs.
  * Provide uniform standards for electronic health information transactions.
  * Provide measures to combat fraud and abuse in health insurance and health care delivery.

**How HIPAA changes things**:

<table>
  <tr valign="top">
    <th>
      Before HIPAA
    </th>
    
    <th>
      After HIPAA (assuming perfect implementation)
    </th>
  </tr>
  
  <tr valign="top">
    <td>
      Privacy procedures regarding a personâ€™s health information were often inconsistent from state to state.
    </td>
    
    <td>
      Basic privacy expectations are now standard across the board; everyone will protect health information to comply with certain federal minimum standards.
    </td>
  </tr>
  
  <tr valign="top">
    <td>
      Security procedures regarding how to protect health information were inconsistent.
    </td>
    
    <td>
      Standardized security procedures are now required.
    </td>
  </tr>
  
  <tr valign="top">
    <td>
      Lack of standard data formats made sharing health information cumbersome and inefficient.
    </td>
    
    <td>
      Streamlined, more efficient systems for sharing electronic health information.
    </td>
  </tr>
  
  <tr valign="top">
    <td>
      Communication was difficult.
    </td>
    
    <td>
      Improved communication and enhanced consumer service, for example, the coordination of health care benefits, will be easier.
    </td>
  </tr>
</table>

**HIPAA is _supposed_ to affect almost everyone**. HIPAA applies to three fundamental types of organizations that collectively are referred to as Covered Entities, as they must comply with HIPAA. These Covered Entities are:

  * Health Plans &#8211; Individuals or groups that provide or pay for healthcare, such as insurance companies, health maintenance organizations and Medicare and Medicaid programs. 
  * Health Care Clearinghouses &#8211; Organizations that facilitate the processing of health information such as billing services or transcription services. 
  * Health Care Providers &#8211; Individuals, such as physicians, dentists, pharmacists, and larger organizations, such as hospitals, are Covered Entities when they electronically transfer patient information. 

Who is Covered &#8211; Examples

  * Hospitals and clinics 
  * Nursing homes 
  * Home health agencies 
  * Most physicians, pharmacists, and dentists 
  * Ambulance services 
  * Managed care organizations 
  * Some local health and social services departments 
  * Laboratories 

Who is Not Covered &#8211; Examples
  
Even though these organizations are involved with healthcare, since they do not pay for healthcare, provide healthcare, or process healthcare information, they are not considered Covered Entities:

  * Workers compensation programs 
  * Government programs that fund health care through grants 
  * Government oversight agencies 

**Privacy and Security Require System Modernization**
  
HIPAA has detailed rules regarding:

  * When a staff member need to get a personâ€™s written or oral permission to share health information. 
  * When a staff member should give a person a written privacy notice that tells the person how an organization will deal with his/her clinical information. 
  * What an organization has to do in order to implement HIPAA. 

What is covered
  
HIPAA does not protect all health information, only information in the hands of a Covered Entity or covered program which is integral to its activities as a Covered Entity or covered program.

Protected Health Information
  
The HIPAA privacy rule covers and sets standards for the collecting, sharing and storing of a personâ€™s Protected Health Information, or PHI, for short. PHI is information that:

  * Relates to past, present or future physical or mental health or condition, payments and provisions about healthcare. 
  * Identifies the individual in a personal way. 
  * Provides a reasonable basis to be used to identify the individual. 
  * Is created or received by a Covered Entity. 

The privacy standards describe which health information about individuals is protected and the determination of who is permitted to use, disclose, or access that information. HIPAA sets procedures for the following privacy areas. Patients will have the right to obtain and amend their PHI to:

  * Request restrictions on uses and disclosures. 
  * Request more confidential communications. 
  * Receive an accounting of disclosures. 
  * Complain about privacy violations. 
  * Use and disclosure of PHI &#8211; Patients will have the right to know how their PHI will be used and who will receive their PHI. They are also entitled to a Notice of Privacy Practices. 
  * Special rules for certain types of entities &#8211; Some Covered Entities have additional privacy regulations covering areas like directories, marketing and fund raising. 
  * Administrative requirements of Covered Entities &#8211; Details record-keeping and procedural compliance issues. 
  * Enforcement and compliance &#8211; The potential penalties and fines for noncompliance. 

**So where&#8217;s the work?**
  
Almost _everywhere_. Most legacy and even systems in current use were written before HIPAA was passed and many of its requirements made it into law. Even though most of the regulations in HIPAA do not discuss privacy and confidentiality specifically in electronic systems, many of its provisions can not be met in any reasonable way (based on cost and time) _without_ electronic tracking systems. So, there is plenty of opportunity to create solutions that track the information, that wrap the information as it&#8217;s being transferred, that audit systems to ensure compliance, etc.

Ultimately, the answer is that patients want complete privacy and confidentiality of their records, even if 150 people are authorized to see their data. The challenge is to meet the privacy demands in current systems without throwing out everything and starting from scratch.