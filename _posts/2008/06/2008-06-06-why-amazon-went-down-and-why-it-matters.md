---
title: "Why Amazon Went Down, and Why It Matters"
slug: why-amazon-went-down-and-why-it-matters
date: 2008-06-06 17:32:17 -0500
category: 
external-url: http://gigaom.com/2008/06/06/why-amazon-went-down-and-what-it-means-to-you/
hash: b94adaeab77d5022cf3af0837114ff24
year: 2008
month: 06
scheme: http
host: gigaom.com
path: /2008/06/06/why-amazon-went-down-and-what-it-means-to-you/

---

Amazon.coms U.S. retail site became unavailable around 10:25 AM PST, and now appears to be back up.  Amazons not naming names  all that director of strategic communications Craig Berman would say was that: Amazons systems are very complex and on rare occasions, despite our best efforts, they may experience problems.  Berman did confirm, however, that neither Amazon Web Services nor international sites were affected.  So what happened? Lets look at the facts.   Traffic to https://www.amazon.com was getting there. So DNS was configured properly to send traffic to Amazons data centers. Global server load balancing (GSLB) is the first line of defense when a data center goes off the air. Either GSLB didnt detect that the main data center was down, or there was no spare to which it could send visitors. When traffic hit the data center, the load balancer wasnt redirecting it. This is the second line of defense, designed to catch visitors who werent sent elsewhere by GSLB. If some of the servers died, the load balancer should have taken them out of rotation. Either it didnt detect the error, or all the servers were out. This is the third line of defense. Most companies have an apology page that the load balancer serves when all servers are down. This is the fourth line of defense, and it didnt work either. The HTTP 1.1 message users saw shows something that speaks HTTP was on the other end. So this probably wasnt a router or firewall.  This sort of thing is usually caused by a misconfigured HTTP service on the load balancer. But that would happen late at night, be detected, and rolled back. It could also happen from a content delivery network (CDN) not retrieving the home page properly.  So my moneys on an AFE or CDN problem. But as Berman notes, Amazons store is a complex application and much of their infrastructure doesnt follow normal data center design. So only time (and hopefully Amazon) will tell.  Site operators can learn from this: Look into GSLB, and make sure you have geographically distributed data centers (possibly through AWS Availability Zones.) Its another sign we cant take operations for granted, even in the cloud.
