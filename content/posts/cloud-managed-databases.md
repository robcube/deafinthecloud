---
title: "Cloud Managed Databases"
date: 2019-06-18T13:37:21-06:00
draft: false
---
In many organizations right now, I see and hear of pushbacks from DBAs (Database Administrators) in moving stuff into cloud-based managed databases such as RDS or Azure databases. Managed databases does cost more and the cloud providers aren't afraid to admit it: they're showing you a straight flush before you even start the ante. It shows they're confident of the value managed databases brings to an organization.

Database Administrators are usually on call 24/7 and they're paid very well because of that. As an incentive not to be woken up at 2am, they metliciously care for the databases under their watch, giving them plenty of TLC. That's the nature of the job and that's what they're there for. With cloud-provided managed databases entering the picture, the glass bowl that is their databases are shattered and the day-to-day challenges are no longer there. Cloud win #1.

With cloud-based managed databases, DBAs would focus more time to optimize queries that users may have struggled with, learn more about alternatives to RDBMS such as Big Data and NoSQL so they may better suggest fits with the workflow that might not be exactly ideal for RDBMS (Relational DataBase Management Systems). DBAs would have more time to manage and design databases correctly rather than worrying about the extra work involved with maintenance, backups, and ensuring ample disk space. DBAs will have time to do some deep-thinking and explore database theory -- being more strategic-focused rather than task-focused. Once repetitive tasks can be commoditized via managed databases, then we shouldn't be doing them, let the machine do it for us. More wins, #2.

Managed database providers usually do database tuning and they're always constantly improving their offerings based on lessons learned from the huge cloud community. On-prem DBAs, even while they're very good, only learn lessons within their sphere of influence, or perhaps something happened in their previous jobs that they created preventable workarounds. DBAs learn best practices by reading blogs, talking to peers, or read database documentation -- that in itselves might not be enough to create a perpetually optimized database server. Even you admit it's a hard job! Win #3.

Cloud database providers have tools a-plenty to help you migrate in and out of cloud-based databases (and those same tools also helps you migrate out so no hard feelings). You'd configure how the backups should work, define scalability ratios, and identify areas where you may reduce costs. Putting your database on the cloud, you'll more likely see massive speed improvements in queries probably because you're running on a 3-year old hardware while cloud providers runs on constantly updated hardware. That's win #4.

Another HUGE cost savings using databases on the cloud -- elimination of most user-level licenses -- resulting in less paper-pushing, so to speak, and compliance audits. That's indubitably a win #5 (or a clear winner!).

There are many supplmentental tooling available to interact with cloud-based databases such as dbt, PowerBI, Tableau, et al. Many vendors are embracing the cloud and there's no reason why you shouldn't. Many third-party vendors have tools to allow you to switch cloud providers as people do move from one vendor to another occassionally -- or help you build a multi-cloud platform, i.e. AWS &amp; Azure to minimize perceived cloud vendor lock-in.

There's always learning curves involved with this, as with anything else really! I hope you get some good takeaways from this write-up to help you or your boss to justify moving to the cloud.
   
