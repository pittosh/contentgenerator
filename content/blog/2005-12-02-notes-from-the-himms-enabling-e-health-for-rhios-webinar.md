---
title: Notes from the HIMMS “Enabling e-Health for RHIOs” Webinar
author: Shahid N. Shah
type: post
date: 2005-12-01T22:07:26+00:00
url: /2005/12/02/notes-from-the-himms-enabling-e-health-for-rhios-webinar/
oc_commit_id:
  - https://www.healthcareguy.com/2005/12/02/notes-from-the-himms-enabling-e-health-for-rhios-webinar/1478768943
views:
  - 1082
dsq_thread_id:
  - 44283206
categories:
  - Opinion

---
I attended the HIMMS _Enabling e-Health for RHIOs_ webinar, presented by Sun Microsystems, this afternoon. Overall I found it informative, not too vendor-preachy, and generally filled with practical knowledge. Mike Haymaker and Wayne Owens from Sun and Dr. Steven Carson, CMO of San Diego&#8217;s CMS, presented the deck. Since I&#8217;m a technologist who happens to know healthcare informatics (not a healthcare person looking to learn about technology) I found the two Sun folks knowledgable but I really like what Dr. Carson had to say. Even though the webinar was generally a sales pitch for Sun&#8217;s Enterprise Suite (which they recently open-sourced) and their &#8220;turnkey&#8221; RHIO implementation solution, I found the presentation devoid of Sun worship (which was great).

Dr. Carson was talking about the San Diego RHIO case study (the project was called MINE). The San Diego MINE RHIO has 35+ hospitals, 70 clinics, 378 pharmacies, 7,000 physicians, and radiology labs, nursing homes, health plans, and public health portals in their network. Pretty impressive. In San Diego, he said they started a RHIO but weren&#8217;t sure what it would become. He went on to say that physicians typically see RHIOs as pie in the sky and may feel the government or NHIN has to drive it. But, San Diego wanted to improve quality and not worry about what the government was or wasn&#8217;t going to do so they just started drilling deep into it. Based on his MINE experience, I found some of the stuff Dr. Carson talked about compelling:

  * If you start a RHIO, try not to call it that since RHIOs are seen as pie in sky dreams that may have unattainable goals. In the San Diego example he said they called theirs an HIE (health information exchange). I&#8217;m not sure what changing the name does, but apparently he thought that calling it an HIE and not a RHIO at least got it off the ground. 
  * Don&#8217;t count on grants to start or run a RHIO. If you get grants, that&#8217;s fine but be sure to have a sustainable business model because you _will_ run out of grant funds. Count on between $2 and $5 million in investments based on the size and scope of the RHIO.
  * Make sure docs pay something to get into the network (even if it&#8217;s just &#8220;yellow pages&#8221; type money of $50 a month).
  * Since the biggest benefits of a RHIO occur for health plans, get them involved early and often and have them pay for much of it. 

What&#8217;s most disappointing is that the discussion started off by Wayne (from Sun) and then Dr. Carson both saying that RHIOs (er, HIE) were mainly for patient safety. But, there was very little discussed about how, after instituting a working RHIO, safety was improved in San Diego. Perhaps that will come in a later study.

Wayne mentioned that there are four types of RHIOs:

  * Hospital driven
  * Payer driven
  * Employer driven
  * Physician driven

Wayne said, and Dr. Carson echoed, that the reason for the relative success of the San Diego HIE (er, RHIO) was that it was a grass roots, physician driven, effort. That by getting the toughest customers (physicians) on board first they were able to rope in the payers, hospitals, labs, etc. They didn&#8217;t mention if they got any employers though.

I think the SD MINE project did some smart things &#8212; they didn&#8217;t focus on clinical data sharing (the hardest to homogenize and standardize). Instead, they concentrated on things like providing a portal for HHS and patient education information, linking groups together to find homes for uninsured, universal credentialing, tracking hospitalized patients for UM, community immunization registry, and a community diabetes registry. By concentrating on real-value initial projects with short and successful implementations they got people to buy in early. I liked that. If they focused on trying to share clinical data first they probably would have gotten bogged down.

Now, that doesn&#8217;t mean they&#8217;re not concentrating on the EHR goal of a single patient centric view. Sun purchased a company called SeeBeyond that provides a tool to create a virtual patient record without requiring a centralized database and the MINE project uses that product. SeeBeyond includes stuff like eligiblity and benefit verification, clinical inquiry of labs/meds/ER, prescriptions, order entry, clinical messaging, referrals, and throws in a bit of decision support as well. Sun says they offer an online demo of this tool but I didn&#8217;t get a chance to see that yet. Maybe I&#8217;ll report on that later.

Towards the end of the presentation they took some questions (including from yours truly) and answered them the best they could over the phone. The questions were about how long it takes to setup a RHIO, how many users make it a real useful network, how much does it cost, and how the network topology looks. I wish the presentation was only half the length it was and we could have had more questions and discussions but hey, we can&#8217;t have everything. I can post the answers if anyone&#8217;s interested (I have the notes).

The best thing that came out from it is that RHIOs aren&#8217;t just pie in the sky if you can come up with tangible, real-world benefits and get a good business model together that will sustain it. They mentioned it takes only a few people to run the thing once it&#8217;s up and running (not counting development). So, it&#8217;s not out of scope for even small communities to give it a try.

Oh, and if you want to learn more about the Sun solutions, hit the [Sun Healthcare][1] site. Hey, I had to put that in &#8212; I&#8217;m a _Java_ architect, after all!

 [1]: http://www.sun.com/healthcare