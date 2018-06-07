---
title: The difference between User Stories and Software Requirements Specifications (SRS), especially for regulated systems (part 1)
author: Shahid N. Shah
type: post
date: 2014-10-10T07:52:30+00:00
url: /2014/10/10/the-difference-between-user-stories-and-software-requirements-specifications-srs-especially-for-regulated-systems-part-1/
featured_image: /uploads/2014/10/The-difference-between-User-Stories-and-Software-Requirements-Specifications-SRS-especially-for-regulated-systems-part.jpg
oc_commit_id:
  - https://www.healthcareguy.com/2014/10/10/the-difference-between-user-stories-and-software-requirements-specifications-srs-especially-for-regulated-systems-part-1/1478770873
  - https://www.healthcareguy.com/the-difference-between-user-stories-and-software-requirements-specifications-srs-especially-for-regulated-systems-part-1/1420534350
oc_metadata:
  - |
    {		version:'1.1',		tags: {'software-requirements-specification': {"text":"Software Requirements Specification","slug":"software-requirements-specification","source":{"_className":"SocialTag","url":"http://d.opencalais.com/dochash-1/4ba53140-36a2-3197-9887-5fc5532ffd68/SocialTag/6","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/tag/SocialTag","name":"SocialTag"},"name":"Software Requirements Specification","makeMeATag":true,"importance":1,"normalizedRelevance":1},"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'srs': {"text":"SRS","slug":"srs","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'user-stories': {"text":"User Stories","slug":"user-stories","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'regulated-systems': {"text":"regulated systems","slug":"regulated-systems","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}}	}
dsq_thread_id:
  - 5155642542
categories:
  - User Experience
tags:
  - regulated systems
  - Software Requirements Specification
  - SRS
  - User Stories

---
_It’s getting easier and easier to build unregulated software these days but it&#8217;s still pretty hard to create regulated/certified systems such as EHRs, medical device software, and government IT. To help create better systems we all know we need better user requirements; however, &#8220;heavyweight requirements&#8221; efforts have been shunned, especially in unregulated systems, over the past decade in favor of &#8220;user stories&#8221; and more agile specifications. But, are agile user stories the best way to go in regulated systems where requirements traceability and safety analysis is a must? I invited [Abder-Rahman Ali][1], currently pursuing his Medical Image Analysis Ph.D. in France, to come back and give us advice on whether there&#8217;s room for both user stories and SRSs in regulated industries or if we&#8217;re stuck with formal requirements specs. The following is Abder-Rahman’s third installment for this blog and I&#8217;m excited he&#8217;ll be tackling such an important topic. As always, he can be reached via [e-mail][2] or [twitter][3]. Here&#8217;s what Abder-Rahman says about User Stories vs. Software Requirements Specifications:_

It was on February, 2001, when seventeen practitioners formed what was called [The Agile Manifesto][4]. It seems that since then, we started to hear of the term _User Story_, although, as will be shown below, it seems that the term appeared before that date.

The questions that may pop-up on someone’s head are, is the User Story just a fancy name to the user requirement? Or, it is actually a new mindset of thinking in the way of dealing with user requirements?

Referring to [Wikipedia][5] about the history of user stories, I found that user stories originated with Extreme Programming (XP), but, it wasn’t until 2001, when Ron Jeffries proposed the Three C’s formula: _Card_, _Conversion_, _Confirmation_, where the components of the user stories were captured.

But, what are User Stories after all?

I really liked how [Mike Cohn][6] described User Stories, when he said:

> _User Stories are short, simple description of a feature told from the perspective of the person who desires the new capability, usually a user or customer of the system. They typically follow a simple template:_
> 
> _As a <type of user>, I want <some goal> so that <some reason>._
> 
> _User Stories are often written on index cards or sticky notes, stored in a shoe box, and arranged on walls or tables to facilitate planning and discussion. As such, they strongly shift the focus from writing about features to discussing them. In fact, these discussions are more important than whatever text is written._

Before moving ahead, and comparing User Stories with Software Requirements Specifications (SRS), let us see how SRS is defined. Based on [Chambers][7], SRS describes the essential behavior of a software product from a user&#8217;s point of view, where the purpose of SRS is to be a basis for agreement between the customers and the suppliers on what the software product is to do; a basis for developing the software design; a basis for estimating costs and schedules; a baseline for validation and verification; reducing the development effort; facilitating transfer; and serves as a basis for enhancement.

After knowing what they mean, how can we compare User Stories with SRS? I saw that rather than bringing theory to this part, why not monitor some discussions related to this issue? I thus went through some discussions at a [Programmers Stack Exchange][8] thread, and came up with the following:

One of the people involved in the discussion mentioned: _To be honest, after spending close to two years immersed in Agile development, I still think &#8220;User Story&#8221; is just a fancy term for &#8220;functional requirement&#8221;_. That person continues: _What User Stories almost never capture, in my experience, are non-functional requirements like performance and security. These kinds of requirements are very difficult to write properly and the format of the User Story simply isn&#8217;t very good for capturing them, because they&#8217;re more about general product quality and mitigating (but not eliminating) risks rather than meeting a specific user&#8217;s need. So, I really think of User Stories as a subset of requirements, with a specific formula, and still use the terms pretty much interchangeably. The one major advantage User Stories do have over requirements is that the word &#8220;requirement&#8221; suggests that a feature is required where it is often just desired. User Stories can in theory be prioritized and slotted in for any release, whereas requirements appear to be a prerequisite for every release._

Other opinions arise mentioning that SRS focuses on “how” the user interacts with the system, and “how” to implement the functionality. On the other hand, User Stories focus on “what” (interaction between user and system) purpose do features have, such that, the task of a User Story would be a functional requirement, and is the expected work product after the functional tasks have all been completed. Thus, they are completely different things.

Requirements assume that the design of the application is done beforehand, and development is considering the implementation of that design.

User Stories insist that the design of the product is done at the last minute, and is a collaboration between a product person and a developer person, and the details are decided during implementation.

So, as can be noticed, the amount of details provided is different using the two approaches, such that, in the User Story for instance, there is a lot of information that is available not available in the requirement, namely, _what_ is we are trying to achieve with the feature.

Others go and mention that a functional requirement is a _formal_ specification that allows one to know exactly if the software works or not. Whilst a User Story is an _informal_ way to describe a need of one of the User Stories, such that, it doesn’t specify a rigid specification to determine if the software is valid or invalid. Although you can test some part of the User Story, its real completion is when the user says : “Yes, this solves my problem”.

We thus realize that the User Story is a huge paradigm shift in the way to approach the work to be done. A contract here is not made, rather, you are trying to help your user to solve a problem. If you don’t see your user stories as discussion tools with a real user, then you are actually not using User Stories.

This post can grow bigger and bigger, and seems that when people attempt describe the notions “User Story” and “user requirement”, such descriptions come from their experience, and how they use each of them. Going through the comparisons above may not reveal clearly the differences between both terms. For that, we chose to interview Agile experts about this issue, for which answers will be shown in the next post.

Stay tuned until then, and don’t hesitate to share your views in this topic, and how you approach those two terms.

 [1]: http://www.productivecome.com/
 [2]: mailto:abder-rahman.a.ali@ieee.org
 [3]: http://www.twitter.com/abderhasan
 [4]: http://agilemanifesto.org
 [5]: http://en.wikipedia.org/wiki/User_story#History
 [6]: http://www.mountaingoatsoftware.com/agile/user-stories
 [7]: http://www.chambers.com.au/glossary/software_requirements_specification.php
 [8]: http://programmers.stackexchange.com/questions/212834/user-story-vs-requirement