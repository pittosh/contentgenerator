---
title: 'Guest Article: What will make healthcare software usable?'
author: Shahid N. Shah
type: post
date: 2009-04-13T11:04:50+00:00
url: /2009/04/13/guest-article-what-will-make-healthcare-software-usable/
oc_commit_id:
  - https://www.healthcareguy.com/2009/04/13/guest-article-what-will-make-healthcare-software-usable/1478770473
  - https://www.healthcareguy.com/index.php/archives/5391239621588
oc_metadata:
  - '{		version:1.0,		tags: {}	}'
ratings_users:
  - 4
ratings_score:
  - 18
ratings_average:
  - 4.5
dsq_thread_id:
  - 5160061516
categories:
  - Opinion

---
</p> 

_Last month I posted several entries about how difficult most healthcare software is to use – those articles garnered lots of “yes, you’re right” type of comments along with a number of emails asking for help on how to improve usability. Usability describes the "ability to use" something &#8212; the goal for a usable system is to make it easy to use. Given how hard it is to actually make something easy to use (yes, ironic), I invited an expert in this field &#8212; Paul Nuschke, a usability specialist at_ [_Electronic Ink_][1] _– to write about what it takes to make software usable, with emphasis on healthcare IT systems. Paul went beyond a simple introduction to the field and gives specific advice to software designers; it&#8217;s clear these guys know what they are doing. If you’re building a new EMR (and hey, we have billions of dollars to spend now so what are you waiting for?) please take Paul’s advice:_

In a [previous post on this blog][2], three prototypes compared simple experiences using Apple and Google products with the complicated experience found in Healthcare Information Systems (HIS). However, the diagrams begged the question: if an application cannot be as simple as a search field and a Submit button, how can they be usable? Is simplicity the only way to make usable software?

Fortunately, practitioners in the design and usability field have been studying this problem for a long time. In this article, I am going to summarize three essential attributes of usable software that apply to HISs and Electronic Health Records (EHR). To be considered usable, applications should be easy to learn, efficient, and they should prevent errors.

**Easy to learn**

Imagine a nurse logging into an EHR application for the first time. Does he or she know what to do next? Or does the nurse need a day of training before being able to start? What about a rotating physician or a per diem nurse who uses a system once every few months? Can they remember how to use it? 

With EHRs, your medical providers most likely need training, they commonly forget key system terminology, and they probably forget how to use key portions of the system. Why does this happen? Briefly, it happens because those systems require providers to learn about the system. The systems force providers to learn new vocabulary, workflows, and annoying number of system “quirks.” Instead of being a tool that supports patient care, these systems can disrupt and change the way that care is delivered. 

Well-designed software is easy to learn and allows its users to get work done right away. Imagine for a moment an alternative, easy-to-learn system that meets the following requirements: 

  * Uses terminology already familiar to users 
  * Does not force users to memorize system codes, phrases, and terminology (e.g., see image below) 
  * Allows users to follow familiar task flows 
  * Does not require users to recall lengthy procedures that are not familiar to them 
  * Hides systems processes that are irrelevant to the user 
  * Shows icons and images that users can readily identify 
  * Presents both textual and graphic information in a clear way 
  * Reduces the amount of information clutter 
  * Provides intuitive ways to navigate through the application 
  * Gives users help exactly where they need it 
  * Allows users to explore and make errors without severe consequences 

&#160;

<img src="http://healthcareguy.blueserf.com/uploads/2009/04/vista-orders-small.png" alt="vista-orders-small" title="vista-orders-small" width="601" height="227" class="alignnone size-full wp-image-540" srcset="/img/uploads/2009/04/vista-orders-small.png 601w, /img/uploads/2009/04/vista-orders-small-300x113.png 300w" sizes="(max-width: 601px) 100vw, 601px" />

Figure 1: What are "Delayed Orders"? Why are certain orders blue? Why are CAPS used? These all require users to learn.

When an application fails to deliver on each of these requirements, it becomes cumbersome, complicated and difficult to use. To put it another way: if you are a patient do you want your providers using a system that doesn’t meet these requirements?

