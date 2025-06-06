---
title: "Project - Phase III"
date: 2025-06-05
draft: false
description: "Phase III"
slug: "phase3post"
tags: ["project", "Setup"]
authors:
  - "sophiefarrell"
  - "johnnguyen"
  - "emmakulla"
  - "miagiargiari"
showAuthorsBadges: false
---

# Changes Since Phase 2


## Data Sources
We added a fourth dataset! This dataset we deemed as necessary to try and inference wether or not the expenditure given per capita is relevant when considering the cost of living in these different countries. From the advice given from our last blog post, we did see this as necessary as just because Bulgaria gives less family expenditures then Germany, it has a lower cost of living. This dataset contains annual Consumer Price Index (CPI) data for European Union countries. The CPI measures the average change over time in the prices paid by consumers for a market basket of consumer goods and services. It includes the EU27 average and individual country values and spans multiple years.

- Dimensions: Country, Year
- Units: Index value (CPI)
- Observations: Each observation is the CPI value for a specific country and year.

Relevance: This dataset is useful for understanding inflation trends across Europe. For aspiring parents or families considering relocation, the cost of living—as reflected in the CPI—can influence decisions about where to move, especially when considering the expenditures given to citizens.. Politicians and economists can use this dataset to compare how inflation varies across countries and time, and to assess how these trends may affect birth rates or the affordability of raising a child.

## ML Model Clarity
After phase two, we had certain topics to consider regarding moving forward with our models. We decided the best way to break up expenditures was into three categories: total cash expenditures, maternity expenditures (grants given for childbirth/throughout maternity), and service grants (grants for child care, at-home accommodations, etc.).

## Visualizations

{{< iframe src="birth_rate.html" width="600%" height="600" >}}

Regarding our visualizations, we decided to scrap two of the three we produced last phase, only keeping and fully implementing the crude birth rate visualization shown above. Our other two seemed to not convey useful data, so we decided to go a different route, which we will explain further.


# Phase 3


## REST API Matrix
| Resource | GET | PUT | POST | DELETE |
| ---------|-----|-----|------|------  |
| /locations | Gets all daycare locations from DaycareLocations (can be filtered by country) |  | Adds a new daycare location to DaycareLocations | |
| /locations{daycare_id} |  | Updates opening_time, closing_time, or monthly_price for this daycare |  | Makes this location inactive and no longer visible |
| /groups | Gets a resources from AffinityResources (can be filtered by type, country) |   | Adds a new resource to AffinityResources |   |
| /policy | Gets all policies from Poliies |   | Adds a new policy to Policies |  |
| /weeklyhours | Gets all weekly working hours (can be filtered by country)|  |  |  |
| /expenditure | Gets all expenditures from (can be filtered by type) |  |   |   |


## App In Action
![businesspage](/BusinessPlanningPage.png)
![addlocationpage](/AddNewLocation.png)


# Visualizations

## Eura Pean Employment Trends Observation

![Employment Trends Bar Graph](/EU_EMPL_.png)

This visualization was made for Eura Pean so she can observe employment trends in different countries and this will aid her in choosing a country to relocate to. This bar graph takes in three inputs, which are are gender, employment status, and country. We included hover data so when you hover your curser over a bar it will tell you the country (or if it is the EU average), as well as the average weekly working hours quantified.

## Childcare Services Expenditures by EU Country Choropleth Map

![Choropleth Map](/CaraDayExpendChoropleth.png)

The Chorpleth map generated using plot.ly shows all European Union countries and colored them coordinating with the total amount received in grants for childcare services. The more the country receives in grants the darker it is colored on the map and the color corresponds with the scale. This map will help Cara Day because it will show her which countries get the most aid for childcare, proving some to be more affordable for her needs than others.

## Average Workhours Split by Genger

{{< iframe src="gender_employment_viz.html" width="100%" height="600" >}}

