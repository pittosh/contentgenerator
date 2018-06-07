---
title: Look beyond traditional health IT tools for Accountable Care Organization (ACO) implementations
author: Shahid N. Shah
type: post
date: 2011-04-04T12:48:46+00:00
url: /2011/04/04/look-beyond-traditional-health-it-tools-for-accountable-care-organization-aco-implementations/
oc_commit_id:
  - https://www.healthcareguy.com/2011/04/04/look-beyond-traditional-health-it-tools-for-accountable-care-organization-aco-implementations/1478770732
dsq_thread_id:
  - 270664050
categories:
  - Uncategorized

---
As you&#8217;re probably already aware, CMS has announced the Medicare Shared Savings Program for Accountable Care Organizations or ACOs. The new program is another incentive program, like Meaningful Use (MU), but unlike MU there are no penalties for not participating in the program. In my opinion the ACO program is far more lucrative and likely more disruptive than MU and likely to yield, if done right, more patient quality improvements than MU. Having said that, you should see an ACO as a possibility only if you were able to tackle MU – if you’re struggling with MU implementations, you’ll probably be faring worse with ACO implementations.

Just as we saw in 2009 that almost every health IT vendor was touting their support for MU, now we’re going to see a natural addition of a “we are ready for ACOs” message by vendors going forward. But, unlike MU which ONC and NIST nicely laid out with a formal test process with fairly low barriers to entry, the technology required for ACOs isn’t as well defined.

Don’t be fooled into buying health IT applications that promote an “ACO in a box” solution. There is no such technology and there really can’t be. ACOs are not a technology problem; they are a business model problem first and until the business side has decided how it will (a) identify savings and (b) share those savings any purchase will likely be useless.

When you’re approached by vendors trying to sell you their solution with a new “ACO” sticker slapped on it, ask them the following questions:

  * How does your product help me _identify_ shared savings areas (show me what you look for)?
  * How does your product help me _produce_ shared savings (show me how)?
  * How does your product help me _calculate_ shared savings (what algorithms, what procedures)?
  * How does your product help me _distribute_ the shared savings (tools, techniques)?

The IT required for MU is a quite different from what is required for ACOs and will be nowhere as easy for existing legacy EHR to simply retool their current platforms like they could for MU. That’s why you’ll need to look beyond traditional health IT vendors for your ACO solutions.

Here what to look out for:

  * **Getting data out of your systems through business intelligence and reporting**. MU is mostly (in Phase 1) about getting data _into_ your systems with a little outward sharing. Data collection is something that we’ve been doing for decades – even before MU came along we knew how to build systems that can collect and store data in databases. What most of us have never been good at, though, is getting data _out_ in a useful way. Now with ACOs, business intelligence, reporting, and analytics _across_ dozens of _disparate_ systems is a real requirement. Today we all have problems getting data out from a single departmental EHR to help with billing inquiries and clinical decisions support – with ACOs you not only have to be able to pull data and tie it together with departmental and local systems _within_ your organization but _outside_ your organization as well. It’s all technically feasible but requires a little different way of thinking and lots of external coordination that we’re not all quite familiar with.
  * **Data integration for analytics capabilities.** This doesn’t mean we toss in HL7 routers and hope for the best. Most (even unsophisticated) IT environments have the ability to send messages from one system to another. That’s call “transferring” data – which we’ve been doing for decades. _Integrating_ data, though, means much more – the ability to store and understand information in data marts, data warehouses, and clinical data stores / repositories from a variety of sources. Having an EHR, even a centralized one, does not mean you’re ready for data integration – you need tools beyond what health IT firms provide. Traditional data integration vendors should be getting most of your attention here as opposed to healthcare-specific.
  * **Granular clinical data sharing**. The ability to integrate data in your own health system is one thing; being able to share granular (discrete values) that same data across your ambulatory practices, lab partners, and other shared providers is going to require health information exchanges (HIEs) of varying levels of sophistication. Early on you might even need to try to bypass HIEs and create your own local exchange using the Direct Project to make sure you’re in control. By using the Direct Project to transfer secure data between partners and building your data marts and warehouses outside traditional EHR walls will be your best architecture bet.
  * **Billing and pricing data sharing**. Sharing of clinical data is one thing, which we’re already used to doing in the analog world (charts, documents, faxes, etc). However, sharing of financial and billing (and pricing) data is something most organizations don’t do today and will need to get better at. Regardless of how good your EHR is or how much money you’ve spent on MU implementations, billing and pricing data sharing is something you won’t be able to implement without a sophisticated data integration strategy so you’ll need to look beyond your traditional health IT vendors here as well.
  * **Aggregate data sharing**. If you’re not sure you can do granular data sharing for billing or clinical data (which is likely early possibility), you can try aggregate data sharing. Aggregate data sharing is easier to get past governance but most of the HIEs aren’t ready to do aggregate sharing yet (the standards aren’t in place).
  * **Sharing clinical effectiveness evidence (evidence-based medicine, EBM).** One of the important features the CMS Shared Savings Program for ACOs is trying to promote is more evidence-based medicine. Most of us aren’t very good at tracking care through EBM practices – this is another area that is not a technical problem; in fact, everything we need for EBM exists technically. What don’t exist are the sophisticated, repeatable processes (during daily care management) that can track and report the EBM appropriately. This is not a standardization problem but a typical six sigma business management problem.

I haven’t even discussed the patient engagement, coordination of care, beneficiaries management, eligibility management, and other related topics that need to be integrated and shared. Getting ACOs off the ground is going to be tough but I think worth it.