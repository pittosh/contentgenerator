---
title: Unstructured Information Management Architecture SDK for Healthcare IT applications
author: Shahid N. Shah
type: post
date: 2005-12-24T11:17:37+00:00
url: /2005/12/24/unstructured-information-management-architecture-sdk-for-healthcare-it-applications/
oc_commit_id:
  - https://www.healthcareguy.com/2005/12/24/unstructured-information-management-architecture-sdk-for-healthcare-it-applications/1478768972
views:
  - 1660
dsq_thread_id:
  - 44283304
categories:
  - Opinion

---
IBM&#8217;s alphaWorks has announced an update to their [Unstructured Information Management Architecture SDK][1]. It&#8217;s a fascinating tool for use in our industry, though it was not designed specifically for healthcare applications. As we all know the majority of healthcare information is unstructured in nature but we try to force it into a particular structure because as IT people we like to reduce things to a relational data model where possible. We do this because there are lots of tools and technologies available to store, query, format, report, convert, and maintain relational data. Of course the Intersystems (Cache) guys will always argue that their database has offered &#8220;dynamically structured&#8221; data but that&#8217;s not quite the same thing as what I&#8217;ll be talking about here.

The UIMA SDK puts a new spin on information management:

> Unstructured information management (UIM) applications are software systems that analyze unstructured information (text, audio, video, images, etc.) to discover, organize, and deliver relevant knowledge to the user. In analyzing unstructured information, UIM applications make use of a variety of analysis technologies, including statistical and rule-based Natural Language Processing (NLP), Information Retrieval (IR), machine learning, and ontologies. IBM&#8217;s UIMA is an architectural and software framework that supports creation, discovery, composition, and deployment of a broad range of analysis capabilities and the linking of them to structured information services, such as databases or search engines. The UIMA framework provides a run-time environment in which developers can plug in and run their UIMA component implementations, along with other independently-developed components, and with which they can build and deploy UIM applications. The framework is not specific to any IDE or platform. 

How it works:

> UIMA is an architecture in which basic building blocks called Analysis Engines (AEs) are composed in order to analyze a document. At the heart of AEs are the analysis algorithms that do all the work to analyze documents and record analysis results (for example, detecting person names). These algorithms are packaged within components that are called Annotators. AEs are the stackable containers for annotators and other analysis engines.
> 
> How Annotators represent and share their results is an important part of the UIMA architecture. To enable composition and reuse, UIMA defines a Common Analysis Structure (CAS) precisely for these purposes. The CAS is an object-based container that manages and stores typed objects having properties and values. Object types may be related to each other in a single-inheritance hierarchy. Annotators are given a CAS having the subject of analysis (the document), in addition to any previously created objects (from annotators earlier in the pipeline), and they add their own objects to the CAS. The CAS serves as a common data object, shared among the annotators that are assembled for an application. 

If you build health IT applications, you owe it to yourself to look beyond structured information and relational databases. By using modern techniques such as natural language processing and text mining you can make useful applications without forcing your users to do click through a myriad of menus and nested combo boxes.

 [1]: http://www.alphaworks.ibm.com/tech/uima?open&ca=dat-aw&S_TACT=105AGX21&S_CMP=AWATOM