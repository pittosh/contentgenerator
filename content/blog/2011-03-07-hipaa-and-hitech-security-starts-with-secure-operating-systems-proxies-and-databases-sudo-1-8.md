---
title: HIPAA and HITECH security starts with secure operating systems, proxies, and databases (Sudo 1.8)
author: Shahid N. Shah
type: post
date: 2011-03-07T13:35:33+00:00
url: /2011/03/07/hipaa-and-hitech-security-starts-with-secure-operating-systems-proxies-and-databases-sudo-1-8/
oc_commit_id:
  - https://www.healthcareguy.com/2011/03/07/hipaa-and-hitech-security-starts-with-secure-operating-systems-proxies-and-databases-sudo-1-8/1478770725
dsq_thread_id:
  - 5181429526
categories:
  - Uncategorized

---
I spend a lot of time talking with CEOs, CIOs, and other senior executives about what HIPAA security and HITECH privacy policies really mean. I hear a lot of naive talk about how systems are secure because &#8220;we use SSL encryption&#8221; or &#8220;we&#8217;re secure because we have a firewall&#8221;. Anybody who&#8217;s been security and privacy work for more than a few months would know how false those statements are.

Security (whether it&#8217;s for HIPAA, HITECH, or banks) starts with secure operating systems, databases, and other infrastructure elements like proxies and firewalls and the depth of security is really controlled by system admins. Your systems are only as secure as the servers and firewalls they are sitting on so you have to ask yourself: &#8220;what have my system admins and security people done to secure my infrastructure?&#8221;.

Let&#8217;s start with a relatively simple question that all CIOs should know the answer to &#8212; who has access to root permissions on UNIX / Linux server or &#8220;Administration&#8221; role in a Windows server across the enterprise? If you don&#8217;t have an easy answer  to that, then no amount of paper policy will make you HIPAA compliant.

All servers require a super user or privileged account to do some of the most important activities like installing applications, creating file systems, and other mundane but important and sometimes dangerous tasks. If you have a policy of sharing a single account (like root in Linux or &#8220;Administrator&#8221; in Windows) you&#8217;ve got serious security flaws. These days proxies and firewalls are often Linux servers as well so your policies about root access are even more important.

One thing security professionals like me suggest is to never allow root logins (or Administrator logins). Instead, use security wrapping tools and policy enforcement where a person logs in using their own credentials and then can do specific actions which are logged thoroughly.

Windows Server 2008 on up has this policy-style security built-in but on Linux/UNIX you should make sure that you use **sudo**. This past week we saw the [release of Sudo 1.8][1], an important upgrade which brings pluggable policies to this venerable security utility. Here&#8217;s a snippet from the announcements at ServerWatch.com:

> This weekend at [SCALE][2], Todd Miller [introduced Sudo 1.8][3], a major update that brings &#8220;enterprise&#8221; features to Sudo that put it on par with proprietary alternatives.
> 
> We&#8217;re all familiar with the venerable utility [Sudo][4], but its feature set hasn&#8217;t kept up with what many companies want for root access control. Specifically, Sudo has lacked support for policy plugins and advanced logging features. There have been a number of proprietary <a id="itxthook0" rel="nofollow" href="http://www.serverwatch.com/tutorials/article.php/3926646/Sudo-18-Brings-Pluggable-Policies-to-Root-Access-Control.htm#">tools</a> that either replace or enhance Sudo for root access control (RAC). But who wants to have to buy an add-on if you can get the features you need as part of the native toolset that comes with your *nix?
> 
> Sudo 1.8 brings a plugin architecture, with two major types of plugins: policy and I/O logging plugins.
> 
> The policy plugins are designed to control who can do what on the system. You&#8217;re probably used to controlling Sudo via the `/etc/sudoers`. If this works for you, nothing changes. You&#8217;ll still be able to use `visudo` to edit the file and add users, and set policies the way you always have. Otherwise, it&#8217;s now possible to write new policies to comply with things like SOX and HIPAA, or tie Sudo into Active Directory for companies that have standardized on that. Sudo will accept only one policy plugin at a time.
> 
> The I/O plugins control logging of sessions that take place using Sudo. Sudo has had a &#8220;replay&#8221; command since 1.7.3, but this release brings much more functionality. Unlike the policy plugin, Sudo can support multiple plugins for I/O, so you could use different I/O policies depending on which users are running Sudo (for example). You can now not only see what commands have been run with Sudo, but also actually replay a session in its entirety if need be (and if you want to log that much).

 [1]: http://www.serverwatch.com/tutorials/article.php/3926646/Sudo-18-Brings-Pluggable-Policies-to-Root-Access-Control.htm
 [2]: http://www.socallinuxexpo.org/
 [3]: http://www.socallinuxexpo.org/scale9x/blog/interview-todd-miller-sudo-maintainer
 [4]: http://www.gratisoft.us/sudo/