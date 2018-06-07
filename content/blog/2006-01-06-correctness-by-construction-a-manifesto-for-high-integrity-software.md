---
title: 'Correctness by Construction: A Manifesto for High-Integrity Software'
author: Shahid N. Shah
type: post
date: 2006-01-06T03:29:33+00:00
url: /2006/01/06/correctness-by-construction-a-manifesto-for-high-integrity-software/
oc_commit_id:
  - https://www.healthcareguy.com/2006/01/06/correctness-by-construction-a-manifesto-for-high-integrity-software/1478768983
views:
  - 1090
dsq_thread_id:
  - 44283342
categories:
  - Opinion

---
Clinical systems and medical devices, which deal with the lives of real people, fall into the category of high integrity systems which can&#8217;t tolerate any defects. _[Correctness by Construction: A Manifesto for High-Integrity Software][1]_ is a great article talking about how to create low- or zero-defect software while still maintaining good developer productivity through an agile methodology. The article&#8217;s abstract says:

> High-integrity software systems are often so large that conventional development processes cannot get anywhere near achieving tolerable defect rates. This article presents an approach that has delivered software with very low defect rates cost-effectively. We describe the technical details of the approach and the results achieved, and discuss how to overcome barriers to adopting such best practice approaches. We conclude by observing that where such approaches are compatible and can be deployed in combination, we have the opportunity to realize the extremely low defect rates needed for high integrity software composed of many million lines of code. 

Next time you hear someone telling you that zero-defect software just point them to this great article. Here&#8217;s a summary of what they say are the fundamental principles:

> The principles of making it difficult to introduce defects and making it easy to detect and remove errors early are achieved by a combination of the following six strategies:
> 
>   1. Using a sound, formal notation for all deliverables. For example, using Z for writing specifications so it is impossible to be ambiguous, or using SPARK to write the code so it is impossible to introduce errors such as buffer overflows.
>   2. Using strong, tool-supported methods to validate each deliverable. For example, carrying out proofs of formal specifications and static analysis of code. This is only possible where formal notations are used (strategy No. 1).
>   3. Carrying out small steps and validating the deliverable from each step. For example, developing a software specification as an elaboration of the user requirements, and checking that it is correct before writing code. For example, building the system in small increments and checking that each increment behaves correctly.
>   4. Saying things only once. For example, by producing a software specification that says what the software will do and a design that says how it will be structured. The design does not repeat any information in the specification, and the two can be produced in parallel.
>   5. Designing software that is easy to validate. For example, writing simple code that directly reflects the specification, and testing it using tests derived systematically from that specification.
>   6. Doing the hard things first. For example, by producing early prototypes to test out difficult design issues or key user interfaces.

Nice stuff. I&#8217;ve worked in a CMM Level 5 shop working on safety-critical software and when you use the principles as a way of life, zero defect software is definitely possible. When you spend more time thinking about requirements, design, and testing and less time about coding you&#8217;re bound to create fewer bugs.

 [1]: http://www.stsc.hill.af.mil/crosstalk/2005/12/0512CroxfordChapman.html