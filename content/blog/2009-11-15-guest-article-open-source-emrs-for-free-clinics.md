---
title: 'Guest Article: Open Source EMRs for free clinics'
author: Shahid N. Shah
type: post
date: 2009-11-15T17:46:21+00:00
url: /2009/11/15/guest-article-open-source-emrs-for-free-clinics/
oc_commit_id:
  - https://www.healthcareguy.com/2009/11/15/guest-article-open-source-emrs-for-free-clinics/1478770530
dsq_thread_id:
  - 5190841259
categories:
  - Uncategorized

---
_[Kevin Clifford][1] and I were chatting about his experiences in taking a Michigan-area free clinic live on an open source EMR and I was very interested to share it with others. Kevin said he volunteered at the free clinic because he wanted to serve his community and said that there are many other such free clinics in need of IT improvements in Michigan and elsewhere. I asked him to write a quick summary of what he did and how it worked. What Kevin is doing is an excellent example for other IT firms looking to break into healthcare IT &#8212; use open source and other free tools to help your local community clinics and physician offices. Here&#8217;s what Kevin had to say about his experience:_

I recently started volunteering at a free health clinic in Pontiac Michigan. The clinic has 30 doctors and dentists that volunteer their time seeing 500 to 600 uninsured patients per month. The clinic has an in-house pharmacy and three full time employees. I have an I/T background so my original intent was to help the clinic with any technical issues they may have such as setting up their website and network. Once I started working at the clinic I noticed they were having trouble keeping track of patient files and were making all appointments on paper. In addition they had to go through all their files monthly in order to track specific patient categories and follow-up on missing information.

I suggested to the clinic that they try [OpenEMR,][2] an open source EMR system. They liked the demo I showed them and I started the installation. I installed the [OpenEMR appliance][3] which runs on the VMware virtual server, the appliance allowed me to run the LAMP version of OpenEMR on a windows machine. I then configured the appliance so it would use a static IP address.

Once the program was up and running I changed the layouts and added fields for specific information that the clinic needed to collect. The most time consuming and labor intensive part of the install was in transferring all the patient records over to the program. Through the PHPMyAdmin part of the tool I was able to create the SQL queries that allowed the clinic to run the specialized reports that they needed. Our plan at the clinic is to continue exploring the capabilities of OpenEMR in order to improve the clinics efficiency even more.

The program has allowed the clinic to:

  * Schedule patients and doctors electronically
  * Manage patient encounters
  * Save time by running reports on patient data

Due to the current economic environment the number of patients seen at the clinic has risen dramatically over the last year and there is currently a waiting list. There are a number of similar clinics located throughout the country that could improve efficiencies by installing an open source EMR system. I would like to expand the service on OpenEMR implementations to free medical clinics and am looking for thoughts and advice from the community.

If you have any suggestions or are interested in working with me on this endeavor please provide feedback here on Shahid&#8217;s site via comments if you want to speak publicly or if you prefer private communication you can contact me at <kclifford@gmail.com>.

 [1]: mailto:kevinclif@gmail.com "E-mail Kevin"
 [2]: http://www.oemr.org/
 [3]: https://www.healthcareguy.com/2007/01/07/open-source-emr-and-practice-management-software-appliance/341/