---
title: 'Guest Article: 8 Mistakes to Avoid when Securing Cloud Services'
author: Shahid N. Shah
type: post
date: 2012-07-26T16:28:04+00:00
url: /2012/07/26/guest-article-8-mistakes-to-avoid-when-securing-cloud-services/
oc_commit_id:
  - https://www.healthcareguy.com/2012/07/26/guest-article-8-mistakes-to-avoid-when-securing-cloud-services/1478770808
dsq_thread_id:
  - 780981424
categories:
  - Cloud Computing
  - Engineering
  - Information Assurance (IA) and Security

---
_There’s solid demand these days for services like DropBox.com or Box.net that allow easy but secure file sharing to occur with proper privacy restrictions and audit tracking. I was pleasantly surprised to learn that there are a few companies, such as [FolderGrid][1], trying to solve the problem of HIPAA-compliant file sharing. What FolderGrid is doing, though, is quite unique in healthcare – creating infrastructure software for other health IT developers to build on top of. I reached out to Eric Simmerman, CTO at FolderGrid as well as head of IT and Chief Security Officer at [Pascal Metrics][2], a Patient Safety Organization (PSO). I asked Eric to give us some lessons he’s learned and what mistakes we should avoid while both building and evaluating cloud services for the healthcare marketplace. Here’s what Eric wrote back:_

In the race to avail yourself of the many benefits of cloud computing, don&#8217;t leave behind security as you pursue the convenience of ubiquitous availability. It&#8217;s tempting to equate newer technology and services with better fundamentals. But as recent headlines have demonstrated even the most established firms have been caught using inadequate and in some cases negligent practices when securing their customers&#8217; sensitive data.

If you are an engineer building a new cloud service or a prospective user evaluating the security policies of a service provider &#8211; the following eight commandments are meant to help you avoid some of the vulnerabilities that have already led to account compromises and sensitive data disclosures. No such list could hope to be comprehensive and this one is meant only to establish what should actively be avoided as a bare minimum. If your service requires higher than standard security measures, such as those subject to HIPAA or PCI compliance, you should run kicking and screaming from any vendor who fails to adhere to these simple tenets.

1. Don&#8217;t forget to salt your passwords

