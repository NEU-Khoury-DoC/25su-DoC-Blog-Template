---
title: "Project - Phase II"
date: 2025-05-27
draft: false
description: "Proof of Concept - Gathering Data and Designing"
slug: "phase2post"
tags: ["project", "Setup"]
authors:
  - "katherineahn"
  - "anoushkaabroal"
  - "arthurhuang"
  - "shivenajwaliya"
showAuthorsBadges: false
---
# Project Updates
For this phase, we started by clarifying our user archetypes, as well as their stories that elaborate on their motivations. Updates can be viewed on our [blog post for phase 1](/team_posts/phase2post/). We also went back and articulated our data sources better, and found a new, more comprehensive data set as well, that changed some of the technicalities we wanted in our inital plan. Due to this, we also changed those concepts to match our new vision in our first blog post. 

# Data Sources:
At the end of Phase I, we had gathered data from two datasets, households impoverished by out of pocket payments, and general practitioners per 10,000 population. For Phase II, in addition to cleaning and visualizing these two datasets, we have also gathered, cleaned, and graphed out data from 9 new datasets, as updated in our [blog post for phase 1](/team_posts/phase2post/). 8 of these new datasets were pulled from the World Health Organization API, the other dataset web scraped from the Global Health Security Index, to give us that overall score we were looking for. For each of the World of Health datasets, the gatherer information was fitted into a dataframe which had distinct country and date columns, since every W.H.O dataset contained these two values.
We have visualized a couple of the datasets in different ways as they relate to the wireframes that we plan to implement: 

# ER Diagrams:
Below are localized ER diagrams for each personna: the green diagram corresponding to the mover Archibald, red diagram corresponding to the student Gale, and the blue diagram corresponding to the policymaker Nancy.

![image](CareCompass Mover ER.png)
![image](CareCompass Student ER.png)
![image](CareCompass Policymaker ER.png)

Further, the global ER model is seen here:

![image](CareCompass Global ER.png)

Based on our global data model, a first pass of our SQL DDL can be seen below.



