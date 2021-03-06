---
title: "Jenkins Amazon EC2 Plugin"
slug: jenkins-amazon-ec2-plugin
date: 2012-11-21 22:32:28 -0600
category: 
external-url: https://wiki.jenkins-ci.org/display/JENKINS/Amazon%2BEC2%2BPlugin
hash: d51032dd07ec279d9145a709547f8aa5
year: 2012
month: 11
scheme: https
host: wiki.jenkins-ci.org
path: /display/JENKINS/Amazon%2BEC2%2BPlugin

---

Allow Jenkins to start slaves on EC2 or Ubuntu Enterprise Cloud (Eucalyptus) on demand, and kill them as they get unused.With this plugin, if Jenkins notices that your build cluster is overloaded, it'll start instances using the EC2 API and automatically connect them as Jenkins slaves. When the load goes down, excessive EC2 instances will be terminated. This set up allows you to maintain a small in-house cluster, then spill the spiky build/test loads into EC2 or another EC2 compatible cloud.
