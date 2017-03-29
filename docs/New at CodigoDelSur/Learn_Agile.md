
#What is Agile?

>Agile is a structured and iterative approach to project management and product development, most commonly used for software. It gives you the ability to respond to change without going off the rails, which is good news for any team. When a team transitions to agile from traditional software development, such as waterfall, they should remember that it is a cultural and technical philosophy, not just a set of ceremonies.
> - [atlassian.com](www.atlassian.com/agile)

There are serveral Agile methodologies, the most popular are: Scrum, Kanban, Extreme Programming, Crystal, Dynamic Systems Development Method and Feature-Driven Development. You can learn more about all this different methodologies by entering this [link](https://www.versionone.com/agile-101/agile-methodologies/). 


###Agile Manifesto

The term agile came form the Agile Manifesto. This Manifesto was created when seventeen well-known software development figures met together to discuss about the issues that development methods were having. On that meeting they redacted [4 Values and 12 Principles](http://agilemanifesto.org).

<iframe width="560" height="315" src="https://www.youtube.com/embed/rf8Gi2RLKWQ" frameborder="0" allowfullscreen></iframe>

##Scrum

At CodigoDelSur we mostly use **Scrum**. When we started using this agile methodology, it gave us really good results in our projects. We adopted scrum with a step by step process: we first pick some of the scrum elements that we thought that will be more useful for us. For example, on some projects we started with the daily standup and the sprint retrospective meeting, and then we continue  adding more Srcum ceremonies and elements.   

You can get a quick picture of this methodology by watching thid video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/TRcReyRYIMg" frameborder="0" allowfullscreen></iframe>

If you want to know a little bit more about the roles, ceremonies and components of scrum you can check this links:

- [https://www.atlassian.com/agile/scrum](https://www.atlassian.com/agile/scrum)
- [https://www.atlassian.com/agile/ceremonies](https://www.atlassian.com/agile/ceremonies)
- [https://www.agilealliance.org/glossary/backlog-grooming/](https://www.agilealliance.org/glossary/backlog-grooming/)

Although we love all the Scrum components, we are conscious that Scrum is just a framework, some elements might not apply to all projects. Furthermore, some projects, given its specific nature, might not event be appropriate for Scrum methodology. We believe that beyond the Scrum framework the key value on this agile methodology is in the concepts and the philosophy that the framework helps you to develop. Concepts like continuous improvement, business-value-oriented features, adaptation to changes, client integration on the development process, etc.   

##Internal Quality

In contrast to other methodologies like Extreme Programming, Scrum doesn't specify technical practices to tackle products internal quality, it is mainly centered on project management techniques. We strongly believe that the software internal quality is something that should not be negotiable. If you don't pay attention to the internal quality of your products, you will end soon fighting with your software code to add functionalities and fixing bugs. This will decrease drastically the productivity of the team. 

We have learned that the technical practices that monitors and take care of the internal quality may vary between projects and technologies but here we will mention some common practices that can be applied on every project:

**Technical debt** is a metaphor that compares the poor quality code of a software project with a financial debt. Is crucial to know that all projects will have at least a minimum technical debt, it will appear for different reasons: Human error, misunderstanding, short time lapse, features changes, etc. Is our responsibility to track and try to pay off that debt. What we usually do in our projects is to have a separate backlog were we can add all the technical debt items that we found in the code. This keep us conscious of the debt. On every sprint planning we analyze which items on the technical debt backlog can be tacked on that sprint.

**Definition of Done** is a crucial concept, it consists in a list of activities added to the User Stories (writing code, coding comments, unit testing, integration testing, release notes, design documents, etc.). In order to consider a Task done all the items on the list must be done. This simple activity improves the quality on the software development process. The fact that the whole team stablish a "done criteria", removes a lot of doubts at the moment to the determine the acceptance level of a certain task. Also is very important that the tasks must be well described and must have a clear output so the developers involve on that task doesn't have missunderstanding errors. 

**Continuous Integration** is a well know practice that many developer teams had acquired. Basically Continuous Integration consist in execute plenty frequently an automated integration procedure (download app source, build app, execute tests, etc.) in order to rapidly detect errors and always ensure a deliverable build. Here at CodigoDelSur we are really happy with the results of this practice, it has been super helpful to anticipate issues on our apps.

####References:
- [https://www.scrumalliance.org/community/articles/2008/september/what-is-definition-of-done-(dod)](https://www.scrumalliance.org/community/articles/2008/september/what-is-definition-of-done-(dod))
- [https://martinfowler.com/bliki/FlaccidScrum.html](https://martinfowler.com/bliki/FlaccidScrum.html)
- [https://martinfowler.com/bliki/TechnicalDebt.html](https://martinfowler.com/bliki/TechnicalDebt.html)
- [https://www.scrumalliance.org/why-scrum](https://www.scrumalliance.org/why-scrum)
 