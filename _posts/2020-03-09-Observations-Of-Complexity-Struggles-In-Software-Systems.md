---
layout: post
title: Observations of Complexity Struggles In Software Systems
description: This post will attempt to provide some insight into ways to identify growing complexity and make the argument for effective complexity management
modified: 2020-03-09
category: articles
tags: [software, complexity, process, engineering]
comments: true
share: true
featured: true
---

# Observations of Complexity Struggles In Software Systems

Software systems tend to grow over time as does complexity between components or services.  One of the major challenges in software engineering is managing the complexity of a system (that is, keeping the complexity low) even as the system grows.  This post will attempt to provide some insight into ways to identify growing complexity and make the argument for effective complexity management.

## Common Indicators of Complexity Issues

* Long, manual testing cycles
* Error prone deployments
* General anxiety around deployments
* “We have tests in place but it still broke!”
* Simple changes affect many different pieces of the system
* “Why wasn’t this issue identified in code review?”

## When Complexity Isn’t Managed
In many systems we see complexity increasing faster than the number of changes, or features.  This results in each change to the system being more difficult, time consuming, and risky than the last.

## Effective Complexity Management
When complexity is effectively managed the effort to make a change begins to taper off after a short period of time.  Effective complexity management results in the system being designed to promote change.  Designing for change means designing for safety of change - a way for the system to self-verify the change has not had a negative impact.

This benefit isn’t without a tradeoff.  Notice when the graphs are overlaid the change effort when complexity is not actively managed starts out lower as opposed to when complexity is actively managed, where the change effort starts higher.  This initial spike in effort is an investment in managing complexity by creating initial architectures and designs that support change.

We observe a period of investment in managing complexity where returns are below that of not actively managing complexity.  However there is a point in time where poorly managed complexity begins to skyrocket where well managed complexit
