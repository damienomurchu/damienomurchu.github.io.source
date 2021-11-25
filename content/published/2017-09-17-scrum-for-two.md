---
draft: false
layout: post
date: 2017-09-17
title: "Scrum for two"
subtitle: "Small-scale Agile"
description: ""
author: "Damien"
image: ""
tags:
  - Agile
  - Scrum
  - Software Development Process
URL: "/blog/2017/09/17/scrum-for-two/"
categories: [Articles]
---

# Scrum for two?
No, the title isn’t a misnomer, what follows are my experiences using scrum methodologies within a two-person team for a final year college project.

# Some personal background
In 2016 I found myself back in full-time education, in the midst of an aggressively paced computer science conversion course. Targeted towards existing graduates from non-computing disciplines, my classmates were a motley bunch ranging from musicians and fine artists to engineering and even agricultural graduates.

Against this background in 2017 I found myself on work placement in Red Hat Mobile while also working feverishly with a colleague on a final year college project. One of the slightly less usual aspects of our project was our decision to manage our project with all the trimmings of scrum, a set of methodologies usually preferred for larger teams. This article outlines my experiences resulting from that choice and experiment.

# The project itself
The project at the root of this was one around JIRA and extending some existing JIRA tooling. With Red Hat Mobile being large users of JIRA to manage their agile-scrum development process, it was a relatively straightforward decision to look at a project in this area.

Serving as the companies ‘single source of truth’ around its development workflow, JIRA contains a valuable bank of development data, and several tools had been written by colleagues to tap into this data. For this project, we chose to build upon a command-line tool, jira-miner, and develop graphical and data-analysis functionality on top of it.

# Project process
Developed in the same manner as any other internal projects within Red Hat Mobile, product owners were designated, as well as our direct engineering manager who would serve as our scrum master for the duration of the project. With project stakeholders allocated, requirements for the project were then fleshed out in a product requirements process and captured in a product requirements document (PRD).

With product requirements specified, these were then translated into JIRA tickets in the form of tasks (individual items of work) and epics (themes with which to group tasks). Story point values were agreed and assigned to tasks to reflect their complexity, and these tasks were then prioritized on our backlog.

# Agile-Scrum process
Each organisation and team has its own implementation of agile-scrum, and for our project we followed the general agile-scrum process within Red Hat Mobile. Tickets sit on our backlog until they were brought into a sprint (block of development). For our project this meant two week sprint cycles.

Once within a sprint, tickets were self-assigned and as a scrum team we followed the various scrum rituals most teams do.

Our stand-ups (team update sessions) were daily, typically lasting 10- 15 minutes and always run only when at least both team members would be present. In a slight departure from typical scrum practice, our scrum master would not always be present, in which case the team would run the stand-up themselves. All other scrum rituals would be orchestrated by our scrum master.

In addition to our stand-ups, we would have regular backlog refinement sessions to ensure the backlog of tasks always reflected the work required and the priority of that work. Tasks would be story-pointed as required, and a sprint planning session held before each sprint to decide the focus of the sprint and the tasks to be worked on during it.

At the end of each sprint, a retrospective session was held to discuss what went well, what didn’t go so well, what could be improved, and what actions should be taken for the next sprint.

# Project challenges
Running the project as we did provided a number of challenges and learning opportunities.

Consensus within a small (and even numbered) team proved a challenge on occasion. While not a frequent issue, lack of a higher technical authority to resolve such issues was sometimes a challenge with a (then) small and relatively inexperienced team.

The scrum-agile structure itself was sometimes a challenge and for small-scale projects, the formalities of scheduled stand-ups, planning, backlog refinement, and retrospective sessions every sprint cycle could seem over-rigorous and sometimes could have been achieved informally and less rigorously.

Inexperience with the agile-scrum process was also a challenge initially, but the project structure itself afforded a valuable opportunity to learn the process, and actually provided a valuable sandbox to learn and experiment with the agile-scrum process we used within our larger teams.

# What I learned
For this project we worked as a small scale, collaborative and semi-distributed team. Working in this way offered an opportunity to explore the many facets of an agile-scrum process followed by an agile-scrum development team. This also offered the opportunity to challenge, question, and reinforce the whole approach. This would have been far more difficult, or impossible to the same extent in a larger and established team.

Working on an project from its inception also allowed us to explore, decide and see the structures of a project through their many stages from setup and establishment to subsequent iteration and refinement of those same processes as we adapted them to our team.

A small team allows no one to hide, which was very valuable in ensuring any issues that emerged were both faced and resolved. This led to rapid team development and ensured the team continued to remain as healthy as possible.

Finally our project allowed us quite clearly to see the evolution and growth of our team, and the relevance of the structures we chose for it, as well as the teams needs at various points in its evolution. This learning has already proved valuable in subsequent projects and assessing whether other approaches like Kanban would be more suitable.

# Some reflections
Working on a project, it is sometimes difficult to assess the project using just one filter; in this case that of the small scale scrum approach we chose.

Beginning and seeing a project through to a conclusion was a very insightful way of assessing a methodology like scrum and its potential suitability for the needs of a team.

Some of the greatest value in exploring this approach within the sandbox of a small project has been the knock-on benefits when subsequently using scrum in regular-sized scrum teams. As a regular scrum member after the project, I felt better educated and better equipped as a team member as a result of our small-scale scrum experiment.

Finally, I am currently serving as the scrum master of my present team, a role I assumed less than three months since the conclusion of this project. As scrum master the lessons and perspective gained from this small-scale scrum college project have proved invaluable in my current role.