---
layout: post
title: AWS VPC With Public And Private Subnets Tutorial
description: Tutorial Series on creating an AWS VPC with public and private subnets
modified: 2018-04-20
category: tutorials
tags: [AWS, Cloud, VPC, AWSCasts]
comments: true
share: true
featured: true
---

About the series:

## AWS VPC Overview

Quite simply, a quick overview of an AWS VPC.  A VPC, or Virtual Private Cloud, is a way to segregate a 
Public Cloud, like Amazon Web Services, into Private Clouds.  The 'V' in VPC is for Virtual because the 
cloud is virtually isolated using tools and techniques such as 
[SDN (Software Defined Networking)](https://en.wikipedia.org/wiki/Software-defined_networking).  Of course, 
there are different techniques used to create Virtual Private Clouds, but this is outside of the scope 
of this video.

<iframe width="560" height="315" src="https://www.youtube.com/embed/nNxny_HiGRo" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## AWS Subnets Overview

Subnets, short for Sub-Networks, are isolated networks where access can be controlled.  Subnets have a 
defined set of IP addresses.  A VPC may contain one or many Subnets.  AWS uses 
[CIDR (Classless InterDomain Routing)](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing) notation 
to define subnet IP addresses.  Using Subnets can help isolate AWS resources, for example, creating a 
Public Subnet, one which can be accessed from the Internet, versus a Private Subnet, one that cannot be 
accessed from the open Internet. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/sUMBXbabTbc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## AWS CIDR Overview

[CIDR (Classless InterDomain Routing)](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing) is a 
notation used to allocate or route network traffic using IP addresses.  A group of IP addresses is known as 
a 'block'.  CIDR notation defines a [netmask](https://en.wikipedia.org/wiki/Subnetwork) to represent a block 
of IP addresses.  Routers use the netmask to decide where to send network traffic.  

<iframe width="560" height="315" src="https://www.youtube.com/embed/jAn3bNvyUWM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Create VPC With Public & Private Subnets

We create our first VPC with Public and Private Subnets.  At this point, we haven't secured anything.  There isn't 
a good way to validate that what we built actually works yet.  That is where the next few videos come into 
play.

<iframe width="560" height="315" src="https://www.youtube.com/embed/WW7iVXsUD68" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Create Public & Private Security Groups

[AWS Security Groups](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_SecurityGroups.html) are 
also known as Virtual Firewalls.  They give the ability to control incoming and outgoing traffic.  A Private 
Subnet really isn't private until the Security Group defines the rules to prevent Internet traffic from 
being routed through the firewall.  Similarly, a Public Subnet isn't public until it explicitly allows 
traffic from the Internet.         

<iframe width="560" height="315" src="https://www.youtube.com/embed/rLXNbZoxxps" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Launch EC2 Instance Into Public Subnet

This video shows how to launch an AWS resource, in this case an EC2 Web Server, into the Public Subnet.

<iframe width="560" height="315" src="https://www.youtube.com/embed/BpCjVje32tc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Launch EC2 Instance Into Private Subnet

This video shows how to launch an AWS resource, in this case an EC2 Web Server, into the Private Subnet.

<iframe width="560" height="315" src="https://www.youtube.com/embed/s6hOIgidCIw" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Validate Public Subnet Access

A quick demonstration of a couple ways to validate that our Public Subnet is working as expected.

<iframe width="560" height="315" src="https://www.youtube.com/embed/ebBjoteEdME" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Validate Private Instance Inaccessible From Public Internet

Demonstrate how the Private Subnet is not accessible from the Internet.

<iframe width="560" height="315" src="https://www.youtube.com/embed/ANXms1DdelE" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Validate Private Subnet Accessible From Public Subnet

Validate the networking and virtual firewall rules work to only allow access from the Public Subnet.

<iframe width="560" height="315" src="https://www.youtube.com/embed/6W8Zs_oZO8M" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>  
