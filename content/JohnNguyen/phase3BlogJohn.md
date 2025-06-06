---
title: "Phase 3 Individual Deliverable"
date: 2025-06-05
draft: false
description: "Phase III: John's Individual Deliverable for Belgium '25 Dialogue of Civilizations"
slug: "p3jn"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "johnnguyen"
showAuthorsBadges : false
---

# My Contributions to Phase 3

## Streamlit

I led the format and transformation from wireframes to Streamlit in this Phase. I built the home page by leveraging HTML and CSS elements, including a fade in and text overlay above image. When authenticated, I introduced `Your Insights` where users can jot down notes as they browse our resources. It remains as long as the user is logged in and can be downloaded as markdown or plain text. It also provides an warning message before wiping the user's notes as they log out. Another small touch is our greetings on the side bar based on the time of day. Using NewsAPI, I tested displaying related news articles for Paul, the politician. I also transformed our birth rate visualization to Streamlit, which has multi-selection elements. The About page was altered from its template form to our project and includes a brief "About the Authors" section. Beyond Streamlit, I used Adobe Illustrator to craft the gradients that would become the theme for each personas and the front page of Eurobébé.

## CS Aspect

I tweaked our SQL DDL to more closely mimic the cleaned data. I also translated them from CSV to MySQL and incorporated them into our database files. This included making a new table for our fourth dataset: EU consumer price index (CPI). Additionally, I implemented the first model with its weights into our database and formatted the Streamlit elements accordingly. For now the model is part of the birth rate predictor feature for politicians.k