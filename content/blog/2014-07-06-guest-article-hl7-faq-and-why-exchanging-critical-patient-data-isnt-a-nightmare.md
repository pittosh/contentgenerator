---
title: 'Guest Article: HL7 FAQ and why exchanging critical patient data isn’t a nightmare'
author: Shahid N. Shah
type: post
date: 2014-07-06T20:44:06+00:00
url: /2014/07/06/guest-article-hl7-faq-and-why-exchanging-critical-patient-data-isnt-a-nightmare/
featured_image: /uploads/2014/07/HL7-FAQ-and-why-exchanging-critical-patient-data-isn’t-a-nightmare.jpg
oc_commit_id:
  - https://www.healthcareguy.com/2014/07/06/guest-article-hl7-faq-and-why-exchanging-critical-patient-data-isnt-a-nightmare/1478770870
  - https://www.healthcareguy.com/guest-article-hl7-faq-and-why-exchanging-critical-patient-data-isnt-a-nightmare/1420178795
dsq_thread_id:
  - 5158139749
oc_metadata:
  - |
    {		version:'1.1',		tags: {'featured': {"text":"Featured","slug":"featured","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'health-level-7': {"text":"Health Level 7","slug":"health-level-7","source":{"_className":"SocialTag","url":"http://d.opencalais.com/dochash-1/c2cb2127-9fd2-3c08-b2bd-e20d10619def/SocialTag/5","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/tag/SocialTag","name":"SocialTag"},"name":"Health Level 7","makeMeATag":true,"importance":1,"normalizedRelevance":1},"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'standards-organizations': {"text":"Standards organizations","slug":"standards-organizations","source":{"_className":"SocialTag","url":"http://d.opencalais.com/dochash-1/c2cb2127-9fd2-3c08-b2bd-e20d10619def/SocialTag/4","subjectURL":null,"type":{"_className":"ArtifactType","url":"http://s.opencalais.com/1/type/tag/SocialTag","name":"SocialTag"},"name":"Standards organizations","makeMeATag":true,"importance":1,"normalizedRelevance":1},"bucketName":"blacklisted","bucketPlacement":"user","_className":"Tag"}, 'data-management-tools': {"text":"Data Management Tools","slug":"data-management-tools","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'interface-technologies': {"text":"Interface Technologies","slug":"interface-technologies","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}, 'medical-informatics': {"text":"Medical Informatics","slug":"medical-informatics","source":null,"bucketName":"current","bucketPlacement":"auto","_className":"Tag"}}	}
categories:
  - Cloud Computing
  - HL7
tags:
  - Data Management Tools
  - Featured
  - Health Level 7
  - Interface Technologies
  - Medical Informatics

---
_I recently saw a demo of the [Decisions.com][1] platform and left impressed with the workflow engine, business rules execution, forms automation, and data integration platform. I&#8217;m very familiar with almost all the major HL7 routers and integration engines out there but Carl Hewitt, Founder and Chief Architect at Decisions, is releasing something fairly unique &#8212; an visual HL7 interface definition and integration platform for use by analysts and non-technical personnel charged with healthcare data connectivity across business workflows. I found their approach unique enough that I&#8217;ll be something that I don&#8217;t do often &#8212; a review. But, before I post the review in the coming days, I reached out to Carl to help set the stage and share the most common questions and answers we get about HL7._

**What is HL7?**

HL7 is how healthcare applications talk to each other – for example, when a patient is admitted to a facility, when a patient schedules an appointment, when a lab test is ordered, or when a medication is prescribed an HL7 message can be sent from one system to another. HL7 is what disparate systems use to tell each other about patient activity. HL7 is a widely adopted text based communications standard created in 1987 that can run on almost all modern hardware and software systems that support the standard.

The HL7 specification is governed by Health Level Seven International, a not-for-profit, ANSI-accredited standards developing organization.

**How do HL7 systems communicate?**

HL7 is human readable text that is broken up into meaningful sections and sent as data packets from application to application across well defined communication mechanisms with handshaking and acknowledgement procedures.  Because the data is sent over widely adopted communication mechanisms in a readable format (i.e., text that can be opened on any computer), HL7 tends to work pretty well.

**What are the various components of HL7 messages?**

Like any technology, HL7 uses a glossary of specific terms that have specific meaning.  While an interface engine alleviates the need to directly integrate with all of these concepts, understanding them will help you know what the HL7 engine is actually doing.

  * **Envelope**: Each communication from one system to another is contained in a block of data.  This block of data (Envelope) could contain one or more messages.

  * **Message**: A message is a set of data that is logically related (for instance, about a specific patient encounter or hospital admission).  A message is bounded by its type (Message Type) and contains a number of (Segments)

  * **Message Type**:  A message type is the definition of the structure of a communication and provides rules for what data sections (Segments) are required, which are optional, and the order of the data.  The order of the data in a message is important as one section (Segment) can have different meanings depending on where it is in the message.  Messages are usually referred to by their message type and event type, for example: an ADT^A01 is an ADT message with an event type of A01 which means that this is an Admission, Discharge, or Transfer type message (ADT) and is signaling the event that a patient was Admitted (A01).

  * **Event**: Events allow a message type to have slightly different meaning as described above.  Events are related to the message type and an important part of the standard.  The same message structure can be used to signal different types of events.  The same basic data is needed to admit and discharge a patient with only small differences.

<p style="padding-left: 30px;">
  HL7 has evolved over many years and new events have been added to the standard that weren’t there in previous versions.  For instance, an ADT A01 (ADT Patient Admit) and an ADT A08 (ADT Patient Data Update) were initially defined as different message types, but later combined.  So, a message that comes in as an ADT A08 in version 2.5 of HL7 will actually have the structure of an ADT A01, however, because it is sent as an A08 &#8211; the meaning of the message will be an update.  Confusing?  No worries, most interface engines hide this fact and make you think you are still getting an A08.
</p>

  * **Segment**: A segment is a section of a message that contains the actual values that are being sent between systems.  Generally, a segment can be thought of as a line in a message and it always starts with an identifier that indicates what the segment type is.  An example of a segment is “PID” (patient identifier) where information about a person or patient is sent, or “MSH” (message header) which is described below.  Segment identifiers are always 3 characters.

  * **Message Header**, **MSH Segment**:  Every message starts with an MSH segment that declares information about the message including its version, type, which text delimiters are used, etc.  This special segment is used to provide information as to how to interpret the entire message.

  * **Optional**, or **Z Segments**:  HL7 is a flexible standard and allows for users to send data between systems that the specification does not accommodate.  This is done by using a Z segments, which is a custom segment with an identifier that starts with Z.  Most people use the Z and then follow it with characters that are part of the specification.  For example, to send additional data about a patient identity someone might use ZID, a derivative of PID.

  * **Data Type**:  Every segment is composed of data elements.  Each of these data elements has a “type.”  Types may be number types like integer and decimal or dates, or more complex types defined by the standard.  These data types are positional in the ‘segment line’ and delimited by the defined character (usually a pipe, |) for the message.  A data type might have one or more pieces to it (itself being delimited by another delimiter).  For instance, a ‘Code’ data type has an ID and Description, but it is one element inside the segment.

  * **Delimiters**:  While the characters that can break up a message are by convention pretty standard, they can be defined in the MSH segment.  Each message segment is always on a new line, and each segment is subdivided into data by a pipe character, ‘|’, and each data type is subdivided into its elements by a caret, ‘^’.  See example message below for more information.

  * **ACK/NAK**:  Acknowledge or NOT acknowledge the receipt of a message.  Most HL7 systems can be configured to send back receipts of communication.  This allows systems to keep a careful audit of data sent between them.  Sending systems can generally be configured to resend or at least report messages that get no receipt or get a NACK (not acknowledge message) returned.

  * **Interfaces**:  An interface can mean slightly different things between software and hardware vendors, but essentially an interface is usually a connection between two systems.  When an HL7 data feed is configured from the Emergency Department in a hospital to the Electronic Medical Record system this is usually referred to as an interface.

<p style="padding-left: 30px;">
   Some interfaces are one way &#8211; they either send data to another system or listen to data from another system.  Most interface engines or interface technologies support sending and receiving data as these technologies normally sit in between two medical systems and modify the messages as they are sent.  Different interface engines might have functionality to transform or route messages attached to interfaces.
</p>

**How are HL7 text messages transmitted?**

There are two primary technologies used to send message in most healthcare applications: TCP and Files.

  * **Direct Connection (TCP)**:  Data can be transmitted over a network connection using TCP (also referred to as LLP or MLLP).  This is often referred to as a ‘direct’ connection or a real time connection between applications.
  * **File Connection**:  A simpler way of transmitting messages is by sending the data in a file or multiple files.  This can involve loading it into an application or configuring a directory to watch for new files to appear.  A file connection can also take the form of an FTP or SFTP server.

**What does an HL7 Message Look like?**

HL7 messages are made up of segments. Each carrying specific information about anything from a patient’s name to an allergy, a radiology image, a transcript, etc.

> <pre>MSH|^~\&|MegaReg|XYZHospC|SuperOE|XYZImgCtr|20060529090131-0500||ADT^A01|01052901|P|2.5
EVN||200605290901||||200605290900
PID|||56782445^^^UAReg^PI||KLEINSAMPLE^BARRY^Q^JR||19620910|M||2028-9^^HL70005^RA99113^^XYZ|260 GOODWIN CREST DRIVE^^BIRMINGHAM^AL^35 209^^M~NICKELL’S PICKLES^10000 W 100TH AVE^BIRMINGHAM^AL^35200^^O |||||||0105I30001^^^99DEF^AN
PV1||I|W^389^1^UABH^^^^3||||12345^MORGAN^REX^J^^^MD^0010^UAMC^L||678 90^GRAINGER^LUCY^X^^^MD^0010^UAMC^L|MED|||||A0||13579^POTTER^SHER MAN^T^^^MD^0010^UAMC^L|||||||||||||||||||||||||||200605290900
OBX|1|NM|^Body Height||1.80|m^Meter^ISO+|||||F
OBX|2|NM|^Body Weight||79|kg^Kilogram^ISO+|||||F
AL1|1||^ASPIRIN</pre>

In the message above you’ll notice some things that are ‘bold’ to call your attention to them.

  1. MSH the message header segment identifies the message.
  2. ADT^A01 shows us that we have a patient being admitted (A01) and the message structure is an ADT message.
  3. EVN is the event data with some key dates like when the message was sent
  4. PID is the patient identifier.  This has medical record numbers, names, and contact information.
  5. PV1 is the patient visit data which details this specific visit to a facility.
  6. OBX is an observation, like vitals taken by a nurse
  7. AL1 is the description of patient allergies

**What type of data does HL7 Transmit?**

The HL7 specification is fairly comprehensive.  It contains data about many aspects of health care and data including patients, schedules, appointments, interactions between providers and patients, insurance information, information on diagnoses and procedures, medical records and much more.  If an application is configured to receive all messages of all types from another application, it is likely that much of the data that is received is not relevant to what is needed.  For instance, if I have a scheduling application, it might not be relevant for me to get information on updates of patient allergies &#8211; but changes to patient demographic information is very important.

**What are challenges with HL7 in the Healthcare Enterprise?**

A growing challenge with contemporary Healthcare IT Solutions is the “app-centric” approach many vendors are taking to solving problems. With more and more of these enterprise apps being designed as standalone systems, Healthcare IT teams are faced with unique integration challenges involving sensitive patient health information.

Many teams are trying to figure out how to implement a data layer that can bring all of the healthcare provider systems (billing, lab, patient, etc.) and partner systems together so each has access to the data that it needs. Some are taking home grown approaches with custom message services and open source technologies. Others are discovering a new breed of data management tools. Let’s take a closer look at what some of the primary tools have been and what some of the new tools look like.

There are a number of unique challenges to handling a standard driven data structure such as:

  * Handling multiple versions to and from multiple sources.
  * Complicated nesting
  * Non-conformity
  * Communication Infrastructure
  * Dirty data
  * Cost of Integration

&nbsp;

 [1]: http://www.decisions.com/