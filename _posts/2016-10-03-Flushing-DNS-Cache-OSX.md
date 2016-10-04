---
layout: post
title: Flushing the DNS Cache On OS X
description: How to clear your DNS cache using OS X (Yosemite)
modified: 2016-10-03
category: articles
tags: [OSX, DNS]
comments: true
share: true
featured: true
---

# Why Flush Local DNS Cache?

I've been spending a lot of time lately working on configuring web apps running
on AWS with domains that have been purchased from
[Google Domains](https://domains.google.com/registrar)
(Yea, I have a legitimate reason for not using Route 53, but I'll save that for
another post).

I need to flush DNS cache regularly, like every few minutes in order to validate
my DNS config changes.  I'm leaving the TTL of my records set at 5 minutes.

## The Script

<script src="https://gist.github.com/jamesbyars/8f2967a1d71b9e0e954efec5bf8494be.js"></script>

Please note: I referenced https://support.apple.com/en-bw/HT202516 while creating
this post.

# Still have to wait on DNS

Just because you flush your local DNS cache doesn't mean the change you made
to your DNS record will have propagated through the DNS system.  Use the dig
command to verify your changes have take effect.
