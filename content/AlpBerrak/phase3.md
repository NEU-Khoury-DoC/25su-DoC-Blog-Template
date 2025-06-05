---
title: "Phase 3 Deliverable"
date: 2025-06-5
draft: false
description: "Phase 3 Individual Deliverable"
slug: "phase3alp"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "alpberrak"
showAuthorsBadges : false
---

# Phase Three Blog Post

In this phase, a lot occured. To start, the work I did was mainly focused on the diplomat persona. I implemented the routes the EU Commissioner (diplomat to be renamed later) uses. I also designed the UI and sidebar for the commissioner. This included four pages, 2 of them with just stand in data that will be implemented in phase 4. one of them calls the sql data tables to get each countires accepted refugee application to population ratio and displays either all of the data in a bar chart, the top ten, or the bottom ten. This uses just a get request. In my other working file, the aid projects, there is a chart that currently does not work properly that will show each countries aid projects via graph (once fully implemented). below it, there is a form to upload (post) a aid project suggestion, the option to edit (put) a project the user suggested and soon the option to delete a project the user suggested.

This project also brought forth a lot of issues that required a lot of collaberation. An incorrect merge caused issues that resulted in us needing to figure out how to revert pulls. My docker crashed several times causing me to spend time debugging it to figure out how to get my containers working again. On top of that, figuring out how the routes and all the data conneced together required a lot of back and fourth between my teammates and myself.