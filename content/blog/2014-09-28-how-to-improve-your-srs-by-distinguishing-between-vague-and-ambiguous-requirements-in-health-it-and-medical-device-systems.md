---
title: How to improve your SRS by distinguishing between vague and ambiguous requirements in health IT and medical device systems
author: Shahid N. Shah
type: post
date: 2014-09-28T08:05:57+00:00
url: /2014/09/28/how-to-improve-your-srs-by-distinguishing-between-vague-and-ambiguous-requirements-in-health-it-and-medical-device-systems/
featured_image: /uploads/2014/09/How-to-improve-your-SRS-by-distinguishing-between-vague-and-ambiguous-requirements-in-health-IT-and-medical-device-systems.jpg
oc_commit_id:
  - https://www.healthcareguy.com/2014/09/28/how-to-improve-your-srs-by-distinguishing-between-vague-and-ambiguous-requirements-in-health-it-and-medical-device-systems/1478770877
  - https://www.healthcareguy.com/how-to-improve-your-srs-by-distinguishing-between-vague-and-ambiguous-requirements-in-health-it-and-medical-device-systems/1420535157
oc_metadata:
  - |
    {		version:'1.1',		tags: {'srs': {"text":"SRS","slug":"srs","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'improving-srs': {"text":"Improving SRS","slug":"improving-srs","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'meaningful-srs': {"text":"Meaningful SRS","slug":"meaningful-srs","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}}	}
dsq_thread_id:
  - 5158062598
categories:
  - Implementation
  - Meaningful Use
  - Medical Devices
tags:
  - Improving SRS
  - Meaningful SRS
  - SRS

---
_Because it&#8217;s so easy to build software these days we&#8217;re seeing a proliferation of healthcare apps — what&#8217;s hard to figure out is whether we&#8217;re building the right software. [Abder-Rahman Ali][1], currently pursuing his Medical Image Analysis Ph.D. in France, has graciously agreed to give us advice on how to write good software specifications for health and medical technology solutions. Some of you are probably rolling your eyes and thinking that software requirements specifications (SRS) are old and &#8220;tired&#8221; and we should be writing agile user stories instead. The reality is that in regulated and safety critical environments we still rely on SRS documents but the complex nature of systems of systems is making even those documents difficult to write. So, we&#8217;ll be talking requirements instead of user stories for now. The following is Abder-Rahman&#8217;s second installment, focused on vague and ambiguous requirements. He can be reached via [e-mail][2] or [twitter][3]._ 

Sometimes, when we pass by a software requirement that is not clear enough, we may say it is _vague_, and in another occasion, we may say it is _ambiguous_. Yes, we added such two features to that same requirement by that same person. But, did that person just use those two terms to refer to that that requirement was unclear? Does he just use those two terms interchangeably? Well, the bottom line, do _vague_ and _ambiguous_ mean the same at all? Or, they refer to two different things? This is what we will investigate in this article of our series.

Before beginning this topic, let us see how dictionaries define the terms _vagueness_ and _ambiguous_.

Of the ways how _Merrian-Webster_ dictionary defines the term _vague_ is as follows:

> _Not clear in meaning: stated in a way that is general and not specific_
> 
> _Not thinking or expressing your thoughts clearly or precisely_
> 
> _Not completely formed or developed_

Whereas, if we see how the same dictionary defines the term _ambiguous_, some of how it defines it is as follows:

> _Able to be understood in more than one way: having more than one possible meaning_

I like how Diana Santos distinguishes between those two terms in [her book][4], where she argues that _vagueness_ is related to the language system, and thus, is considered systematic, and is a frequent property of the language. Whereas _ambiguity_ is considered an unsystematic and accidental property.

Diana also stresses that for an expression to be vague between A and B, there should be a shared content. That is, having the same linguistic object doing double duty. In this case, we can consider the cases of “either A or not A” as an instances of vagueness. This Vagueness is automatically reflected in the speaker’s performance since it is an essential property of the linguistic system. But, if we go towards ambiguity, most ambiguities produced by speakers go unnoticed, since as we mentioned, it is considered unsystematic.

Put in another way, [invitation to critical thinking][5] takes us to the following; If we want to say that a term or expression is _ambiguous_, is to say that it has more than one conventional meaning. That is, it can be conventionally understood in more than one way.

Let us take an example. If you hear the word “bank”, what would it mean? Some of the meanings for “bank” are as follows:

  * a noun for piled up mass, such as snow or clouds
  * a noun for the slope of land adjoining a body of water
  * a value for the action of putting something of value away in safekeeping

The book also points out that for a term to be _vague_ means that it is not entirely clear what it does and doesn’t apply to.

[Cognitive Linguistics: Basic Readings][6], sums the above up, by mentioning that the difference between ambiguity and vagueness is a matter of whether two or more meanings associated with a given phonological form are _distinct_ (ambiguous), or _united_ as non-distinguished subcases of a single more general meaning (vague). An example for _ambiguity_ as we mentioned is the term “bank”, where the meanings are quite separate. An example of _vagueness_ is “aunt”, where it can mean “father’s sister” or “mother’s sister”, thus, the meanings are united into one meaning, that is, “parent’s sister”. So, the bottom line is that _ambiguity_ corresponds to separation of different meanings, and _vagueness_ corresponds to unity of different meanings.

So, I think we should now start admitting that there really exists a difference between those two terms, shouldn’t we?

Let us come back to software requirements. As [Ben Rinzler][7] mentions, the requirements statements must define a specific and testable outcome. That is, a way to measure that the requirement has been met has to be provided. But, such precision will diminish with vague and ambiguous requirements.

Rinzler continues; a _vague_ requirement is that requirement that does not include enough information to establish exactly how to meet the requirement. On the other hand, an _ambiguous_ requirement can have multiple meanings. Such requirement may sound precise, but defines the desired result in terms that can be interpreted in more than one way.

Let us take an example on both vague and ambiguous requirements to make this more clear.

An example of a _vague_ requirement is the following:

> _The system shall be able to read updates from MedImg_

The above requirement is considered vague since what will be “read” and what happens to the data was not specified.

This requirements can be improved as follows:

> _The system shall be able to import new tumor patient data supplied by MedImg to the radiology management system, for evaluating the tumor to be malignant or benign_

An example of an _ambiguous_ requirement is the following:

> _The system shall be able to provide historical reports_

Here, we have to specify what we mean by “historical reports”. Thus, the requirement can be improved as follows:

> _The system shall be able to provide patient tumor data for the past five calendar years_

We will end up the article here at the moment, so it doesn’t grow bigger for the reader. The main point to remember is that _vagueness_ and _ambiguous_ refer to two different terms, and they are factors that diminish the requirements’ precision and its ability to be measured and evaluated.

Stay tuned for the next articles, where we will dig more deep on how to deal and work with such uncertain requirements, and how can we present them in a precise manner.

&nbsp;

 [1]: http://www.productivecome.com/
 [2]: mailto:abder-rahman.a.ali@ieee.org
 [3]: http://www.twitter.com/abderhasan
 [4]: http://www.amazon.com/gp/search?index=books&linkCode=qs&keywords=9789042017511
 [5]: http://www.amazon.com/gp/search?index=books&linkCode=qs&keywords=9780495103714
 [6]: http://www.amazon.com/gp/search?index=books&linkCode=qs&keywords=9783110190854
 [7]: http://www.amazon.com/Telling-Stories-Writing-Software-Requirements/dp/0470437006