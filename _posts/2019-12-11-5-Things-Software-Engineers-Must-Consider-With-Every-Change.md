---
layout: post
title: 5 Things Software Engineers Must Consider With Every Change
description: 5 Considerations (Continuous Delivery, Built-in Quality, Consider the Whole System, Continuous Monitoring, You Build It - You Run It) Software Engineers should take into account with each change.
modified: 2019-12-11
category: articles
tags: [software, learning, process, engineering]
comments: true
share: true
featured: true
---

## 5 Things Software Engineers Must Consider With Every Change

World class engineering organizations must be able to deliver system changes to 
production in minutes, not months, weeks, or days.  Along the road to attaining 
this goal, engineering teams must figure out how to make releases a 
“non-event” - that is, releases aren’t special and they require no more attention 
than any other event.  This article outlines 5 considerations engineers should 
consider that cut across 5 advanced software engineering 
concepts: **Continuous Delivery, Built-in Quality, Consider the Whole System, 
Continuous Monitoring, You Build It - You Run It**.  These considerations are by 
no means complete, but will serve as a solid foundation for progress.

### **Continuous Delivery** - How could we deploy changes without releasing them?

Technology delivery methods have advanced far beyond traditional development 
and deployment models.  Building the engineering and business capacity to 
deliver working, valuable software to customers on demand and as frequently 
as possible is now a necessary step to creating world class engineering 
teams.  It may seem that increasing the frequency of software delivery 
would increase organizational risk; however, according to industry 
research (https://services.google.com/fh/files/misc/state-of-devops-2019.pdf) 
higher frequency software delivery is correlated with reduced risk and 
increased quality.

This does not mean turning teams loose into the wild wild west. Instead, teams 
take steps to build competency and capability coupled with advanced delivery 
and testing patterns, building confidence in pipelines and processes along the 
way.  New techniques require new vocabulary, here are a few definitions to 
clear the air:

* <u>Continuous Deployment</u> - process of migrating changes into an environment 
with every successful build, ideally, a production environment.  Changes 
migrated do not need to be made visible or available to clients.
* <u>Continuous Delivery</u> - making a change visible or available to clients, this 
does not, and should not, require a deployment.
* <u>Release</u> - I prefer to use release and Continuous Delivery interchangeably.

#### Tips/Tricks/Tools

* Feature flags - Java - [Togglz.org](https://www.togglz.org)
* [Blue/Green Deployment](https://martinfowler.com/bliki/BlueGreenDeployment.html) 
* [Canary releases](https://martinfowler.com/bliki/CanaryRelease.html?ref=wellarchitected)

### **Built-in Quality** - How can we prove the solution works?
Consider the following example from a more established engineering domain, Civil 
Engineering.  A bridge must be built to cross a large creek/small river.  What 
*doesn’t happen* is the engineer takes an educated guess at what needs to be 
done, builds the bridge, and then walks/drives over it to test that it will 
stand.  The engineer starts by understanding the constraints and forces at 
play in the environment in which the bridge lives:

* How much weight the bridge must support at any given time?
* At what speed will persons/vehicles cross the bridge?
* What type of ground material will the bridge rest on?
* What is the flow rate of the river/creek (what is the maximum flow rate 
the bridge must resist)?
* What kind of weather conditions will the bridge encounter?
* How much flex in the bridge is tolerable?
* What frequency will inspections occur?
* What is the desired lifespan of the bridge?
* Etc…

The engineer takes each of these constraints and designs the bridge, testing 
each component individually, and then the integration between components 
prior to building the bridge.  Bridges built in the midwest that has a variety 
of hot and freezing days will be built using different materials than a 
bridge in Florida, for example.

Software Engineering requires a similar thought process of understanding 
constraints and engineering a solution.  Each of the constraints should 
be tested as we go to prevent a faulty component from entering a 
production environment.

* Many facets to this concept, unit, integration, and functional tests.
* Quality cannot be *added* on top once a change is complete, that is 
quality assurance.  Quality must be *built in* to the change.  
* Useful techniques include Test Driven Development (TDD), Behavior 
Driven Development (BDD), etc...

### **Consider the Whole System** - How will the change integrate with the system and what impact could it have?

Considering the whole system requires engineers to take a step back and 
evaluate not only how the change will impact their area, but consider how 
the change will impact the organization as a whole.  What should a team do 
if the best solution will benefit them directly but create a negative impact 
on two other teams?  How should they approach going about making the 
tradeoff?  The answer, it depends.

A few potential questions to ask:

* How will changes impact the way data flows through the system?
* How will the change affect monitoring solutions in place?
* How will upstream or downstream clients be impacted?
* Who might need to be aware of the change?
* How might the change affect the sales team or prospects?

#### Tools/Tips/Techniques

Integration is difficult, especially in a microservices architecture.  Yes, 
API’s should have clearly defined interfaces, be predictable, and isolate 
breaking changes via API versioning, but those alone don’t cover all scenarios.

One useful technique for managing inter-service integration is 
[Consumer Driven Contracts](https://martinfowler.com/articles/consumerDrivenContracts.html), 
which Spring Boot supports 
([Spring Contract Guide](https://spring.io/guides/gs/contract-rest/)) or you 
can easily roll your own.  Each producer/consumer create a contract 
(potentially real json request & response, for example) for a variety of 
scenarios.  Then each party can run tests against those contracts to verify 
each of the scenarios are handled.  The same procedure can be used for 
message queues/streams.  Sample messages are created and included in test 
resources and each build of the system checks that all contracts are met.

### **You Build It, You Run It** - How will teams be the first to know if a change fails in production?

Accountability in software engineering creates a culture of ownership.  When 
software engineers feel ownership of their product; quality, communication, 
and speed to market improve - all of which benefit the organization as a 
whole.  Simply assuming an on call engineer can triage and handle issues is 
unsustainable and possibly extends outages and response times.

Additionally, running your own services in production provides fast feedback 
to errors and performance issues that might not have been thoroughly thought.  
Engineering teams can respond in near real time to feedback, learning as 
they go how best to engineer their services to reduce operational noise and 
improve service reliability.

#### Tips/Tricks/Tools

* Create team (product) level dashboards.
* Failures & errors trigger alerts to teams as necessary.
* Track and classify failures to identify common failure points.  Prioritize 
and address these issues in addition to regular work.

### **Continuous Monitoring** - Are there any team (product) level KPIs to measure the change impact? 

Teams that run their own services, deploy frequently, and build in quality 
will need to see how their applications are performing in production.  
Monitoring allows teams to measure how changes impact baseline measures and 
provides fast feedback into the health of services.  

Teams are responsible for their own metrics.  Metrics are created when 
they are useful and should be deleted when no longer useful.  Each team 
should have their own dashboard to visualize KPIs for services and include 
appropriate alerting should a threshold be met.  Dashboards include 
information such as request throughput, transaction times, and other 
operational measures.

#### Tips/Tricks/Tools

* Each team owns their own dashboard and metrics **in plain view**.  These 
metrics, or a subset, can be flowed to enterprise monitoring tools as well.
* Identify KPIs for teams (products).
* Failure alerting processes and tools.
* Should a failure occur that does not trigger an alert or show up on the 
dashboard, a new metric should be added and monitored.
