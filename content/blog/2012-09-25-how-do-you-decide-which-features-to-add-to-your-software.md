---
title: How do you decide which features to add to your software?
author: Shahid N. Shah
type: post
date: 2012-09-26T00:50:30+00:00
url: /2012/09/25/how-do-you-decide-which-features-to-add-to-your-software/
oc_commit_id:
  - https://www.healthcareguy.com/2012/09/25/how-do-you-decide-which-features-to-add-to-your-software/1478770811
dsq_thread_id:
  - 5159500802
categories:
  - Engineering
  - Implementation
  - Usability
  - User Experience
  - UX

---
Given the well-warranted focus on design these days it’s always difficult to find the right balance between features that we should add to our software and those that we leave out. I was running a class recently on how to build product roadmaps for health IT apps / medical device software and the question of how we should decide which features to add came up. 

Here’s are just a few of the facets I talked about during that lecture:

  * **Will the new feature increase patient safety by a measurable amount?**&#160; This is really hard to measure but only because we rarely do risk management for individual features. Forcing to think about this would be important.
  * **How many new clients would we sign because we had the feature?** This is calculated in whatever way you define _users_ but must be defensible. The sales team usually can help with this but needs input from others (marketing, training, etc).
  * **What specific benefits will the users see because of the new feature?** Be specific with clicks that might be removed, new business that they may win, money they might save, etc. _This is a lot harder to quantify than it seems_. If you can’t quantify the benefits, is it worth implementing? Why or why not?
  * **Is the feature something our users require due to regulatory burden on their side?** These include functionality like MU requirements, HIPAA, or CMS rules. If your customer has a regulatory burden that your product can handle, give it higher priority even if customers don’t ask for it specifically.
  * **How much time (which resolves to money) will it save on implementation at our customer sites?** This is calculated in _minutes per client_ and must be defensible. Usually the IT team can compute this.
  * **How much time (which resolves to money) will it save on training our users?** This should be calculated in _minutes per client_ and must be defensible. Usually the training team can compute this.
  * **How much time (which resolves to money) will it save on tech or product support?** This should be calculated in _minutes per client_ and must be defensible. Usually the training team can compute this.
  * **How much it would cost to develop, QA, and deploy the feature (the development team does this)?**
  * **What kind of positive press or other free PR might the feature create?** This needs to be defensible, not just guesswork.
  * **What is the risk of breaking things (side effects)** for existing users or impacting existing training and knowledge at the clients that will increase support costs because of the new feature?

There are probably a million more considerations but very few of them are easily defensible with good metrics. What kinds of questions do you consider when thinking about new features for your health IT app? I’d love to get your thoughts on how you make such decisions, drop me a comment below.