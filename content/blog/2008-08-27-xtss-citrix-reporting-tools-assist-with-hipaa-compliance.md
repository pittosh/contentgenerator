---
title: XTS’s Citrix reporting tools Assist with HIPAA Compliance
author: Shahid N. Shah
type: post
date: 2008-08-27T01:47:42+00:00
url: /2008/08/27/xtss-citrix-reporting-tools-assist-with-hipaa-compliance/
oc_commit_id:
  - https://www.healthcareguy.com/2008/08/27/xtss-citrix-reporting-tools-assist-with-hipaa-compliance/1478770413
views:
  - 2026
dsq_thread_id:
  - 5175225910
categories:
  - Opinion

---
It has been some time since I last [wrote about XTS][1], a rapidly growing virtualization management vendor focused on the Citrix market. In my recent interview with Eric Spiegel, CEO, I found out that XTS has had many important changes this year. On the product side, they launched a new, more powerful version of their analysis and reporting solution and renamed it Introspect for XenApp. Although it&#8217;s not designed for it, Introspect is a very useful tool for performing HIPAA compliance checks and audit reports of which users have been accessing specific applications and servers that might contain patient data.

Last week they released a free utility that enables Citrix administrators and architects to easily create configuration reports for their Citrix farms. These configuration reports are the first step to documenting application usage for HIPAA compliance reports.

Unlike the full product Introspect, which is focused on usage data captured in the Resource Manager summary database, the free configuration report generator utilizes the ubiquitous Citrix data store and features the same flexible, easy to use interface that they have always had in Introspect for quickly creating reports exactly the way you need them.

I see it as being useful for the following tasks:

  * Documenting implementations and upgrades 
  * Creating baselines for troubleshooting, audits and disaster recovery 
  * Identifying incorrect server configurations, either to solve a problem or proactively reduce help desk calls 
  * Ensuring consistency of hotfixes across a Citrix farm 

Additionally, integration with Active Directory can be leveraged for better insight into user and application assignments. Other bells and whistles like automated scheduling, report distribution via email and the ability to customize look and feel of report output can also be found in this robust piece of free code. 

Anyone can [download the free configuration report generator][2] from the XTS website. It is currently packaged as a fully functional virtual machine and includes a sample Resource Manager summary database so you can try Introspect&#8217;s starter templates to evaluate the historical usage reporting and analysis capabilities as well. Please also note that they recently simplified their pricing model and now base it on the number of Resource Manager summary databases, which makes Introspect very affordable in my opinion.

If you are a Citrix administrator or architect I suggest checking out this free utility from XTS which will probably help you save time and possibly some headaches in the future. 

If you&#8217;ve already downloaded a copy and tried it, drop us a line here and let us know how it&#8217;s working out.

 [1]: http://shahid.shah.org/index.php/archives/114
 [2]: http://www.xtsinc.com/dnn/ShahidShahlandingpage/tabid/437/Default.aspx