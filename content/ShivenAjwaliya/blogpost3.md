---
title: "Blog Post 3"
date: 2025-06-05
draft: false
description: "Phase 3 Deliverable Individual"
slug: "shivenajwaliyablog3"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "shivenajwaliya"
showAuthorsBadges : false
---

### Project
For Phase III, my main focus shifted from design and modeling to implementation. I was responsible for building out most of our backend REST API, starting with the country routes. I implemented endpoints that allow users to retrieve detailed country profiles, list all countries (with optional score filtering), and fetch factor scores by country ID. I also added admin-only functionality for updating and deleting country records, which gives us full CRUD support. 

Beyond country routes, I worked on the recommendations and comparison endpoints. I built the ```/recommendations/factors``` route to return the six health system dimensions we use across the app, each with a description to help users understand what they're prioritizing. For the comparison feature, I implemented the ```/compare``` route, which allows users to select up to three countries and view their factor scores side by side in a structured table format. I also created the ```/compare/timeseries``` route, which lets users track how a specific health factor has changed over time across multiple countries. This supports our student and policymaker personas by making historical trends and system performance differences easy to analyze at a glance. 

Finally, I contributed to the team blog by writing the section on the Rest APIs. 

### Belgium DOC
Last weekend, we visited Luxembourg, which turned out to be a wonderful experience. On our free day, we headed to the beach and enjoyed a refreshing swim until a sudden thunderstorm cut our plans short. Still, it was a fun and memorable outing.



