---
title: 'Guest Article: The challenge of interoperability across local and hosted solutions'
author: Shahid N. Shah
type: post
date: 2009-02-19T01:20:24+00:00
url: /2009/02/19/guest-article-the-challenge-of-interoperability-across-local-and-hosted-solutions/
oc_commit_id:
  - https://www.healthcareguy.com/2009/02/19/guest-article-the-challenge-of-interoperability-across-local-and-hosted-solutions/1478770441
ratings_users:
  - 4
ratings_score:
  - 16
ratings_average:
  - 4
dsq_thread_id:
  - 5236292627
categories:
  - Opinion

---
_Dr. Robert Rowley is a practicing family physician in the San Francisco Bay Area, and has been using electronic medical records systems for 10 years._ _Recently he joined_ [_Practice Fusion_][1] _as its Chief Medical Officer where he helps build a hosted web-based EMR free to physician end users. Dr. Rowley has written regularly in print media as well as blogs about a variety of aspects of ambulatory EMRs so I asked him to share with us his thoughts_ _about a really hard problem: clinical data interoperability, especially for hosted solutions connecting to on-premise solutions. Here’s what he had to say._

“Interoperability” has emerged as the new buzz-word in healthcare IT, and is a prominent feature in EMR certification as outlined in the new economic stimulus package. The goal is for all pieces of patient data to work together, regardless of how they are housed – clinical EMRs in multiple physicians’ offices (&#8216;”on premises”), hospital systems, billing systems, patient interfaces, and content sources. So what stands in the way of achieving this?

**Traditional EMRs**

Traditional EMRs were built to replicate the information in a paper chart and put it into discrete data fields in a database. They were practice-specific, and intended to be deployed locally in a physician’s office. Depending on the solution, the data is almost always kept on premises and often isn’t available remotely. The traditional EMR vendors (like NextGen and Allscripts) designed their data structure around templates – templates are each correlated with data tables – which means that the data structure of one practice using one set of templates will be different than another practice using a different set of templates (even if they are both using the same EMR product). This makes data sharing much more complex. 

The response to the difficulty in sharing clinical data between practices has been adoption of a standard-format input/output file, the Continuity of Care Record (CCR). This captures most of the important clinical data (but not everything in the template-driven database). Uploading and downloading CCRs for output or input into an EMR system is still pretty manual, and needs the evolution of networked “CCR bulletin boards” where such data can be posted (since there is no guarantee that two practices sharing the same patient will be available to each other at the same time). The result? Most practices, even with traditional EMRs, simply print out and fax clinical data to each other when requested. Not quite the goal of interoperability as envisioned.

**Hosted or Online EMRs**

Over the past decade newer EMR companies are beginning to emerge, such as Practice Fusion (the one I am working with), which are usually web-based and hosted “in the cloud” (ASP). By design, these systems have a standardized data structure, such that chart-sharing is easier because everyone’s data in one data center. They are designed to connect with multiple outside data sources (“cloud computing”), giving a unified view of a chart with pieces (like notes from different physicians seeing the patient, to hospital records, to reference content, etc) being pulled from different places. This entire way of approaching EMR (from an interoperability basis, rather than an internal-looking basis) is still young and evolving, but the potential for better interoperability is there. The parallel notion in the electronic-devices world is the USB standard, allowing multiple different products from different vendors to work with each other by simply plugging in and doing a one-time setup. The healthcare IT world needs to move in that direction.

**Connecting it all together**

So what is a physician to do? If one is in a paper-based environment, it is probably best to explore lightweight EMR systems designed for interoperability. If one already is using an on-premise system, then there are two options: (1) develop a way of connecting with others, such as through upload and download of CCRs, or (2) bolt-on a next-generation solution. Small “EMR lite” applications may be more amenable to migration; larger, committed installs in more expensive or complex systems are probably looking at CCR-based interconnectivity. 

Regardless of the solutions available at the present time, one thing is certain: the landscape is changing, and the market will see the emergence of inter-connectable products beyond what has emerged so far. And the orientation of the federal stimulus package encourages the market to move in that direction. As physicians, we practice interactively in networks (formal and informal), and the tools we use need to reflect that reality.

 [1]: http://www.practicefusion.com/