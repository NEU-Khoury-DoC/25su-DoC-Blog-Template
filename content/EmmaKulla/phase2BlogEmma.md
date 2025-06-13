---
title: "Phase 2 Individual Deliverable"
date: 2025-05-27
draft: false
description: "The individual blog post for phase 2 of what I contributed + my time in Leuven"
slug: "emmaphase2"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "emmakulla"
showAuthorsBadges : false
---

## Initial Changes
Based on our feedback from phase 1, we had a few adjustments to make to some of our user stories. I helped reframe some of our personas, such as making Cara Day an owner of a branch of daycares, so that one of her user stories could be her interest in expanding to other countries.


## Data Cleaning
In regard to data cleaning, I cleaned the Birth Rates API as well as the Work Hours CSV. The birth rate data was relatively clean and very simple to format; all that needed to be done was to remove non-EU countries as well as years before 2015. The work hour data was slightly more complicated, this data had several different columns and dimensions that needed to be filtered and decoded, such as the different employment types (SO MANY: employed, self-employed, self-employed with employees, etc). The data also had a good bit of missing values in so I decided it would be best to drop the given rows.


## Visualization
I created the birth rate over time visualization that we expect our politician, Paul, to find relevant. I used just the birth rate CSV and created a drop-down feature so that the birth rate for each individual country can be assessed individually, as well as a weighted average for all EU countries.


## ML Modeling
Mia and I created our proof of concepts for our two machine learning models. We ended up deciding on one supervised model for Paul - Takes in work hours and expenditures in order to predict future birth rate for his country. Our second model was catered towards Eura and Cara, and we hope to do a model similar to the one we learned in class today (rank on similarity).


## Blog Post
In regards to the blog, I formatted the ML Proof of concept and data cleaning part, as well as added my visualization and description to the visualization section.


