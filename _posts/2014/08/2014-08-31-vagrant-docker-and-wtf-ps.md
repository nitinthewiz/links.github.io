---
title: "Vagrant, Docker and Ansible. WTF? - devo.ps"
date: 2014-08-31 09:15:45 +0000
external-url: http://devo.ps/blog/vagrant-docker-and-ansible-wtf/
hash: 870eee3f0b9d8680e12d267e8489c070
annum:
    year: 2014
    month: 08
hostname: devo.ps
---

And that's why we ended up adding Docker to our development workflow. We were already familiar with it (as it powers some parts of the devo.ps infrastructure) and knew there would be obvious wins. In practice, we are shipping Docker containers in a main Vagrant image and drive some of the customization and upgrade with Ansible.