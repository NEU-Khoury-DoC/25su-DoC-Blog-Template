---
title: "Blog Post 4"
date: 2025-06-13
draft: false
description: "Phase 4 Deliverable Individual"
slug: "shivenajwaliyablog4"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "shivenajwaliya"
showAuthorsBadges : false
---

### Project
In Phase IV, I focused on tying together major parts of the CareCompass app, especially around personalization and content integration.

First, I built the Rankings page, where users can see how countries rank across healthcare factors based on their own priorities. I implemented the logic to weight and sort countries according to six core health system scores and connected it with sliders that let users tweak these weights interactively. Initially, I had the ranges for Rank 1, 2, 3, 4, 5, 6 to be 90-100, 70-90, 50-70, 30-50, 10-30, 0-10 respectively but since that is not intutive for the user, I changed to 0-10 and had underlying math to calculate the weights for all. To improve usability, I also wrote descriptions for each factor so users could better understand what each factor actually meant. 

Next, I created the CountryArticles table (foreign key to Country with CountryCode)and populated it with realistic mock data using Mockaroo. These articles now show up on each country profile page, providing contextual reading. This feature was especially designed to support students and policymakers looking for deeper insights beyond just the numbers. For each article a random image is selected to make the page more pleasing. Although when it is reloaded it shuffles the images around. In the future I want to implement such that the image stays the same for each article (probably could be done using custom list or a number range from mockeroo). 

I wrote the entire README file for our repository, ensuring it could serve as a standalone overview for anyone trying to understand, run, or extend our project. The README includes:
- Overview: A concise summary of what CareCompass is, who it serves, and the core value it offers.
- Project Goals: Our aims to demystify international healthcare systems through interactive data analysis and ML-powered recommendations.
- Tech Stack: Detailed the backend (Flask, SQL), frontend (Streamlit), ML (sklearn, pandas), and deployment tools (Docker).
- Core Functionalities: Explained each feature clearly—rankings, comparisons, time-series forecasts, article recommendations, and country matching.
- Structure of the Repo: Helped contributors and instructors navigate our folder layout and file purposes.
- Data Sources: Linked and summarized our use of WHO data, the Global Health Security Index, and others.
- Prerequisites & Run Instructions: Gave step-by-step setup for running the app locally, including installing dependencies and launching with Docker.
- Future Plans: Outlined realistic next steps, including improving article sourcing and experimenting with quality-of-life based similarity rather than healthcare-only metrics.

Finally, I cleaned up the backend by removing unused routes and finalizing our REST API matrix, ensuring all documented endpoints reflect what’s actually used in the app. Particularly, I removed certain country routes that we didn't use, comparison routes because it the ml routes did something similar, and I moved the recommendation route to country since it didn't make much sense to have a whole folder for just one route. 

Overall, I am pretty proud with what we accomplished by the end. There were certain features that I would've wanted incorperated (ex. adding a toggle for having country of origin be a factor) but this is still a presentable state at this point. I had a lot of fun making this project and I learned a lot in the process so thank you!

