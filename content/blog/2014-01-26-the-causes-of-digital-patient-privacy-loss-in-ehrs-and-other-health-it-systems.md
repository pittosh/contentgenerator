---
title: The causes of digital patient privacy loss in EHRs and other health IT systems
author: Shahid N. Shah
type: post
date: 2014-01-26T21:55:24+00:00
url: /2014/01/26/the-causes-of-digital-patient-privacy-loss-in-ehrs-and-other-health-it-systems/
oc_commit_id:
  - https://www.healthcareguy.com/2014/01/26/the-causes-of-digital-patient-privacy-loss-in-ehrs-and-other-health-it-systems/1478770850
  - https://www.healthcareguy.com/the-causes-of-digital-patient-privacy-loss-in-ehrs-and-other-health-it-systems/1420199885
dsq_thread_id:
  - 5195284574
oc_metadata:
  - |
    {		version:'1.1',		tags: {'ethics': {"text":"Ethics","slug":"ethics","source":{"_className":"SocialTag","url":"http://d.opencalais.com/dochash-1/ea5c7831-1da4-34d7-ae79-505054ed419e/SocialTag/1","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/tag/SocialTag","name":"SocialTag"},"name":"Ethics","makeMeATag":true,"importance":1,"normalizedRelevance":1},"bucketName":"blacklisted","bucketPlacement":"user","_className":"Tag"}, 'enterprise-systems': {"text":"Enterprise Systems","slug":"enterprise-systems","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'privacy': {"text":"Privacy","slug":"privacy","source":{"url":"http://d.opencalais.com/dochash-1/ea5c7831-1da4-34d7-ae79-505054ed419e/SocialTag/2","subjectURL":null,"type":{"url":"http://s.opencalais.com/1/type/tag/SocialTag","name":"SocialTag","_className":"ArtifactType"},"name":"Privacy","makeMeATag":true,"importance":1,"_className":"SocialTag","normalizedRelevance":1},"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'ehr': {"text":"EHR","slug":"ehr","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'law': {"text":"Law","slug":"law","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'health-it': {"text":"Health IT","slug":"health-it","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'digital-health': {"text":"Digital Health","slug":"digital-health","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'hipaa': {"text":"HIPAA","slug":"hipaa","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'privacy-law': {"text":"Privacy Law","slug":"privacy-law","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}}	}
categories:
  - Events
  - Government Regulations
  - Information Assurance (IA) and Security
  - NIST
tags:
  - Digital Health
  - EHR
  - Enterprise Systems
  - Health IT
  - HIPAA
  - law
  - Privacy
  - Privacy Law

---
This past Friday I was invited by the [Patient Privacy Rights (PPR) Foundation][1] to lead a discussion about privacy and EHRs. The discussion, entitled “**Fact vs. Fiction: Best Privacy Practices for EHRs in the Cloud**,” addressed patient privacy concerns and potential solutions for doctors working with EHRs.

While we are all somewhat disturbed by the slow erosion of privacy in all aspects of our digital lives, the rather rapid loss of patient privacy around health data is especially unnerving because healthcare is so near and dear to us all. In order to make sure we provided some actionable intelligence during the PPR discussion, I started the talk off giving some of the reasons why we&#8217;re losing patient privacy in the hopes that it might foster innovators to think about ways of slowing down inevitable losses.

Here are some of the causes I mentioned on Friday, not in any particular order:

  * **Most patients, even technically astute ones, don&#8217;t really understand the concept of digital privacy**. Digital is a “cyber world” and not easy to picture so patients believe their data and privacy is protected when it may not be. I usually explain patient privacy in the digital world to non-techies using the analogy of curtains, doors, and windows. The digital health IT world of today is like walking into a patient’s room in a hospital in which it’s a large shared space with no curtains, no walls, no doors, etc. (even for bathrooms or showers!). <span style="line-height: 1.5em;">In this imaginary world, every private conversation occurs so that others can hear it, all procedures are performed in front of others, etc. without the patient’s consent and their objections don’t even matter. If they can imagine that scenario, then patients will probably have a good idea about how digital privacy is conducted today &#8212; a big shared room where everyone sees and hears everything even over patients&#8217; objections.</span>
  * **It&#8217;s faster and easier to create non-privacy-aware IT solutions than privacy-aware ones**.  Having built dozens of HIPAA-compliant and highly secure enterprise health IT systems for decades, my anecdotal experience is that when it comes to features and functions vs. privacy, features win. Product designers, architects, and engineers talk the talk but given the difficulties of creating viable systems in a coordinated, integrated digital ecosystem it&#8217;s really hard to walk the privacy walk  Because digital privacy is so hard to describe even in simple single enterprise systems, the difficulty of describing and defining it across multiple integrated systems is often the reason for poor privacy features in modern systems.
  * **It&#8217;s less expensive to create non-privacy-aware IT solutions**. Because designing privacy into the software from the beginning is hard and requires expensive security resources to do so, we often see developers wait until the end of the process to consider privacy. Privacy can no more be added on top of an existing system than security can &#8212; either it&#8217;s built into the functionality or it&#8217;s just going to be missing. Because it&#8217;s cheaper to leave it out, it&#8217;s often left out.
  * **The government is incentivizing and certifying functionality over privacy and security**. All the meaningful use certification and testing steps are focused too much on prescribed functionality and not enough on data-centric privacy capabilities such as notifications, disclosure tracking, and compartmentalization. If privacy was important in EHRs then the NIST test plans would cover that. Privacy is difficult to define and even more difficult to implement so the testing process doesn&#8217;t focus on it at this time.
  * **Business models that favor privacy loss tend to be more profitable**. Data aggregation and homogenization, resale, secondary use, and related business models tend to be quite profitable. The only way they will remain profitable is to have easy and unfettered (low friction) ways of sharing and aggregating data. Because enhanced privacy through opt-in processes, disclosures, and notifications would end up reducing data sharing and potentially reducing revenues and profit, we see that privacy loss is going to happen with inevitable rise of EHRs.
  * **Patients don&#8217;t really demand privacy from their providers or IT solutions in the same way they demand other things**. We like to think that all patients demand digital privacy for their data. However, it&#8217;s rare for patients to choose physicians, health systems, or other care providers based on their privacy views. Even when privacy violations are found and punished, it&#8217;s uncommon for patients to switch to other providers.
  * **Regulations like HIPAA have made is easy for privacy loss to occur**. HIPAA has probably done more to harm privacy over the past decade than any other government regulations. More on this in a later post.

The only way to improve privacy across the digital spectrum is to realize that health providers need to conduct business in a tricky intermediary-driven health system with sometimes conflicting business goals like reduction of medical errors or lower cost (which can only come with more data sharing, not less). Digital patient privacy is important but there are many valid reasons why privacy is either hard or impossible to achieve in today&#8217;s environment. Unless we intelligently and honestly understand why we lose patient privacy we can&#8217;t really create novel and unique solutions to help curb the loss.

What do you think? What other causes of digital patient privacy loss would you add to my list above?

 [1]: http://patientprivacyrights.org/