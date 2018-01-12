---
layout: post
title: Cloud Foundry Organizations and Spaces
description: ""
modified: 2018-01-12
category: articles
tags: []
imagefeature: /cloud-foundry/some-image.jpg
comments: true
share: true
---

Cloud Foundry is an open source PaaS (Platform-As-A-Service) service 
used to abstract infrastructure details from development teams.  I will be 
producing a 'Getting Started' article to accelerate the learning curve at 
some time in the future.  This article will focus on a two concepts 
provided by Cloud Foundry, Organizations and Spaces, to assist development 
organizations with application management.

![CloudFormationLogo]({{ site.url }}/images/cloud-formation/cf-logo.svg)

# Organizations

An organization provides a high level management interface and access 
control.  I think of the Cloud Foundry (CF) Organization to be 
synonymous with a department in a business.  

To give an example, if I was running CF in an Insurance Company I could 
segment the departments of the company into CF Organizations:

* Personal Insurance
* Business Insurance
* Commercial Insurance
* etc...

Organizations can each have a custom domain to segment departments

## Benefits of using CF Organizations

Using organizations 

# Spaces

Applications and services deployed to CF are scoped to spaces with each 
organization containing one to many spaces.

Using my previous example of a Insurance Company.  Within each organization 
we would organize our services into spaces.  Each space may contain a 
component of that particular department.  So for the Commercial Insurance 
department we may have a space for:
 
* Underwriting
* Claims
* Correspondence
* Analytics
* etc... 