---
layout: post
title: Android ListView Set Height Properly
description: Proper way to set ListView height to fill its container
modified: 2015-9-8
category: android
tags: [Android, Software, ListView]
comments: true
share: true
featured: true
---

Looking around the internet I've seen several ways to set the height of a ListView.  Upon 
further reading I came across a *best* way.  One thing I learned is a ListView should never 
be nested inside a ScrollView since the ListView grows to hold all its contents (makes 
sense once you hear that, right?).  

I wasn't directly adding the ListView to the ScrollView, instead I had a fragment 
container which I used to swap in and out views and the ScrollView was the parent of my 
parent container.

# The layout

<script src="https://gist.github.com/jamesbyars/7acce25a885bf1c6efb5.js"></script>