Unfortunately, instead of fixing the problems, most EHR companies like to explain that their software is complicated. They have convinced CIO’s and CTO’s that training can overcome any confusion and is a necessary part of any complex system. In the design community, we see training as a symptom of poorly designed software. The reason is rather simple—applications require training because they do not work in a way that most people find intuitive and they contain information and terminology that does not make sense to users. 

**Efficient**

How quickly and easily can users complete their tasks? Efficient applications are not only technically sound, supporting quick page load times, but they also provide an optimal task flow for both novice and expert users and a visual design that facilitates quick understanding and information retrieval. 

Unfortunately, EHRs are anything but efficient. Providers often spend more time documenting their patient care, and less time actually providing that care, than when they used paper records. In the design world, since nearly every application has some type of data entry form, a set of best practices has evolved about how to design efficient forms. Given the importance of the data entry part of the process, you would think that EHRs would be at the cutting edge of form design. Instead, you have forms that use the wrong input fields and that suffer from poor layout, lack of shortcuts (e.g., using “tab” to advance), and many other issues. 

Making matters worse, once information is in the system, providers and administrators have a lot of difficulty finding it. Why? Because EHR developers have spent virtually no time trying to format or organize the information in a way that makes sense. How can you tell? The systems display the information using logic that is similar to the database structures that contain it, resulting in two approaches. The worst approach is to dump all of the information onto one page, forcing providers to sift through hundreds of fields often irrelevant to their current task. Or they group the information by data type (e.g., prescriptions), placing each group on a separate tab (see figure below). This tab system forces users to navigate and recall information from multiple tabs. Not only does this additional cognitive load reduce efficiency, but it can also lead providers into making costly errors.

&#160;

<img src="http://healthcareguy.blueserf.com/uploads/2009/04/vista.png" alt="vista" title="vista" class="alignnone size-full wp-image-541" width="600" srcset="/img/uploads/2009/04/vista.png 834w, /img/uploads/2009/04/vista-300x208.png 300w, /img/uploads/2009/04/vista-768x532.png 768w" sizes="(max-width: 834px) 100vw, 834px" />

Figure 2: Is this a good use of space? What is currently happening with this patient? Oh, that&#8217;s on a separate screen.

Given how far current systems are from supporting efficient work, you might be wondering what one looks like. Consider the simplistic example of <u>Google’s search</u>. Novices know that they can simply type text into the textbox and press “Google Search”. Eventually these users learn that entering more search terms narrows the results. They might also learn that they can use modifiers like “OR” and “define:” to further narrow results. Recognizing that users need help constructing searches and spelling certain words, after they begin typing Google provides a list of suggestions that further helps users refine their search:

&#160;

<img src="http://healthcareguy.blueserf.com/uploads/2009/04/google-suggestions.png" alt="google-suggestions" title="google-suggestions" width="600" class="alignnone size-full wp-image-547" srcset="/img/uploads/2009/04/google-suggestions.png 774w, /img/uploads/2009/04/google-suggestions-300x147.png 300w, /img/uploads/2009/04/google-suggestions-768x376.png 768w" sizes="(max-width: 774px) 100vw, 774px" />

Figure 3: Google suggesting searches. Note how it doesn&#8217;t force you to choose one.

What can more complicated applications learn from this interface? Translating these characteristics into general requirements, an efficient system:

  * Allows users to follow familiar task flows (e.g., enter text in textbox and click button or press Return) 
  * Does not require users to recall lengthy, unfamiliar procedures (e.g., registering before use) 
  * Hides systems processes that are irrelevant to the user (e.g., database query language) 
  * Presents both textual and graphic information in a way that is clear 
  * Reduces the amount of information clutter where possible (e.g., the copious white space on every Google page) 
  * Provides intuitive ways to navigate through the application (e.g., Next buttons on the search results page) 
  * Provides shortcuts for advanced users (e.g., “define:”), while providing more obvious mechanisms for novices to accomplish the same tasks (e.g., simply searching) 
  * Provides decision support tools that aid rather than force decision making (e.g., drop-down list with suggestions) 
  * Prioritizes information in a way that supports tasks (e.g., best result listed first) 

