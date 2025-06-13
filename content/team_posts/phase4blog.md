---
title: "Project - Phase IV"
date: 2025-06-13
draft: false
description: "Proof of Concept - Starting Deployment"
slug: "phase4post"
tags: ["project", "Setup"]
authors:
  - "katherineahn"
  - "anoushkaabroal"
  - "arthurhuang"
  - "shivenajwaliya"
showAuthorsBadges: false
---

#Project Reflection

After five weeks, we have put together our platform Care Compass. We have spent our time improving and implementing our machine learning models, as well as creating our tables and updating our API Layer so that the backend integrates seamlessly with the front end. Our platform provides users with future predictions of healthcare values, information about similar healthcare systems, and country information in our country profile. Our UI has been updated throughout this process, and is now user-friendly with streamlit resources such as buttons, drag-and-drop, and sliders. Below, we articulate a bit more in-depth about our work processes, and we include screenshots of some of the front end pages.


#ML MODELS: 

##Autoregressive Model: 

The autoregressive model was a new addition during this phase which was aimed at replacing the linear regression model from phase 3, which was a poor fit for the World Health Organization data we were trying to predict, which is time series data. The autoregressive model is accessible by two of the user person types. The first being the student user, who is able to interact with the autoregressive model on their country comparator page which allows them to see a graph of the historic and predicted values of up to three countries for one of the given W.H.O datasets (live births, general practitioners per 10,000 population, and total expenditure). Specifically the user selects up to three different countries at the top of the page. The user then has the option to see a table for The second is the policy maker user who interacts with the model on the features over time page which allows them to input a country, date, and returns a graph of all the countries values (historic and predicted) up to that point for a given dataset. In order to test the accuracy and reliability of our model, we cross validated the model and calculated the mean squared error, r^2, and residuals of the model for each of our datasets, which can be seen in the images below. For the general practitioners model, the r^2 of 0.88 demonstrates that the regression model fits the variation of the data well. This is further supported by the mean squared error of 0.04 which shows very little difference between the model predicted values and the actual values on average. In terms of residuals, the residuals over order graph seen below does not seem to demonstrate any significant patterns/trends within the data, which is an indication that the model does not possess autocorrelation. This is the same conclusion with the model for live births, that has a r^2 of 0.79, a MSE of 0.007, and a residuals over order graph without pattern. However, the total expenditure model possessed an r^2 of 0.14 and had an mse of 314, which indicates that the autoregressive model is not a great representation of total expenditure. Based on these analyses, it can be concluded that the autoregressive model can be considered a “good” model for predicting general practitioners and live births over time, but not for total expenditure.

###General Practitioners Analysis:
![genprac_value](genprac_values.png)
![genprac_graph](genprac_graph.png)

###Live Births Analysis:
![livebirths_value](livebirths_values.png)
![livebirths_graph](livebirths_graph.png)

###Total Expenditure Analysis:
![expenditure_value](expenditure_values.png)
![expenditure_graph](expenditure_graph.png)

##Cosine Similarity Model:

The cosine similarity model that we worked on during phase 3 is now fully implemented. The user is now able to rank their priority of the healthcare factors: Prevention, Risk Environment, Health Systems, International Norms Compliance, Rapid Response, and Detection & Reporting. The user can drag-and-drop to rank these factors, and then use sliders to fine tune their ranking weights. Each factor also has a little information tooltip, to explain what each factor really means (a bit of information on the subcategories in the ghs_index). A route is used to get the cosine similarity information after the calculations are put into a dataframe. The visualizations include a bar chart that has the top five countries and their similarity score, as well as a gradient map that is colored based on how similar the country’s healthcare system is to the given country. This model is also used in the Country Profile page, where the sidebar has the top five similar countries based on healthcare factors.  
