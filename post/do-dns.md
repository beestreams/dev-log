---
title: "Digital Ocean DNS"
date: 2019-08-02T14:08:27+02:00
draft: true
---

# Digital Ocean DNS Management
I am currently experimenting with using the digital ocean API. After half an hour I am very tempted to make a simple GUI that has our needs in mind. The plan is to make a master droplet that we can use to spin up new sites. If we also can manage DNS for at least staging, that is a big bonus.

## So far …
The process has been really smooth so far. I have a test domain on loopia.se that I have changed Nameservers on to use digital ocean. Via the DO API I have set up a sub-domain on Digital Ocean and pointed an A record to our Demo server IP. In a few hours I might know if it worked.

## Next steps
I'm not sure how we will manage the domain on the actual droplet yet. The current plan is to have an SSH key with access that can modify the server block. I probably should use something like Ansible, but I'm not convinced the setup is worth it. If I just have a template serverblock that can be sent over and then magically update with certbot I think that is enough.