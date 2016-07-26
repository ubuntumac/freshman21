---
published: true
title: The backtick / tilde key outputs less than or greater than
layout: post
author: Tim
category: articles
tags:
- bug
- keyboard layout
- programming issues
- confirmed
- fix
- hack

---

This was an issue for me from install. Upon first starting up, I tried to get into terminal and perform something, and when I tried to use the tilde key to reference my home directory, it outputted the greater than sign. The backtick, I found, outputted the less than sign.

The solution feels like a bit of a hack, because it's not directly affecting a configuration for this specific issue. However, until I find a better solution (figure out how to manage key mappings) I'm going to be using it.

Add this line into your `/etc/rc.local` file:

```
echo 0 > /sys/module/hid_apple/parameters/iso_layout
```

Reference: ["AskUbuntu Answer"](http://askubuntu.com/a/627483)
