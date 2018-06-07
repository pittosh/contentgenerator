---
title: How to manage tape backups in health IT shops
author: Shahid N. Shah
type: post
date: 2006-01-31T02:08:12+00:00
url: /2006/01/31/how-to-manage-tape-backups-in-health-it-shops/
oc_commit_id:
  - https://www.healthcareguy.com/2006/01/31/how-to-manage-tape-backups-in-health-it-shops/1478768997
views:
  - 2037
ratings_users:
  - 1
ratings_score:
  - 4
ratings_average:
  - 4
dsq_thread_id:
  - 44283382
categories:
  - Opinion

---
These days we&#8217;re hearing more and more about how backup tapes, which are crucial for business continuity and disaster recovery purposes, are getting lost due to carelessness or transfer problems. Many of you are CXOs in charge of technology and information systems and I&#8217;m hoping you have had a chance to review your off site backup tape storage policies. Off site storage is crucial if you use backup tapes so that a fire or other disaster doesn&#8217;t take along your backups with your primary systems. However, about 30% of you still don&#8217;t put your backup tapes in off site storage. This was true of a number of hospitals and care providers in Louisiana and Mississippi and they lost significant data. There&#8217;s no getting it back.

If you are going to backup your systems to tape, you need to have a mechanism to track them. Backup tapes are a favorite means by which company insiders take off with information and thieves will also try to steal data through backup tapes.

Most stories that reveal data theft through backup tape transfers forget to mention something important: thieves take backup tapes because they can easily get data off them. Most db admins and system admins don&#8217;t do simple stuff like _encrypt their data on backup tapes_. If you&#8217;re responsible for your IT department please be sure to check that all data on backup tapes are encrypted. It&#8217;s easy to do and in case your backup tapes are ever stolen it won&#8217;t give the thieves an easy mark. Oh, and don&#8217;t use simple symmetric encryption &#8212; make it a bit harder by apply dual key encryption or something more difficult to crack.

The moment a backup tape is created, it needs to be uniquely identified and labeled. Try using a barcode if possible. At the time the tape is created, the ID of the tape should be entered into a physical and electronic log. The physical log should be just a log book with signatures and the electronic log can be a simple spreadsheet that can be searched later. A physical and electronic log should be kept in your primary and secondary locations. There should be columns in the log that track who created the tape, what&#8217;s on it, and who it was handed to (courier service, etc). If a courier service picks up the tapes (not a good idea unless they are specialists) they need to sign off appropriately and ensure that the courier is known by name and logged in the log book and spreadsheet.

After identification and labeling, but before transfer, the backup tape should be put under lock and key in a lock box. If you are not using a courier service (a good idea), one of your staff should be made responsible for getting the transfer done and ensuring logs on both side (source and destination) are filled out properly. An executive (or manager) should review the logs regularly to make sure there are no discrepancies.

None of these techniques I&#8217;ve discussed is inexpensive or trivial to implement. However, if you&#8217;ve got a solid process in place you can keep the name of your organization out of the newspapers. Something your boards and CEO might appreciate :-).

By the way, if you&#8217;ve got a little bit more cash you can eliminate backup tapes altogether and create an active disaster site with full electronic backups in a secondary location. This way, there are no issues with transfers, tapes, etc. For example, I have clients that have a primary data center and then a secondary data center where we store snapshots (backups) on hard drives instead of tapes. Then, the snapshots are placed onto optical media and stored in the secondary location in a vault.