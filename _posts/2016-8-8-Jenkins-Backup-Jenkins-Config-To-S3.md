---
layout: post
title: Jenkins: Jenkins Automated Backup To AWS S3
description: Creating a Jenkins job that backs up all Jenkins jobs to AWS S3
modified: 2016-8-8
category: android
tags: [Jenkins, Automation, Software, Cloud]
comments: true
share: true
featured: true
---

# Why backup build jobs?

I'm running a containerized Jenkins instance for my CI jobs and wanted an easy
way to ensure my build configs would persist even if something happened to my
Jenkins container.  

## My options

I could have used a Docker volume, or created a custom AMI,
or even created an AWS volume from my AMI that could be mounted on any other AMI.

## Why didn't I do these things?

None of the above options made sense.  Had I used a Docker volume I would have had
to persist that volume somewhere, creating additional overhead.

If I chose to create a custom AMI that contained my configs then anytime I
updated my CI configurations I would have had to build a new AMI...doesn't
help me move faster.

What about creating a Volume in EC2?  Same problem, any time I update something
in Jenkins I would have to create a new volume.

# The Solution

I created a Jenkins job that runs daily.  This job tar's and gzip's my configs
and uploads it to an S3 bucket (The job requires the Jenkins S3 plugin).  Builds
are versioned and maintained in a persisted state.

## Build Job (shell)

<script src="https://gist.github.com/jamesbyars/31266615b9560399bbb54014c67b75c6.js"></script>

Please note: I referenced http://www.clausconrad.com/blog/backup-jenkins-configuration-to-s3
while creating this script.
