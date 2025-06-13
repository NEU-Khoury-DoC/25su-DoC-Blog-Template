---
title: "Phase 3 Individual Deliverable"
date: 2025-06-05
draft: false
description: "This is my individual blog post for Phase III that explain my contributions to the group thus far."
slug: "emmaphase3"   
tags: ["authors", "config", "docs"]
authors:
  - "emmakulla"
showAuthorsBadges : false
---

## Dataset changes
Based on the feedback we received from phase two, we found it necessary to add a fourth dataset that contained some sort of cost-of-living index. I decided to take this on, and landed on choosing the CPI index, one standardly used across the EU. This data was relatively easy to clean as the index is just one value, and most EU countries did not have much missing data for the relatively recent years. One thing that took me quite a while was merging different aspects from our four datasets into one dataset, containing total average weekly working hours, CPI value, birth rate, and the three different types of expenditure we landed on. Regarding data, this was the bulk of the work we did throughout this phase. 

## Visualizations
From the feedback we received from phase two, we realized our visualizations needed a good bit of work. As a team, we decided to try and plan out how our wireframes would look and where helpful visualizations would fit in. From this planning, we landed on creating four more visualizations to include in our app. One that I worked on was the average weekly working hours split up by gender, which will be used to see, on average, how many hours parents would be spending with their children (mock data). The second visualization I started, but did not yet complete, would take in the recommended countries from our second model, and plot out the given expenditures as well as the price index of that country, to help our users make the most informed decisions about their futures, especially when it comes to relocation. 

## Model
In regard to our ML model, I built, trained, and tested our first model, Paul’s linear regression birth rate predictor. Testing out different features took me a good bit of time, as more times than I’d like to admit, I predicted insane birth rates (including -47). After talking to Dr. Gerber, we decided that squaring and cubing certain features (that showed more nonlinear relationships), may help increase our R^2. I tested the model for each assumption, and summarized my conclusions in the blog. 