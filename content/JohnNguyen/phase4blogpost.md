---
title: "Phase 4 Individual Deliverable"
date: 2025-06-13
draft: false
description: "Phase IV: John's Individual Deliverable for Belgium '25 Dialogue of Civilizations"
slug: "p4jn"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "johnnguyen"
showAuthorsBadges : false
---

# My Contributions to the Final Phase

The final phase primarily called for the implementation of our second model as well as polishing touches. I began making small changes such as ensuring our logo features 12 stars, making the slidedeck readable, and editing the structure of our sidebar buttons. I also worked on streamlining our web pages into one coherent design language with the blurred gradients; all tools now feature the same gradient background instead of the standard `st.title()` element. After receiving our second model Python code, I implemented it into our RESTful API calls, defined functions to calculate the cosine similarity scores, and returning that into a refined dashboard tool. Additionally, we decided to include a radar chart since all values are normalized and we believed this chart depicted the comparisons between user preferences and a country's actual values well. The deliberate choice was so also made to include the statistics about our data, including average, median, minumum, and maximum values. Since the model is included in two different personas, we carefully tweaked the wording of each tool to fit in with the user's intent. Beyond our second model, I also expanded the use of our NewsAPI implementation, now a part of daycare location profiles, politician home, and the 'From the News' tab of the EU Market Expansion tool. The 'Home' page, too, got a significant facelift. It now features an image carousel celebrating 20 years of service, a section linking to our 'About' page about the project and authors, testimonies, then a back to top button. It gives a grand welcome to all who comes to our site, especially when we know how important the matter at hand is. In the backend, I also built additional SQL DDL tables to store new data associated with model 2, and converted all `pd.read_csv()` functions into new tables that uses RESTful API. Any further changes are typically small UI tweaks, such as the star rating system on the home page.