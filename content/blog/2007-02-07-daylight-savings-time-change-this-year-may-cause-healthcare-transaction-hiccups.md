---
title: Daylight Savings Time change this year may cause healthcare transaction hiccups
author: Shahid N. Shah
type: post
date: 2007-02-07T15:39:45+00:00
url: /2007/02/07/daylight-savings-time-change-this-year-may-cause-healthcare-transaction-hiccups/
oc_commit_id:
  - https://www.healthcareguy.com/2007/02/07/daylight-savings-time-change-this-year-may-cause-healthcare-transaction-hiccups/1478769112
views:
  - 6915
dsq_thread_id:
  - 5179361402
categories:
  - Opinion

---
</p> 

_This article was initially posted at_ [_HISTalk_][1]_. However, the issue is important and I&#8217;ve received good feedback on the readiness of medical devices from Tim Gee of_ [_Medical Connectivity_][2] _and I wanted to share his thoughts here as well._ 

As we all probably know by now, this year Daylight Savings Time (DST) starts on March 11 instead of in April. Daylight-saving time has usually started on first Sunday of April and reverted to standard time on the last Sunday in October. However, due to the US Energy Policy Act of 2005, the daylight-saving schedule will be extended by a month, with the period beginning on the second Sunday in March and ending on the first Sunday in November. At first glance this is not a big deal, clocks will just move ahead by an hour three weeks earlier; however, given that most modern healthcare environments are networked and networked systems need to synchronize using price time servers we may be in for some headaches. 

Some people compare this to “Y2K” upgrades but let’s not kid ourselves, it’s nowhere as big or as time-consuming as Y2K. That’s just FUD that consultants want to promote to get more work. 

However, here are just _some_ symptoms we will see if we’re not up to speed with the DST changes: 

  * Missed meetings and appointments 
      * Hospital orders not being picked up in time 
          * Operating room scheduling issues 
              * Billing and contract deadline issues 
                  * Record compliance and management problems due to time-correlation mismatch 
                      * Transportation of biologics blood bags, tissue, etc 
                          * Expiration of biologics and supplies 
                              * Transportation of supplies and short-lived medications 
                                  * Security-related issues where log files need to be correlated 
                                      * “Smart” medical devices which work on time-based controls (pumps, vital signs, etc) 
                                          * I’m sure there are dozens of other symptoms that the esteemed audience of this blog will be able add (put them in comments so we can all keep an eye out for them).</ul> 
                                        <font color="#697c83"><a href="http://www.medicalconnectivity.com">Tim Gee</a> added this specifically about medical devices:</font>
                                        
                                        > Many medical devices create data that includes the date and time – diagnostic imaging modalities, 12-lead ECG carts, continuous patient monitors, just to name a few. About any device that prints a strip chart, creates an image or report will include the date and time that the data was generated. Data from devices must have the proper date and time so that patient data can be represented accurately. Data tagged with the wrong date and time could result in critical data being missed or misinterpreted, resulting in an adverse patient event.
                                        
                                        What do you do today? 
                                        
                                          1. Make sure everybody knows the change and is looking out for issues. 
                                              * Immediately read [Windows: Preparing for daylight saving time changes in 2007][3]. Act on it ASAP – especially keep in mind that unsupported systems won’t have patches from Microsoft. 
                                                  * If you have unsupported systems, check out [Global DST update tool for all versions of Windows from NT4 through Server 2003 and Vista][4] (not from Microsoft and costs $500). You can also use [Unofficial DST patch for Windows 2000][5] (free). 
                                                      * If you are running Java, check out their [article on how to upgrade][6]. 
                                                          * If you’re running UNIX systems, run the following command to see what the following command returns: zdump -v /etc/localtime | grep 2007. If it doesn’t return the proper dates you’ll need to patch your system (contact your vendor – the Linux, AIX, Sun, etc patches are all ready). 
                                                              * Contact the vendors of all your medical devices and see if their devices are compliant or what patching needs to be done. Most may _not_ be ready. 
                                                                  * Contact the vendors of all your patient-related software (OR scheduling, patient scheduling, lab management, etc) to see if they’re ready. &nbsp;Most _should_ be ready – especially if they get their times and DST rules from the operating system. 
                                                                      * Contact the vendors of your billing systems and financial systems to get their patches. Most of the big names already have patches ready.</ol> 
                                                                    [Tim Gee][2] also added:
                                                                    
                                                                    > The more sophisticated systems already sync to a time server on the hospital’s network. The challenge for hospitals will be to identify the devices that are not automatically time synched, and ensure that they are updated (and configured) to support the daylight savings changes or manually reset when daylight savings occurs. Biomedical engineering may already have a list of effected or vulnerable devices, and in any event they are the best source for identifying and tracking vulnerable systems will be your biomeds.
                                                                    
                                                                    If you’ve already called device vendors, software vendors, consultants, etc please share your thoughts as comments here (or send me an email and I will summarize it into another blog posting).

 [1]: http://www.histalk.com
 [2]: http://www.medicalconnectivity.com
 [3]: http://www.microsoft.com/windows/timezone/dst2007.mspx
 [4]: http://www.sharpebusinesssolutions.com/dst2007.htm
 [5]: http://www.intelliadmin.com/blog/2007/01/unofficial-windows-2000-daylight.html
 [6]: http://java.sun.com/developer/technicalArticles/Intl/USDST/