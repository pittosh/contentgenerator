---
title: Client/Server vs. ASP/Web-Based in Healthcare IT
author: Shahid N. Shah
type: post
date: 2009-03-12T15:01:20+00:00
url: /2009/03/12/client-server-vs-asp-web-based-in-healthcare-it/
oc_commit_id:
  - https://www.healthcareguy.com/2009/03/12/client-server-vs-asp-web-based-in-healthcare-it/1478770462
  - https://www.healthcareguy.com/index.php/archives/4981236870081
ratings_users:
  - 1
ratings_score:
  - 5
ratings_average:
  - 5
oc_metadata:
  - "{		version:1.0,		tags: {'encryption': {			text:'encryption',			slug:'encryption',			source:{			url:'http://d.opencalais.com/genericHasher-1/d2987b46-c83f-3511-bc98-c1c814457b69',			type:{			url:'http://s.opencalais.com/1/type/em/e/Technology',			iconURL:'',			name:'Technology'		},			name:'encryption',			nInstances:1		},			bucketName:'current'		},'healthcare-applications': {			text:'healthcare applications',			slug:'healthcare-applications',			source:{			url:'http://d.opencalais.com/genericHasher-1/ea461c6b-861e-3b7c-b584-9cf9f7c5b191',			type:{			url:'http://s.opencalais.com/1/type/em/e/IndustryTerm',			iconURL:'',			name:'IndustryTerm'		},			name:'healthcare applications',			nInstances:1		},			bucketName:'current'		},'citrix': {			text:'Citrix',			slug:'citrix',			source:{			url:'http://d.opencalais.com/comphash-1/4e7af238-044f-3b19-bf5e-841a00a36299',			type:{			url:'http://s.opencalais.com/1/type/em/e/Company',			iconURL:'',			name:'Company'		},			name:'Citrix',			nInstances:1		},			bucketName:'current'		},'mumps': {			text:'MUMPs',			slug:'mumps',			source:{			url:'http://d.opencalais.com/genericHasher-1/65c8cbd9-211f-3658-9396-8a6d9a6cc5e9',			type:{			url:'http://s.opencalais.com/1/type/em/e/MedicalCondition',			iconURL:'',			name:'MedicalCondition'		},			name:'MUMPs',			nInstances:1		},			bucketName:'current'		},'healthcare': {			text:'healthcare',			slug:'healthcare',			source:{			url:'http://d.opencalais.com/genericHasher-1/456f7843-b46a-3245-b537-49661db4c976',			type:{			url:'http://s.opencalais.com/1/type/em/e/IndustryTerm',			iconURL:'',			name:'IndustryTerm'		},			name:'healthcare',			nInstances:1		},			bucketName:'current'		}}	}"
dsq_thread_id:
  - 5162133866
categories:
  - Opinion

---
I get tons of email for healthcare IT advice (which I love, so keep the questions coming) and every once in a while a question comes along that I decide to answer here since I think it will be interesting to many readers. Here’s a great one from yesterday:

> I am a frequent reader of your blog. I find your writing very pertinent to my own business. I run a development shop that creates EMR software and our company is currently in a debate about the future of our application architecture. We are a client/server based application. We sell to small clinics, multi-specialty and large hospital settings. We usually play along side the GE Centricity, NextGen, Meditech and AllScripts EMRs &#8211; interfacing primarily via HL7. We encounter the same issues as any other client/server based application. There are high deployment costs. Implementations and upgrades are very costly.
> 
> Recently I have been pushing the strategy (internally in my company) of moving to an ASP model. I have been evangelizing on the merits of this architecture as a way to cut costs and support a more dynamic delivery model. There are obviously many gains to be had.
> 
> What I was wondering is in your experience how much of the healthcare application space is already using or is moving towards an ASP model? Is the healthcare world comfortable with this paradigm? We have always written off this model as risky due to HIPAA concerns. Why aren&#8217;t the major EMRs going this way? Will they? Won&#8217;t they have to? I just see it as the inevitable evolution.

[![][1]][2]

First, let me thank the reader for the question. I bet he feels alone like the fellow in the picture above :-).

Now, let’s talk about the state of the applications architecture world in healthcare IT. Lots of healthcare applications are still (yes!) running on mainframes and mid-range computer systems connected to “dumb terminals” running text only user interfaces (using in many cases very old but still quite functional MUMPs software). This is the “big iron”.

Most healthcare applications today run on the client/server paradigm with “fat client” applications running either UNIX or Windows on the server and Windows user interfaces on client PCs. This means that the database server is usually on its own computing hardware and the user interfaces (data entry, reports, etc) run on the user’s PCs. Very traditional, tried & true, and things work (but have plenty of deployment issues).

There are only a few pure web-based applications out there in the EMR/EHR world. Of course, the PHR world has tons of web based software (almost exclusively). There are many hybrid solutions out there where legacy EMR vendors have put “web portals” in front of their legacy client/server solutions. These portals are often useful but not as useful as complete web-based systems.

There are many companies that have client/server software but also run in an ASP (application service provider) model by using either Terminal Services or Citrix to provide remote and multi-user access from a single deployment architecture.

To answer the reader’s specific questions:

**In your experience how much of the healthcare application space is already using or is moving towards an ASP model?**

Yes, many healthcare IT providers are using the ASP model. It’s generally safe and if architected properly it works well. Of course the ASP model using client/server architectures is much harder than the web model but it’s certainly achievable using Microsoft and Citrix desktop sharing technologies.

**Is the healthcare world comfortable with this paradigm? We have always written off this model as risky due to HIPAA concerns.** 

Hospitals and large organizations are not necessarily comfortable with external ASP but the small to mid-size market (physicians, small healthcare groups, etc) are comfortable with the model (in fact, they prefer it over on-premise models). However, even the large hospitals and organizations that are uncomfortable using external ASPs would love to use ASP models in their own data centers (in fact, many are requiring it these days).

HIPAA concerns are almost all mitigated these days by using VPNs, leased lines, or other encryption mechanims so it’s really no worry.

**Why aren&#8217;t the major EMRs going this way? Will they?** 

Many are already going this way and those that aren’t will whither away quietly.

**Won&#8217;t they have to?** 

Yes, they will. If EMRs can’t be hosted on premises, in an externally managed ASP, in an internally managed ASP, and “in the cloud” _simultaneously_ they won’t have a long shelf life. All successful EMR vendors will allow multiple deployment models if they really want to grow big. If you want to stay small you can choose one model; if you want to grow big, you will choose a flexible model.

Last words of advice for all software vendors: don’t think that “the cloud” or “ASP” or any specific deployment model will fit all needs. Create a flexible approach using modern web techniques that lets your users tell you how they want things deployed. No single model will work for very long or for a large number of customers.

 [1]: http://farm1.static.flickr.com/44/153225000_698c62c38a.jpg
 [2]: http://flickr.com/photos/18305489@N00/153225000 "UNIX - Server"