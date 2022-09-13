---
title: Why i use diagrams.net as my GoTo diagrams app
date: 2022-09-13T00:00:02+00:00
description: sdfafdaf
draft: false
tags:
    - diagrams
    - tools
---

I'm getting a lot of questions lately from people asking me what tool(s) i use to create my diagrams. You will be surprised that this is actually a free tool which is accessible to everyone.

{{< admonition note "Disclaimer" >}}
Please note that this is my personal opinion. There are many tools out there and some might have the same features a this one. I did not test all other tools.
{{< /admonition >}}

# My history in creating diagrams

## Why create diagram in the first place

Diagrams... we see them all the time. Schematic representations of a topic or solution with beautiful boxes, lines, arrows and icons. 

For me, diagrams are a real added value to any kind of documentation or presentation. They help to tell the story, clarify the textual part of a document and are really handy to use in meetings (point and click). 

For instance, a piece of text in a solution design can be detailed with the addition of a diagram. On the other hand, it's also hard to create a diagram which is fully self-explanatory. Therefore a diagram is often accompanied by a piece of text to explain what is meant.

I've been using a lot of different tools throughout the years. Some where payed licensed tools and some where freeware. In this blog will walk you tough some of the main tools and what i used them for but in the end the focus is mostly on `diagram.net`.

## Types of diagrams i have experience with

I've had my share of roles in the years passed and with those roles came different levels of details. Below is a summary of the most frequently used diagrams i've worked with.

If you are not interested in this short historical overview, feel free to jump to the actual topic of this blog, [diagram.net](#diagramnet).

### Unified Modeling Language (UML)

When i started working as a lead developer / software architect is was mainly focussed on creating architecture designs for individual applications or sometimes small solutions (some front-end with a backend and a database). This would involve drawing application diagrams  with components, classes and interface, data models and some sequence diagrams.

Initially i started out using `Visio` for this. This was the GoTo tool at that time and because we had access to the microsoft tooling this was an obvious choice. It's basic, allows for creating the diagrams by installing additional stencils but lacks reusability and flexibility. Let alone the fact that you could add metadata to your elements. 

Later Rational [Software Architect Designer](https://www.ibm.com/products/rational-software-architect-designer), which is a mouth full :) was provided by my company as a preferred tool. A diagram tool designed by IBM which did add some more flexibility and reusability to the diagram workflow. Creating elements with properties (metadata) and using them on multiple diagrams was a real added value.

Back in the days of Visual Studio 2010 (something like that) there was also an option to use the class designer and create some basic class diagrams. You could actually generate the diagram based on the code in the project, which was actually pretty handy sometimes. THe problem with this tool was the lack of reusability. 

After many attempts i finally got the chance to obtain a [Sparx Enterprise Architect](https://sparxsystems.com/) license. A reall treat for modeling and designing diagrams. Lots of features, project structures, exporting and importing, document creating, but most of all a really extended arsenal of modeling frameworks was supported. It could also import code from C# projects and generate code based on you models. The later i was nog fund of but still...

### ArchiMate

When i became a Solution Architect i was working more and more on a higher level of abstraction. UML was replaces by a modeling framework, which i came across during my TOGAF training, called [ArchiMate](https://www.opengroup.org/archimate-forum/archimate-overview). This modeling framework was especially designed for enterprise architectures and focusses on business-, application- and infrastructure layers. Later some additional layers where introduced but i never really used these.

Initially i kept using Sparx as it also contained the ArchiMate framework but as the scope of the diagrams became more and more limited to ArchiMate i turned to [Archi](https://www.archimatetool.com/). This tool is free and is based on the eclipse IDE. It's specifically written for ArchiMate and contained the lated versions and elements which where required.

### Cloud Architectures

For my current role as an Azure Cloud Architect i take a small step back from the business layer. And although the business aspect is still relevant it's not the main focus of the diagrams. I mainly draw 

Draw cloud solutions (similar to microsoft documentation)
recognizable to customers

## diagram.net

(formerly draw.io)

Feels like Visio on steroids.

### The good stuff

### What is missing

Reusability, only one templates option. Would like to have more.

Project structure, don't really like the tabs

## Resources

[Security-first diagramming for teams.](https://www.diagrams.net/)

[The actual online app](https://app.diagrams.net/)

[Official electron build of draw.io on GitHub](https://github.com/jgraph/drawio-desktop)

[Diagrams.net on Wikipedia](https://en.wikipedia.org/wiki/Diagrams.net)