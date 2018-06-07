---
title: Why medical device data is the best way to fill meaningful use EHRs and conduct comparative effectiveness research (CER)
author: Shahid N. Shah
type: post
date: 2011-07-11T13:50:57+00:00
url: /2011/07/11/why-medical-device-data-is-the-best-way-to-fill-meaningful-use-ehrs-and-conduct-comparative-effectiveness-research-cer/
oc_commit_id:
  - https://www.healthcareguy.com/2011/07/11/why-medical-device-data-is-the-best-way-to-fill-meaningful-use-ehrs-and-conduct-comparative-effectiveness-research-cer/1478770751
dsq_thread_id:
  - 5178935432
categories:
  - Uncategorized

---
I will be presenting at the [O&#8217;Reilly Open Source Convention (OSCon) in Portland][1] at the end of the month. As an avid reader of dozens of O&#8217;Reilly&#8217;s technical books over the years I was excited when they reached out to ask if I would talk about open source in the healthcare world. While open source isn&#8217;t a major force in the healthcare IT ecosystem right now, that will be changing over the coming years and should be able to change the medical world in the same way that open source has improved enterprise IT and made the consumer web possible.

My presentation on Thursday July 28th at OSCon is on why medical device data is the best way to fill meaningful use EHRs and how open source technologies and open architectures can make that possible. I was interviewed by O&#8217;Reilly&#8217;s Andy Oram about this subject and the [podcast is available][2].

What I told Andy during the interview was that &#8220;Meaningful Use&#8221; is all about data, not about EHRs &#8212; the government needs data for cost comparisons, health professionals need data for treatment research and chart management, and patients need data for choosing the right providers and treatments. EHRs are just a vehicle, not the end goal.

Right now we know that Medicare and Medicaid are paying more 50% of the nation’s healthcare costs but doing so as &#8220;fees for services&#8221; without regard (for the most part) to what treatments, medications, or tests really work. The evidence-based research that goes into figuring out what works and what doesn&#8217;t is the foundation of what has been affectionately known as &#8220;Comparative Effectiveness Research&#8221; (CER) and is being re-branded as &#8220;Patient Centered Research&#8221;.

The government needs tons of data for CER, which is designed to inform health-care decisions by providing evidence on the effectiveness, benefits, and harms of different treatment options. The evidence is generated from research studies that compare drugs, medical devices, tests, surgeries, or ways to deliver health care.

In the best cases, researchers review evidence about the benefits and harms of each choice for different groups of people from existing clinical trials, clinical studies, and other research. Then, over time of course, researchers conduct studies that generate new evidence of effectiveness or comparative effectiveness of a test, treatment, procedure, or health-care service.

CER sounds like it’s all about the government and evidence-based medicine to contain healthcare costs but ultimately it’s about providing treatment comparison choices to help make informed decisions. In the end healthcare professionals must deliver tools to the patient that can help the patient and their families select the right treatment options.

Given that CER is very important and is ultimately why the government is giving away billions of dollars in incentives for healthcare IT (and not to prop up the EHR market), it&#8217;s important to understand where data comes from so that we know what the best approaches are to collect it.

There are two kinds of data that we normally see: one is _structured_ data which is computable, analyzable, comparable, quantifiable, and reportable; the other is _unstructured_ data which is basically dictations, documents, faxes, letters, and almost everything that is not computable or easily analyzable but is electronic nonetheless.

There are many sources of both unstructured and structured data but and oversimplified view is shown below. In a typical provider environment medical information comes from patients, professionals, labs/diagnostics, and medical devices. The table below shows how unstructured and structured data is &#8220;sourced&#8221; today.

<table class="comparison" border="0" cellspacing="0" cellpadding="5">
  <tr>
    <td>
    </td>
    
    <td>
      <strong>Patient</strong>
    </td>
    
    <td>
      <strong>Health Professional</strong>
    </td>
    
    <td>
      <strong>Labs & Diagnostics</strong>
    </td>
    
    <td>
      <strong>Medical Devices</strong>
    </td>
  </tr>
  
  <tr>
    <td>
      Source
    </td>
    
    <td>
      Self-reported by patient
    </td>
    
    <td>
      Observations by HCP
    </td>
    
    <td>
      Computed from specimens
    </td>
    
    <td>
      Computed real-time from patient
    </td>
  </tr>
  
  <tr class="section">
    <td>
      <strong>Unstructured Data</strong>
    </td>
    
    <td>
      Yes
    </td>
    
    <td>
      Yes
    </td>
    
    <td>
      Yes
    </td>
    
    <td>
      No
    </td>
  </tr>
  
  <tr>
    <td>
      Errors
    </td>
    
    <td>
      High
    </td>
    
    <td>
      Medium
    </td>
    
    <td>
      Low
    </td>
    
    <td>
    </td>
  </tr>
  
  <tr>
    <td>
      Time
    </td>
    
    <td>
      Slow
    </td>
    
    <td>
      Slow
    </td>
    
    <td>
      Medium
    </td>
    
    <td>
    </td>
  </tr>
  
  <tr>
    <td>
      Reliability
    </td>
    
    <td>
      Low
    </td>
    
    <td>
      Medium
    </td>
    
    <td>
      High
    </td>
    
    <td>
    </td>
  </tr>
  
  <tr>
    <td>
      Data size
    </td>
    
    <td>
      Small
    </td>
    
    <td>
      Small
    </td>
    
    <td>
      Large
    </td>
    
    <td>
    </td>
  </tr>
  
  <tr>
    <td>
      Availability
    </td>
    
    <td>
      Common
    </td>
    
    <td>
      Common
    </td>
    
    <td>
      Common
    </td>
    
    <td>
      Uncommon
    </td>
  </tr>
  
  <tr class="section">
    <td>
      <strong>Structured Data</strong>
    </td>
    
    <td>
      Yes
    </td>
    
    <td>
      Yes
    </td>
    
    <td>
      Yes
    </td>
    
    <td>
      Yes
    </td>
  </tr>
  
  <tr>
    <td>
      Errors
    </td>
    
    <td>
      High
    </td>
    
    <td>
      Medium
    </td>
    
    <td>
      Low
    </td>
    
    <td>
      Low
    </td>
  </tr>
  
  <tr>
    <td>
      Time
    </td>
    
    <td>
      Slow
    </td>
    
    <td>
      Slow
    </td>
    
    <td>
      Medium
    </td>
    
    <td>
      Fast
    </td>
  </tr>
  
  <tr>
    <td>
      Reliability
    </td>
    
    <td>
      Low
    </td>
    
    <td>
      Medium
    </td>
    
    <td>
      High
    </td>
    
    <td>
      High
    </td>
  </tr>
  
  <tr>
    <td>
      Discrete size
    </td>
    
    <td>
      Small
    </td>
    
    <td>
      Small
    </td>
    
    <td>
      Small
    </td>
    
    <td>
      Small
    </td>
  </tr>
  
  <tr>
    <td>
      Streaming size
    </td>
    
    <td>
    </td>
    
    <td>
    </td>
    
    <td>
    </td>
    
    <td>
      Large
    </td>
  </tr>
  
  <tr>
    <td>
      Availability
    </td>
    
    <td>
      Uncommon
    </td>
    
    <td>
      Common
    </td>
    
    <td>
      Somewhat Common
    </td>
    
    <td>
      Uncommon
    </td>
  </tr>
</table>

As is evident by the table above, many of the existing MU incentives in Phase 1 (patient reported and healthcare professional entered especially) promote the wrong kinds of collection: unreliable, slow, and error prone. Accurate, real-time, data is only available from connected medical devices and labs / diagnostics equipment. 

Given that meaningful Use and CER advocates are promoting (structured) data collection for reduction of medical errors, analysis of treatments and procedures, and research for new methods it&#8217;s important to see that we&#8217;re not going to get real gains until the medical device vendors are fully connected and providing data directly into EHRs or clinical data warehouses.

Please check out my [O&#8217;Reilly interview with Andy Oram][2] about this subject and let me know whether you agree.

 [1]: http://www.oscon.com/oscon2011
 [2]: http://oreil.ly/nod8i9 "Shahid's Podcast on Medical Device Data Integration"