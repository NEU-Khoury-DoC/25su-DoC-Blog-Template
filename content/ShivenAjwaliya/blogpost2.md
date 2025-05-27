---
title: "Blog Post 2"
date: 2025-05-27
draft: false
description: "Phase 2 Deliverable Individual"
slug: "shivenajwaliyablog2"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "shivenajwaliya"
showAuthorsBadges : false
---

### Project
For Phase II, I focused on refining our personas and finalizing features and ML models based on the feedback and limitations we encountered in Phase I. At that point, many of our models and features were still abstract; we had a few ideas, but we weren’t sure if our chosen datasets would support them. We also learned from feedback that user-driven weighting via sliders shouldn’t be used to calculate composite scores directly. So, using the new dataset Arthur and Anoushka sourced, I proposed switching to a k-nearest neighbors (k-NN) approach. This allowed us to use slider input not as weights but as a user preference vector, which we then compare against normalized country data to recommend the most similar healthcare systems. To make recommendations even more context-aware, we also added an option for users to blend preferences with similarity to a selected origin country. This enables personalized results that balance familiarity with aspirational healthcare goals. I also outlined a second ML model focused on time series forecasting, inspired by the visual style of Google Trends. This powers our country comparison tool by allowing users to track changes in healthcare indicators over time and view projected trends for the next five years.

I also reworked all three of our core personas to make them more specific and aligned with our finalized features. I added concrete details like names, academic backgrounds, family situations, to ground each persona in a real-world use case. The most significant change was to our second persona, who was originally a traveller, whom I reframed as Archibald Bridgemont, a parent planning a long-term move to Europe with his wife and daughter. This shift made more sense for the features we developed, such as personalized country matching based on healthcare priorities and detailed country profile exploration. A short-term traveler wouldn’t realistically compare long-term healthcare systems, but someone relocating abroad absolutely would. These updates helped ensure that our personas felt human, purposeful, and directly connected to the functionality of the app.

Finally, I worked on the country strength and weaknesses wireframe.

### CS3200
As for CS3200, I found querying a database very fun but I did not enjoy doing ER diagrams; they felt very time consuming. 

### Belgium DOC
So far, the highlight of the DOC has been our visit to Professor's Fontenot's friend, Arno's chocolate shop. Making the pastries and chocolate was incredibly fun and I know I will be bringing back home a lot of Belgian chocolate.  

![Arno and the Chocolate Factory](https://i.imgur.com/k3nULI7.jpeg)
