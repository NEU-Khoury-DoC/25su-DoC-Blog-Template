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
We stored data from the API along with the weight vectors for our logsitic regression ML model into two new tables, AverageAcceptanceRates and Weights. In addition to this, we populated our EducationLevel and Education tables with some mock data for all of the countries in our Country table. As of now, each country in our database associated values for each education level: primary, secondary, and tertiary. We also changed some of the attribute names for our other tables so that they make more sense according to the values they represent. For example, LegalAidApplication previously had a UserID attribute which was a foreign key referencing an ApplicantID for an entry in the AsylumSeeker table. We changed this to also be called ApplicationID so it's easier to understand what this value represents. 

# Routes 
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vT6aAyMz747kqhiRaR1dB4uw8S8n5M3bPqAU4DttqdiKApRwsWaEuF8rghtzfgw84GzTnQ64HPGJPcf/pubhtml?widget=true&amp;headers=false"></iframe>

# Web App Pages
## Refugee Persona
### Acceptance Probability Screen
![AcceptanceProbScreen](/acceptance_prob_screen.png)
This screen uses the route that calls the logical regression model. Here, refugees can see their predicted acceptance probability for their top three countries. 
![LegalAidApplication](/legal_aid_app_screen.png)
This screen shows where refugees can apply for legal aid. Their application gets addded to our database which lawyers will be able to see on their dashboard (this will be implemented in the future)

## EU Commissioner Persona 
![ProjectSubmission](/aid_project_submission_screen.png)
This screen shows where EU commissioners can submit suggestions for new humanitarian aid projects. 


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