This plot aims to show the average weekly working hours for both males and females in the selected country. This plot we plan will be used mainly for Paul's persona, as he will be assessing resources (mock) that suggest how much time parents should spend with their children to form healthy and happy bonds with them. He will use this plot to see whether or not the average work hours of his country align with the recommended guidelines, and if not, what legislation can he pass that will resolve this issue.

## Expenditures and CPI Index

This visualization, although not made yet, will be an extremely useful one for our app. As recommended, we saw it necessary to compare a cost of living index with the expenditures provided in order to determine whether or not these expenditures will truly 'make a difference' in terms of child planning. We hope to place this visualization by our second model, which Cara and Eura will use. This visualization will take in the top 5 countries recommended by the model, and compare the expenditures provided (total cash benefits), and the CPI index for the country, so Cara and Eura can then make more informed decisions on which countries would be the best to expand to/move to.

# ML Models


This phase included the completion of our first ML model! This model is designed to predict the birth rate per thousand people in a country based on key socioeconomic indicators. It is aimed at helping policy makers understand how factors such as work hours and social spending relate to population growth and what legislation can be pushed to affect birth rate. This is a linear regression model, trained using the normal equation. Our second model, the reccommendation system, is still underworks, yet will use similar frameworks in terms of how expenditure inputs are split up.

The inputs:
- Weekly Hours: Average weekly working hours
- Cash Per Capita: Total public cash benefits per person
- Maternity per Capita: Benefits given during maternity/at childbirth
- Services per Capita: Public spending on services (for education, daycare) per person

![Services](/services_birth.png)
![Work Hours](/workhours_birth.png)
![Cash Expenditures](/cash_birth.png)

After talking to Dr. Gerber (due to struggling R^2 Values) we decided it was best to include both squared and cubed values for work hours, and squared values for cash and services per capita, as this seemed to best fit these features graphs.

Standardization:
All features were standardized by subracting the mean of the feature from the original feature value, and subtracting that by the standard deviation of the feature. This helped to ensure consistency among the data values and make sure all features were on the same scale.

Training: To train the model, we used a cleaned and merged version of our data sets, that contained the rows, country, birth rate, working hours, as well as the three types of expenditure, and the CPI value of each country. The weights of the model were computed using the normal equation, with the prediction being done using these weights.

Model Evaluation:
- MAE: 0.8554452972486888
- R²:  0.20494214966561752

Model Coefficients:
- intercept 9.709569377990391
- weekly_hours 43.97361741075498
- cash_per_capita -1.5466764388529706
- maternity_per_capita 0.7253613278930059
- services_per_capita -0.6409148556442577
- weekly_hours_squared -86.3538184164236
- weekly_hours_cubed 41.93959752072412
- cash_per_capita_squared 1.4375034265977322
- services_per_capita_squared 0.27451327522306634

Testing Assumptions:
1. Linearity 

![Actual Vs. Predicted](/act_vs_pred.png)

This assumptions states that the relationship between the independent and dependent variables is linear. We checked using this plot, and observed that the plot did show a moderate linear trend, with no strong non-linear patterns. 

2. Independence of Errors

This assumption states that residuals should be independent, and that the error of one observation should not depend on another. Since our data is of different countries, there is no serious correlation. 

3. Homoscedasticity

![Residuals vs. Fitted (Predicted) Values](/resids_vs_pred.png)

This assumption states that the variance of residuals should be constant across all levels of the predicted values. Based off of the visualization, the residuals did appear to be randomly distributed. 

4. Normality of Residuals

![Histogram](/histogram_resids.png)

![Q-Q](/Q_Q_residuals.png)

This assumption states that residuals should be normally distributed, the histogram does show a normal distribution. However, the Q-Q plot of the residuals did show some deviation.

5. Multicollinearity

![Correlation Heatmap](/correlation_heatmap.png)

This assumption states that independent variables shouldn't be strongly correlated with one another. Based off of our heatmap, and the fact that we have some cubed and squared terms, there is moderate correlation.