In these requirements, note the overlap between efficiency and learnable systems. This is not an accident: Learnable systems are almost always more efficient, especially for novice and intermediate users. Moreover, learnable systems are less prone to errors, my next topic.

**Prevent Errors**

Consider Dennis Quaid’s well-known case: when his twin infants were being treated in the hospital for a staph infection, they were both accidentally given the adult dose of a blood thinner that was 1000 times higher than standard for infants. The same error had happened at another hospital with six infants, where three infants died. What circumstances led the medical providers to make this mistake? How could the same error type happen repeatedly? The packagings for the different doses of medication were nearly identical, causing providers to confuse the different doses even when they were being vigilant. This “persistence” is one indicator of a particularly onerous usability problem.

IT practitioners have become accustomed to thinking of errors in terms of system crashes and pop-up messages with arcane system terminology like “Error Number: 1249245. Please try again.” For medical providers, discussion about errors involves “medical errors,” like when a surgeon operates on the wrong body part, or as in the example above, when the wrong dosage of a medication is given. In the usability field, we have a more expansive definition: errors happen every time an action does not result in the desired outcome.

Through our research, we know that behind these errors is a system or a process that virtually assures an error is going to happen. Designs that do not take into account human limitations and context-of-use will always lead to errors. For example, suppose that you designed the following form:

<img src="http://healthcareguy.blueserf.com/uploads/2009/04/date.png" alt="date" title="date" width="273" height="74" class="alignnone size-full wp-image-549" />

How can such a simple form create errors? Because it requires users to recall which date format they need to use. Is it “mmddyyyy”, “mm/dd/yy”, or if you’re European, “dd/mm/yy”? How does the system recover from your error? Does it wipe out all of your data and force you to start all over again? 

As in the Dennis Quaid case, errors also occur when people misinterpret information. In particular, the form in which data is presented can greatly affect how people interpret it. Consider the following “Order Details” text box from VistA:

&#160;

<img src="http://healthcareguy.blueserf.com/uploads/2009/04/vista-order-details.png" alt="vista-order-details" title="vista-order-details" width="521" height="448" class="alignnone size-full wp-image-548" srcset="/img/uploads/2009/04/vista-order-details.png 521w, /img/uploads/2009/04/vista-order-details-300x258.png 300w" sizes="(max-width: 521px) 100vw, 521px" />

Figure 4

This “Orders Details” screen broaches a number of questions. What was this order? Was it completed? Why was the attending physician listed so prominently? Why was it formatted in plain text? What does “>>” mean? Why are certain bits of information in CAPS? Why is “Order Text” indented? 

This screen essentially a dump of information contained in the database. Imagine being a tired and hurried physician trying to wade through it to find the piece of relevant information. What if they miss “unreleased”? Maybe the patient sits in their bed for an extra two hours because the physician forgot to “sign” the order.

While catastrophic medical errors get news attention, providers typically experience many of these “small” errors in a given day. We don’t hear about these smaller errors very often for two reasons. First, users often attribute the problem to their failure to remember the system’s rules (e.g., “I should’ve remembered that date format!”). Second, amazingly, many hospitals are contractually obligated not to talk about the errors. In any case, these errors add up to decreased efficiency, lost income, distrust of the system, frustration amongst providers, and worsened patient care.

Preventing errors, improving efficiency, and making the systems easier to learn is a tall order for the EHR industry. As this blog attests, there are several roadblocks—including interoperability and system architecture—that stand in the way. However, with more attention to design and usability, EHR vendors can make large and immediate strides towards improving their systems. Should they need help, there is an entire design industry that has been underutilized and that is, believe it or not, even excited to help improve these applications.

 [1]: http://www.electronicink.com/
 [2]: https://www.healthcareguy.com/index.php/archives/467