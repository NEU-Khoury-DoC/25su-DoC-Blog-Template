---
title: "Project - Phase III"
date: 2025-06-05
draft: false
description: "Our Idea"
slug: "phase2post"
tags: ["project", "Setup"]
authors:
    - "alpberrak"
    - "elianne_mejia"
    - "JessicaPoblete"
    - "mahika_modi"
showAuthorsBadges: true
---
# Project Updates
As a result of feedback we recieved during our mock presentation, we have decided to change our Diplomat persona to a European Commissioner persona since we want this persona not be tied to a specific country but rather be able to allocate EU funding towards member countries based on how much money they already spend on social programs and the amount of refugees they are acceptin. 
# Data Models 
> 
# Routes 
# User Pages 


# Machine Learning Models 

## Logistic Regression Model 



![Social Spending Line Plot 1](/social_spending_1.png)
![Social Spending Line Plot 2](/social_spending_2.png)

## Time Series Forecasting 

Our second machine learning model is our time series forecasting model. Our dataset includes the EU countries and the percentage of their GDP that goes towards social spending from 2011-2022. Our model forecasts out 5 years into the future, so we included 5 lag columns in our X matrix. We also had a COVID column to account for increased social spending during COVID years. This machine learning model will be primarily used my the EU Commissioner persona to be able to allocate funds strategically since the model will show them how much countries will spend on social programs in future years. The proof-of-concept model is fully finished, but we still need to cross validate and implement it into the actual app. As seen by the plots below, the time series model performs fairly well.

![Actual vs Predicted Scatterplot](/actual_vs_predicted.png)
The actual vs predicted datapoints appear to be pretty linear which is a sign that the model is performing decently well.
![Histogram of Residuals ](/histogram_of_residuals.png)
The bars in the historgram all from somewhat of a normal distribution around 0 besides one outlier which may be worth looking into in the future. 

