---
title: Microsoft Health Common User Interface (CUI) Guidance and Controls
author: Shahid N. Shah
type: post
date: 2007-08-08T16:55:59+00:00
url: /2007/08/08/microsoft-health-common-user-interface-cui-guidance-and-controls/
oc_commit_id:
  - https://www.healthcareguy.com/2007/08/08/microsoft-health-common-user-interface-cui-guidance-and-controls/1478769140
views:
  - 3558
ratings_users:
  - 7
ratings_score:
  - 27
ratings_average:
  - 3.86
dsq_thread_id:
  - 44283788
categories:
  - Opinion

---
Microsoft&#8217;s been tying to make some major inroads into healthcare IT (some impressive, others that are a little &#8220;me too&#8221;). They are strong in the office automation and general computing space in hospitals but weak in the healthcare-specific vertical and clinical areas. One of the areas that Microsoft&#8217;s always been strong is supporting the development community and they&#8217;re starting to make some good progress in health IT (specifically _health_ not the just _IT_ part). I&#8217;m a Microsoft [Solutions Architect MVP][1] and believe me they know how to take care of developers.

Microsoft recently released their [Common User Interface (CUI)][2] documents which provides developers, users, and UI specialists with healthcare-specific guidance.

I&#8217;ve gone through [many of the documents][3] and for people that have been in the business for a while (or like me who have actually _built_ about dozen healthcare systems) much of the information is obvious. However, if you&#8217;re new to healthcare IT and design, I definitely recommend taking a look. Even if you already know the material, it&#8217;s great to base new development on something like this so that your engineers and UI specialists don&#8217;t reinvent the wheel. All development teams need guidelines like these and if you lead a team creating healthcare software you owe it to yourself to take a look and use the guidelines directly or adapt them to your liking.

In addition to the guidelines there are also .NET (ASP.NET and desktop) controls that put into practice much of the guidance. Just be careful that once you start using the controls you may no longer be platform-independent. Before jumping straight into the code, try to adapt the documents and build your own UI standards around it and then see if the controls make sense to use. 

Here are the common user interface guidance areas they&#8217;ve implemented so far:

  * Accessibility 
    
      * [Accessibility Principles][4] 
          * [Accessibility Checklist][5]</ul> 
          * Information Display 
            
              * [Address Information Display][6] 
                  * [Date Display][7] 
                      * [Gender/Sex Display][8] 
                          * [Patient ID Number Display][9] 
                              * [Telephone Number Display][10] 
                                  * [Time Display][11]</ul> 
                                  * Information Input 
                                    
                                      * [Date Input][12] 
                                          * [Time Input][13]</ul> 
                                          * Terminology 
                                            
                                              * [Terminology Matching][14] 
                                                  * [Terminology Elaboration][15] 
                                                      * [Terminology Display Standards][16]</ul> 
                                                      * Medications Management 
                                                        
                                                          * [Medications Views][17] 
                                                              * [Drug Administration][18]</ul> 
                                                              * Patient Administration 
                                                                
                                                                  * [Find a Patient][19] 
                                                                      * [Patient Identification][20]</ul>

 [1]: https://mvp.support.microsoft.com/communities/mvp.aspx?product=1&competency=Visual+Developer+-+Solutions+Architect
 [2]: http://www.mscui.net/
 [3]: http://www.mscui.net/DesignGuide/DesignGuide.aspx
 [4]: http://www.mscui.net/DesignGuide/AccessibilityPrinciples.aspx
 [5]: http://www.mscui.net/DesignGuide/AccessibilityChecklist.aspx
 [6]: http://www.mscui.net/DesignGuide/AddressDisplay.aspx
 [7]: http://www.mscui.net/DesignGuide/DateDisplay.aspx
 [8]: http://www.mscui.net/DesignGuide/GenderSexDisplay.aspx
 [9]: http://www.mscui.net/DesignGuide/PatientNoDisplay.aspx
 [10]: http://www.mscui.net/DesignGuide/TelephoneNoDisplay.aspx
 [11]: http://www.mscui.net/DesignGuide/TimeDisplay.aspx
 [12]: http://www.mscui.net/DesignGuide/DateInput.aspx
 [13]: http://www.mscui.net/DesignGuide/TimeInput.aspx
 [14]: http://www.mscui.net/DesignGuide/TerminologyMatching.aspx
 [15]: http://www.mscui.net/DesignGuide/TerminologyElaboration.aspx
 [16]: http://www.mscui.net/DesignGuide/TerminologyCodedInformation.aspx
 [17]: http://www.mscui.net/DesignGuide/MedicationsOverview.aspx
 [18]: http://www.mscui.net/DesignGuide/MedicationsAdmin.aspx
 [19]: http://www.mscui.net/DesignGuide/PatientFindAPatient.aspx
 [20]: http://www.mscui.net/DesignGuide/PatientIdentification.aspx