---
title: "Phase 3 Blog Post"
date: 2025-06-05
draft: false
description: "Blog Post for Phase 3 of the Dialouge Project"
slug: "arthurhuangphase3blog" 
tags: ["authors", "config", "docs"]
authors:
  - "arthurhuang"
showAuthorsBadges : false

---
For phase three of the project lots of my work revolved around the creation of our two ml models, one being a regression model and the other being a cosine similarity model. My work with the regression model built off of our phase 2 deliverable regression model proof of concept. This phase 2 model consisted of a scatterplot and a line of best fit for the corresponding data. For phase 3, I updated this model with the train_test_split function and the linreg_predict function. I then fitted the linear regression model onto the W.H.O expenditure dataset and created an example line of best fit graphs for expenditure over time (years) for designated countries. Later I then transferred this model from the jupyter notebook into the regression.py file within the ml_models folder of the website. The second of the models that I worked on for phase 3 was the cosine similarity model that was fit to the ghs_index dataset. Specifically, I isolated and scaled the ghs_index dataset into a dataframe which consisted of the 6 major factors that went into calculating the ghs_index score. I then tested the model with Vietnam as a comparison to point and returned the top 5 countries that were most similar to Vietnam, as well as the 6 countries that were least similar to Vietnam. For the ghs_index, I also worked with Anoushka to attempt to classify all the countries in the dataset by the corresponding continent, however there are still some discrepancies within this classification. Lastly, I made a route with country_routes.py which transferred and added the General practitioner per 10,000 dataset into a database within the website.

Outside of the project, this weekend, I explored Luxembourg with my close friends which was an incredibly beautiful city that was split between a ridge and a valley. On our free day, we also made a trip to a nearby lake and got to swim and explore the local forests. This past week we also made trips to Eurostat and Wilfred Martens Centre for European Studies, through which I learned the importance of data collection and tech policy within the EU. While in Brussels, I also finally got the chance to get a few boxes of Belgian chocolates for my family back home. 

![Luxemborg](arthurblog3.png)