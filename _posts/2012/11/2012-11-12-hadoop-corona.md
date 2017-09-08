---
title: "Hadoop Corona"
date: 2012-11-12 16:21:00 +0000
external-url: https://github.com/facebook/hadoop-20/tree/master/src/contrib/corona
hash: 9c8423c347028ef74a8a71bfee096860
annum:
    year: 2012
    month: 11
hostname: github.com
---

Hadoop Corona is the next version of Map-Reduce. The current Map-Reduce has a single Job Tracker that reached its limits at Facebook. The Job Tracker manages the cluster resource and tracks the state of each job. In Hadoop Corona, the cluster resources are tracked by a central Cluster Manager. Each job gets its own Corona Job Tracker which tracks just that one job.