A [cryptographic salt][3] is a string added to your password before it is encrypted using a [one-way function][4]. It is a vital element in protecting passwords as LinkedIn learned to their dismay this June when [6.5 million of their users&#8217; passwords][5] were posted to a Russian user forum. Because these passwords had not been salted [over 60% of them were cracked][6] immediately using simple dictionary attacks or similar techniques. Salting passwords is a trivial act (on both the implementation and operational fronts) and not salting the passwords of a modern system is simply negligent.

2. Don&#8217;t use MD5 hashing for password encryption

When chip maker [Nvidia admitted up to 400,000][7] users of its forums had their encrypted passwords compromised in early July, the passwords were revealed to have been [unsalted and encrypted as MD5 hashes][8]. MD5 was [declared “dead” by reknowned security expert Bruce Schneier][9] over seven years ago and is now widely regarded as dangerously insufficient. Best practices mandate the use of a significantly more complex cipher such as [bcrypt][10].

3. Don&#8217;t expose sensitive data through lazy design

Sloppy construction of a modern user interface can lead to a platform that leaks data unintentionally. As the use of “[AJAX][11]” technologies has grown, web and mobile applications commonly “push” large amounts of data to the end user&#8217;s device where it can be used to support multiple views and operations without the need to issue a new request. This leads to generally better user experience and perceived application performance.

Unfortunately, [careless use of these techniques can leak sensitive information][12] leaving seemingly well protected systems hugely vulnerable.

4. Don&#8217;t use a common key for encrypting multiple users data

You wouldn&#8217;t rent an office in a building where every door used the same lock and every tenant was issued the same key. Likewise you should insist that distinct keys be used for encrypting your sensitive data in the cloud. Using a common encryption key for multiple users&#8217; data subjects all of those users to additional risk of compromise. If just one object encrypted with that common key is successfully attacked – every other object encrypted with the same common key is potentially vulnerable.

On a multi-tenant platform this is even more important since there is a very real possibility that one or more of your users or tenants could act maliciously to intentionally compromise the common key and thereby gain access to other tenants&#8217; data.

As an example of proper design, [Amazon&#8217;s Server Side Encryption Support uses a unique key for every object][13] stored. Unfortunately, it seems that [not every vendor offering to encrypt sensitive data at rest][12] adheres to this policy.

5. Don&#8217;t use reset token without expirations

Every service with human users and passwords needs some form of password reset process. These are typically implemented using a “reset link” or “temporary password” which is emailed to the email address of record for a user requesting a reset. Unfortunately, most services fail to adhere to the best practice of expiring these temporary credentials after a short period.

As this month&#8217;s [compromise at Yahoo][14] demonstrates, email accounts are prime targets for virus propagation, malware distribution, and identity thieves. Well designed cloud services should avoid storing a valid password in an email any longer than is absolutely necessary to support the password reset process. Expiration after 15 minutes is a good rule of thumb.

6. Don&#8217;t save user passwords on mobile devices or shared workstations

In the Yin versus Yang battle of security and usability, security concerns often give way to the usability demands of end-users. When a cloud service installs an app on a shared workstation or a mobile device, users often expect that they&#8217;ll only be required to login to that service once. Unfortunately, for an app to keep a user authenticated indefinitely it must persist the user&#8217;s password in an insecure way rendering the security of the service dependent upon the security of the device.

If the app can store and read the password after a restart or a sign-out then an attacker with [access to][15] [the device][15] can do the same. [Evidence abounds][16] that you should not equate physical possession of a device with authorization for a service.

7. Don&#8217;t persist authentication tokens

The last commandment dealt with the storing of a user&#8217;s password and ensuring that the password could not be misappropriated by a malicious user with access to the same workstation. This commandment is similar but reminds us that protecting the password while permitting authentication through other persisted means is equivalent to “kicking the can down the road”.

[Dropbox suffered some embarrassing and unwanted publicity][17] for failing to adhere to this one after users discovered they could surreptitiously access all the files in anyone&#8217;s account by simply copying one file from the victims computer.

8. Don&#8217;t fail to support integration with modern workflows

There&#8217;s an old security adage that states “_The more secure you make something, the less secure it becomes”_. Why? Because when security gets in the way, well-meaning users develop workarounds that defeat the security. Hence the prevalence of doors propped open by wastebaskets and of passwords pasted on the front of monitors.

When we translate that lesson to the realm of cloud services it implies that you must support the needs of your users with modern tooling and workflow integration. If you don&#8217;t want users downloading sensitive files from your service and emailing them to colleagues then your service must provide a convenient means of distribution and collaboration. If you don&#8217;t want your users to share a common set of credentials then make credentialing and delegation as simple as possible.

These are early days for cloud service providers and unfortunately many are cutting corners in their push to market. When you&#8217;re evaluating a service provider&#8217;s security policy a bit of due diligence today can save you [significant pain tomorrow][18]. And if you&#8217;re building the service itself, you should need no further convincing that adhering to these eight commandments is a good start.

 [1]: http://foldergrid.com/
 [2]: http://www.pascalmetrics.com/
 [3]: http://en.wikipedia.org/wiki/Salt_(cryptography)
 [4]: http://en.wikipedia.org/wiki/One-way_function
 [5]: http://mashable.com/2012/06/06/6-5-million-linkedin-passwords/
 [6]: http://nakedsecurity.sophos.com/2012/06/06/linkedin-confirms-hack-over-60-of-stolen-passwords-already-cracked/
 [7]: http://www.washingtonpost.com/world/europe/chip-maker-nvidia-says-up-to-400000-users-encrypted-passwords-compromised-in-attacks/2012/07/13/gJQAqgaeiW_story.html
 [8]: http://www.custompcreview.com/news/nvidia-forums-hacked-pt-2-passwords-not-salted-store-compromised/
 [9]: http://www.schneier.com/blog/archives/2005/06/more_md5_collis.html
 [10]: http://en.wikipedia.org/wiki/Bcrypt
 [11]: http://en.wikipedia.org/wiki/Ajax_(programming)
 [12]: http://blog.foldergrid.com/2012/07/why-we-stopped-trusting-egnyte-a-cautionary-tale-for-users-of-cloud-services/
 [13]: http://aws.amazon.com/about-aws/whats-new/2011/10/04/amazon-s3-announces-server-side-encryption-support/
 [14]: http://www.pcworld.com/article/259135/hackers_publish_over_450000_emails_and_passwords_stolen_from_yahoo.html
 [15]: http://news.cnet.com/8301-13579_3-20099899-37/apple-loses-another-unreleased-iphone-exclusive/
 [16]: http://www.secnap.com/support/whitepapers/laptop-loss-costs.html
 [17]: http://dereknewton.com/2011/04/dropbox-authentication-static-host-ids/
 [18]: http://www.networkworld.com/news/2011/041511-epsilon-breach-senate.html