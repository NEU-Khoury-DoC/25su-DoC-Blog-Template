---
title: "Project - Phase IV"
date: 2025-06-12
draft: false
description: "Phase IV"
slug: "phase4post"
tags: ["project", "Setup"]
authors:
  - "sophiefarrell"
  - "johnnguyen"
  - "emmakulla"
  - "miagiargiari"
showAuthorsBadges: false
---

# Changes Since Phase 3



## Visualizations

![percapita](/CaraVizPerCapita.png)

We edited a previous visualization that was created for phase 3, which was a choropleth heatmap which showed the amounts of grants each country in the EU recieved for childcare expenditure. The edit that we made was switching it to show the amount per capita rather than the total for each country, so that the number was not just reliant on the country's population.

## Models
In regard to our models, phase four is where they truly began to take shape! We completely integrated both our models. Model one evolved from phase two, with all cubed features being removed, as well as adding a year feature, making the model predict the birth rateg for 2024. Since phase three, we have further developed all pages of our app, creating different visualizations and features to add value to our users' experience. 


# Phase 4

## Data Model



## ML Models

## Model 1

Since phase 3, Model 1 was further refined in order to become a predictive model for the birth rates in 2024 of EU countries. This means the year feature was added, we also removed some of the squared and cubed features to adjust for the strong multicollinearity we saw in phase 3 (as recommended by Dr. Gerber). A quick overview:


The Features:
- Average working hours
- Year
- Maternity per capita
- Services per capita
- Average working hours squared
- Cash per capita squared
- Services per capita squared

Model Evaluation:
- MAE: .8335
- R²: .1998

Model Coefficients: 
- Intercept: 9.67 
- Weekly hours: 3.43
- Maternity per capita: 0.54 
- Services per capita: -1.15
- Year: -0.46
- Weekly hours squared: -3.86
- Cash per capita squared: -1.37  
- Services per capita squared: 2.24

Assumptions:
Through adding these slight tweaks to the model and its features, the testing of the assumptions is relatively similar to what we did in phase 3. As Dr. Gerber explained, our features do still show a strong degree of multicollinearity, as there still are some repeated features in terms of squared/cubed values.

Model In Use:

![slidermenu](/model1.png)

Here is an image of what our first model looks like fully implemented. The user chooses what country they would like to predict for, and the sidebar automatically loads with that country's average weekly working hours, as well as expenditure types for 2023. The user can adjust from there to see what changes affect the birth rate for 2024 and in what way.

Adjustments:

![slidermenu](/pred_birth_vis.png)

We decided to use the predicted birth rates for each country (what the birth rate was predicted to be in 2024 from our model without changing any of the country's data from 2023) and use it to add on to our visualization of crude birth rates over time. The user can see the predicted birth rate for all EU countries in 2024 or choose to switch this feature off. 


Model 2

The inputs:
- Desired working hours
- Importance of benefits
- Maternity/childbirth benefits
- Cash benefits (periodic)
- Services per capita

![slidermenu](/preferences_slider.png)

This is an image of what the slider menu looks like to take the user input on their preferences.

![rankedlist](/ranked_list.png)

This shows the output of the top 5 countries that match the user's input about their preferences.

![matchdata](/country_dataML2.png)

This is an example of the data that is produced for each top 5 country that matches the user's input.




## App In Action

## Link to our App!

Here is the link to access our app:
https://github.com/johnncp/25su-DoC-Project-Team-Cool25