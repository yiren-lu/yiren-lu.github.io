---
layout: page
title: DNS Relay
description: a tiny DNS proxy written in C
img: /assets/dnsrelay/dnsrelay.png
importance: 1
category: course
---

[👁 on Github](https://github.com/yiren-lu/bachelor-cs/tree/master/dnsrelay)

A DNS relay that answers to DNS resolution requests from clients, integrated with a LRU cache that stores history results. If the required record doesn't exist in the cache, the program will ask the upper DNS server and cache the result, and then relay to the requester. It supports all types of DNS records, and also deletes out-of-date record when necessary. Moreover, it is able to block the resolution of URLs on given blacklist.

See detailed document for further information:

<object data="/assets/dnsrelay/document.dnsrelay.pdf" width="100%" height="1000" type='application/pdf'/>
