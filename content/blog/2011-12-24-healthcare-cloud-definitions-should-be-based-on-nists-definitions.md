---
title: Healthcare Cloud definitions should be based on NIST’s definitions
author: Shahid N. Shah
type: post
date: 2011-12-24T13:59:12+00:00
url: /2011/12/24/healthcare-cloud-definitions-should-be-based-on-nists-definitions/
oc_commit_id:
  - https://www.healthcareguy.com/2011/12/24/healthcare-cloud-definitions-should-be-based-on-nists-definitions/1478770775
dsq_thread_id:
  - 5163805316
categories:
  - Cloud Computing
  - Government Regulations
  - NIST
tags:
  - Cloud; NIST

---
As most of my regular readers know, I work as a technology strategy advisor for several different government agencies; in that role I get to spend quality time with folks from NIST (the National Institute of Standards and Technology), what I consider one of the government’s most prominent think tanks. They’re doing yeoman’s work trying to get the massive federal government’s different agencies working in common directions and the technology folks I’ve met seem cognizant of the influence (good and bad) they have; they seem to try to wield that power as carefully as they know how. Since most of you are in the technology industry, albeit specific to healthcare, I recommend that you learn more about NIST and the role it plays – they can make your life easier because of the coordination and consensus building work they do for us all. I, for one, was thrilled when NIST was picked as the governing body for the MU certification criteria. These guys know what they’re doing and I wish they got more involved in driving healthcare standards.

A few years ago NIST came up with the first drafts of the seminal definitions of _Cloud Computing_; they ended up setting the stage for communicating complex technical concepts and helping making “Cloud” a household name. After 15 drafts, the 16th and final definition was published as [_The NIST Definition of Cloud Computing_][1] (NIST Special Publication 800-145) in September. It’s worth reading because it’s only a few pages and is understandable by the layperson. No computer science degree is required.

Yesterday I was speaking to a senior executive in the EHR space and we had a great discussion on what healthcare providers are doing in terms of cloud computing and how to communicate these ideas to small practices as well as hospitals. It reminded me of the numerous similar conversations I’ve had with other senior executives we serve in the medical devices and other regulated IT sectors. In almost every conversation I can remember about this topic over the past couple of years, I had to remind people that NIST has already done the hard work and that we can, indeed, rely on them. Most of the time the senior executive was unaware of where the definitions came from so I figured I’d put together this quick advisory.

My strong recommendation to all senior healthcare executives is that we not come up with our own definitions for cloud components – instead, when communicating anything about the cloud we should instruct our customers about NIST’s definition and then tie our product offerings to those definitions. The essential characteristics, deployment models, and service models have already been established and we should use them. When we do that, customers know that we’re not trying to confuse them and that they have an independent way of verifying our cloud offerings as real or vapor.

Below I have copied/pasted from NIST 800-145 their key definitions. Imagine how many debates you would avert with technicians at clients when, during conversations with a client, you communicated some of the following information first, showed them how it was a “standard definition” and handed them a copy of the publication, and then mapped your offerings and discussions to the different areas. Your sales teams and the marketing teams would appreciate the clarity, too.

Note that you do not need to map every offering you have to every definition – just start mapping the obvious ones and then figure out how you can communicate the “gaps” as being not applicable to your products / services or if those gaps will be filled in the future as part of your roadmap. Treat these definitions as canonical but not inclusive – meaning that just because your SaaS offering doesn’t fit every essential characteristic doesn’t mean that you’re _not_ “cloud” – it just means _partially_ cloud.

If you’ve got questions about how to map your product offerings, drop me some comments and I’ll assist as best as I can.

Here are the key definitions from NIST 800-145, [copied directly from the original source][2]:

Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management effort or service provider interaction. This cloud model is composed of five essential characteristics**,** three service models, and four deployment models.

**Essential Characteristics:**

_On-demand self-service._ A consumer can unilaterally provision computing capabilities, such as __server time and network storage, as needed automatically without requiring human interaction with each service provider.

_Broad network access._ Capabilities are available over the network and accessed through standard __mechanisms that promote use by heterogeneous thin or thick client platforms (e.g., mobile phones, tablets, laptops, and workstations).

_Resource pooling._ The provider’s computing resources are pooled to serve __multiple consumers __using a multi-tenant model, with different physical and virtual resources dynamically assigned and reassigned according to consumer demand. There is a sense of location independence in that the customer generally has no control or knowledge over the exact location of the provided resources but may be able to specify location at a higher level of abstraction (e.g., country, state, or datacenter). Examples of resources include storage, processing, memory, and network bandwidth.

_Rapid elasticity._ Capabilities can be elastically provisioned and released, in some cases __automatically, to scale rapidly outward and inward commensurate with demand. To the consumer, the capabilities available for provisioning often appear to be unlimited and can be appropriated in any quantity at any time.

_Measured service._ Cloud systems automatically control and optimize resource use by leveraging __a metering capability<sup>1</sup> at some level of abstraction appropriate to the type of service (e.g., storage, processing, bandwidth, and active user accounts). Resource usage can be monitored, controlled, and reported, providing transparency for both the provider and consumer of the utilized service.

**Service Models:**

_Software as a Service (SaaS)._ The capability provided to the consumer is to use the provider’s __applications running on a cloud infrastructure<sup>2</sup>. The applications are accessible from various client devices through either a thin client interface, such as a web browser (e.g., web-based email), or a program interface. The consumer does not manage or control the underlying cloud infrastructure including network, servers, operating systems, storage, or even individual application capabilities, with the possible exception of limited user-specific application configuration settings.

_Platform as a Service (PaaS)_. The capability provided to the consumer is to deploy onto the cloud __infrastructure consumer-created or acquired applications created using programming languages, libraries, services, and tools supported by the provider.<sup>3</sup> The consumer does not manage or control the underlying cloud infrastructure including network, servers, operating systems, or storage, but has control over the deployed applications and possibly configuration settings for the application-hosting environment.

_Infrastructure as a Service (IaaS)._ The capability provided to the consumer is to provision __processing, storage, networks, and other fundamental computing resources where the consumer is able to deploy and run arbitrary software, which can include operating systems and applications. The consumer does not manage or control the underlying cloud infrastructure but has control over operating systems, storage, and deployed applications; and possibly limited control of select networking components (e.g., host firewalls).

**Deployment Models:**

_Private cloud._ The cloud infrastructure is provisioned for exclusive use by a single organization __comprising multiple consumers (e.g., business units). It may be owned, managed, and operated by the organization, a third party, or some combination of them, and it may exist on or off premises.

_Community cloud._ The cloud infrastructure is provisioned for exclusive use by a specific __community of consumers from organizations that have shared concerns (e.g., mission, security requirements, policy, and compliance considerations). It may be owned, managed, and operated by one or more of the organizations in the community, a third party, or some combination of them, and it may exist on or off premises.

_Public cloud._ The cloud infrastructure is provisioned for open use by the general public. It may be __owned, managed, and operated by a business, academic, or government organization, or some combination of them. It exists on the premises of the cloud provider.

_Hybrid cloud_. The cloud infrastructure is a composition of two or more distinct cloud __infrastructures (private, community, or public) that remain unique entities, but are bound together by standardized or proprietary technology that enables data and application portability (e.g., cloud bursting for load balancing between clouds).

 [1]: http://csrc.nist.gov/publications/PubsSPs.html#800-145
 [2]: http://csrc.nist.gov/publications/nistpubs/800-145/SP800-145.pdf