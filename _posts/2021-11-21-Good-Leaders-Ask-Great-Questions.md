---
layout: post
title: Good Leaders Ask Great Questions
description: Notes from reading Good Leaders Ask Great Questions by John Maxwell
modified: 2021-11-21
category: articles
tags: [book, learning, notes, professional development]
comments: true
share: true
featured: true
---

# Overview

Coming soon, overview of this book and sentiment

## Notes

When facing a problem with an unknown solution ask the following questions:
1. Why do we have this problem?
2. How do we solve this problem?
3. What specific steps must we take to solve this problem?

---
Ask tough questions of oneself

---
Three Questions People Ask of Their Leaders
1. Can you help me? (Competence)
2. Do you care for me? (Compassion)
3. Can I trust you? (Character)

---
When leaders learn and live good values, they make themselves more valuable and lift the value of other people

Good leaders exhibit three qualities
1. Humility: understanding your place in the bigger picture
2. Authenticity: being comfortable in your own skin
3. Calling: have a purpose bigger than you

---
Identifying Leaders to grow
1. Influence- do they influence others
2. Capacity - do they have the potential to grow and develop
3. Attitude - do they desire to grow and develop themselves
4. Chemistry - do we like each other
5. Passion - are they self motivated
6. Character - are they grounded
7. Values - are our values compatible
8. Teamwork - do they work well with others
9. Support - do they add value to me
10. Creative - can they find possibilities in the impossible
11. Options - can their contribution give me options
12. 10 percent - are they in the top 10% of those on the team

---
Others are more likely to listen to us if first we listen to them

---
Communication tip: Ask people to tell me something I NEED to hear but may not WANT to hear.

---
Good leaders ask great questions that inspire others to dream more, think more, learn more, do more, and become more.

---
Questions to ask team members, customers
1. What do you think?
2. How can I serve you?
    1. What could I do for you that would make your job easier, make you more successful, and make the team better?
3. What do I need to communicate?
4. Did we exceed expectations?
5. What did you learn?
    * Ask after meetings or situations to inspire inspection and adaptation. People start to think about what they learned in anticipation of this question
6. Did we add value?
7. How do we maximize this experience?
8. What do I need to know?
9. How do we make the most of this opportunity?
10. How are the numbers?
11. What am I missing?

---
Rule of 5 for improvement
1. Read
2. Write
3. Think
4. Ask questions
5. File what you learn

---
Positive supportive people to add to a team
1. Believers - people who believe in you and your vision
2. Achievers - people who contribute to the team with excellence
3. Conceivers - people who bring good ideas to the table
4. Relievers - people who compliment your skills and abilities

---
Let loneliness drive you to aloneness. When you are feeling the weight of leadership, find ways to get by yourself and think things through.

---
“Were any great men born in this village?” - “No, only babies.”

---
Demonstrating competence as a leader
* Work hard - people respect a hard worker
* Think ahead  - begin with the end in mind
* Demonstrate excellence - the better you are the higher your credibility
* Follow through - bring things to completion

---
Establishing character
* Care about the people you lead
* Make things right
* Tell the truth

---
What really matters to you?
* What makes me sing?
    * Identifies joy
* What makes me cry?
    * Touches your heart
* What makes me dream?
    * Sparks your imagination
* What makes me excel?
    * Strengths
* What makes me different?
    * Uniqueness

---
Onboarding as a new leader
1. Strengthen relationships
2. Earn peoples trust
3. Position team members appropriately
4. Create clear expectations
5. Determine peoples capacity

---
“Motivation is always in direct proportion to the level of expectations “

---
Raising the bar for employees
* Are you reaching your maximum potential?
* What would you like to do better?
* Do you know how to reach your maximum potential?
* Can I help you?

Law of Magnetism - Who you are is who you attract

---
Traits for identifying motivated people
1. Positive attitude
2. Can articulate specific goals for their life
3. Initiators
4. Proven track record of success

---
“When you made the choice to start, you made the choice to finish. It’s not two choice; it’s one.”

Tips to help people become finishers
1. Show them the big picture
2. Give them accountability
3. Help them schedule their time
4. Provide a work partner
5. Reward only finished work

---
If you give effort to negative people you must ask yourself:
* How much of my energy will I let them take?
* How much of my time will I let them take?
* How much of my focus will I let them take?
* How much of my joy will I let them take?
* How much of the resources will I let them take?
  
These questions help you realize the cost to keeping negative/unproductive people

---
Inspiring a team
* Share your passion - contagious
* Paint the picture of a better future
* Show how their role makes a difference
* Challenge them to keep growing

“When we have made our last climb, we are old, whether forty or eighty” - Fred Smith








#### Tips/Tricks/Tools

* Feature flags - Java - [Togglz.org](https://www.togglz.org)
* [Blue/Green Deployment](https://martinfowler.com/bliki/BlueGreenDeployment.html) 
* [Canary releases](https://martinfowler.com/bliki/CanaryRelease.html?ref=wellarchitected)


## Built-in Quality - 
### How can we prove the solution works?
Consider the following example from a more established engineering domain, Civil 
Engineering.  A bridge must be built to cross a large creek/small river.  What 
*doesn’t happen* is the engineer takes an educated guess at what needs to be 
done, builds the bridge, and then walks/drives over it to test that it will 
stand.  

The engineer starts by understanding the constraints and forces at 
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

#### Tips/Tricks/Tools

* Many facets to this concept, unit, integration, and functional tests.
* Quality cannot be *added* on top once a change is complete, that is 
quality assurance.  Quality must be *built in* to the change.  
* Useful techniques include Test Driven Development (TDD), Behavior 
Driven Development (BDD), etc...


## Consider the Whole System - 
### How will the change integrate with the system and what impact could it have?

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


#### Tips/Tricks/Tools

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

## You Build It, You Run It - 
### How will teams be the first to know if a change fails in production?

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


## Continuous Monitoring - 
### Are there any team (product) level KPIs to measure the change impact? 

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
