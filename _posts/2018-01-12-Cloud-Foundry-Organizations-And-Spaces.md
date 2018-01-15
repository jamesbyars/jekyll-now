---
layout: post
title: Cloud Foundry Organizations and Spaces
description: "How Cloud Foundry Organizations and Spaces are used and how they fit into the Cloud Foundry ecosystem."
modified: 2018-01-12
category: articles
tags: [cloud, software]
comments: true
share: true
---

[Cloud Foundry](https://cloudfoundry.org/) is an open source 
[PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service) (Platform-As-A-Service) service 
used to abstract infrastructure details from development teams.  I will be 
producing a 'Getting Started' article to accelerate the learning curve at 
some time in the future.  This article will focus on a two concepts 
provided by Cloud Foundry, Organizations and Spaces, to assist development 
organizations with application management.

![CloudFoundryLogo]({{ site.url }}/images/cloud-foundry/cf-logo.png)

# Organizations

An organization provides a high level management interface and access 
control.  I think of the [Cloud Foundry](https://cloudfoundry.org/) 
(CF) Organization to be synonymous with a department in a business.  

To give an example, if I was an Insurance Company running CF I could 
segment the departments of the company into CF Organizations:

* Personal Insurance
* Business Insurance
* Commercial Insurance
* etc...

### Benefits of using Cloud Foundry Organizations

Each [Cloud Foundry](https://cloudfoundry.org/) organization has its 
own domain.  This feature can be used to segment organizations 
services.

Organizations are setup to allow individual users to have access to the 
organization.  In the above insurance company example we can enforce 
authentication and authorization for each organization, so a developer 
in the Personal Insurance organization would not have access to make a 
change in the Business Insurance organization (unless said permission 
was explicitly set, of course). 

[Cloud Foundry](https://cloudfoundry.org/) organizations are configurable 
to set resource limits to prevent services in one organization to hog 
all resources causing an issue with another organization.  Additionally, 
resource consumption can be monitored to make allocation decisions.

# Spaces

Applications and services deployed to 
[Cloud Foundry](https://cloudfoundry.org/) (CF) are scoped to 
spaces with each organization containing one to many spaces.

Using my previous example of a Insurance Company.  Within each organization 
we would organize our services into spaces.  Each space may contain a 
component of that particular department.  So for the Commercial Insurance 
department we may have a space for:
 
* Underwriting
* Claims
* Correspondence
* Analytics
* etc... 

Spaces allow for finer grained authentication and authorization security.  
Each user can be assigned a role that grants permissions for specific 
activities.  For example, a user with the "Space Developer" and another 
user with the "Space Auditor" roles can both view all the same things, 
however the user with "Space Developer" has additional permissions to 
create/edit/delete/rename services, applications, and routes.

To view all roles and permissions for an organization have a look at the 
matrix at [Roles and Permissions for Active Orgs](http://docs.cloudfoundry.org/concepts/roles.html#roles).

# Cloud Foundry Organizations and Spaces Summary

[Cloud Foundry](https://cloudfoundry.org/) organizations and spaces provide 
ways to organize compute resources in natural ways.  There are clear 
benefits to creating separate organizations for departments in a large 
organization.  Adding the ability to group resources into distinct 
spaces provides simplified tools for monitoring and security.  Users are 
created at the organization level to allow general access to the 
organization in Cloud Foundry.  Each space can create its own roles 
and permissions to create more fine grained access controls. 

The concept of spaces encourages modular application design with low 
coupling.  
