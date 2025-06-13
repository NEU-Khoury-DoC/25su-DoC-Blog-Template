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

{{< iframe src="birth_rate.html" width="150%" height="600" >}}

Regarding our visualizations, we decided to scrap two of the three we produced last phase, only keeping and fully implementing the crude birth rate visualization shown above. Our other two seemed to not convey useful data, so we decided to go a different route, which we will explain further.


# Phase 3

## REST API Matrix
| Resource | GET | PUT | POST | DELETE |
| ---------|-----|-----|------|------  |
| /locations | Gets all daycare locations from DaycareLocations (can be filtered by country) |  | Adds a new daycare location to DaycareLocations | |
| /locations/{daycare_id} |  | Updates opening_time, closing_time, or monthly_price for this daycare |  | Moves this location to a deleted locations table |
| /groups | Gets a resources from AffinityResources (can be filtered by type, country) |   | Adds a new resource to AffinityResources |   |
| /policy | Gets all policies from Poliies |   | Adds a new policy to Policies |  |
| /weeklyhours | Gets all weekly working hours (can be filtered by country)|  |  |  |
| /expenditure | Gets all expenditures from (can be filtered by type) |  |   |   |
| /m1weights | gets all the weights from the first ML model |  |  |  |

The /locations resource has two routes: one for a GET request and one for a POST request. The GET request will get all the daycare locations in the DaycareLocations table. This can be filtered by country, city, and monthly price. This route will be useful for the Cara Day persona and her business prediction page. She needs to be able to see her daycares in order to choose a location to update the opening hours, closing hours, and/or monthly price. This route could also be useful for Eura Peon on a page where she could search for a daycare in a specific country or city. 

The /locations/{daycare_id} also has two routes: one for a PUT request and one for a DELETE request. The PUT request will update the opening time, closing time, and/or monthly price of the given daycare. This route will be useful for Cara Day when changing her business' hours or price in the business planning page. The DELETE request will move the daycare to the DeletedDaycareLocations table if it shuts down or something. This will be useful for Cara Day on her business planning page as well, though it has not been implemented yet. 

The /groups resource is yet another resource with two routes: a GET request and a POST request. The GET request will get all the resources from the AffinityResource table. This can be filtered by focus area, type of resource, and country. This will be useful for the Eura Peon persona and her resources page that will connect her to different resources and affinity groups. The POST request will add a resource to the AffinityResource table in the event that Eura Peon wants to start her own affinity group or charity. 

The /policy resource also has the routes with GET and POST. The GET request will get all the legislation in the Policies table; this can be filtered by country, focus area, and year. This will be useful for Paul E. Tishian and his legislation finder page in order for the legislation to appear on the screen and for him to sort through the policies more easily. The POST request will allow him to add a new policy to the Policies table in the case that he passes a new law. 

The /weeklyhours resource has a route for GET requests; it will get all the average weekly hours from the EUEmployment table. This can be filtered by country and year. This will be useful for all of our personas, as Cara Day is interested in knowing the weekly hours so she can see which countries are best to open new locations in, Paul E Tishian is interested in weekly working hours so he can see how it effects his constituents, and Eura Peon is interested in weekly working hours so she can see which countries have better work-life balance for her potential move and new life as a mother. 

The /expenditure resource has a route for GET requests as well. This will get all the expenditures from the Children_FamilyBenefits table and can be filtered by type. This will be useful for Cara Day when she's researching new locations to open a daycare and wants to know the average daycare grants of a country. It will also be useful for Eura Peon when she wants to see which countries have the best public expenditures for parents. 


## App In Action
![businesspage](/BusinessPlanningPage.png)

This page shows off the /locations GET request route. When the "See Current Locations" button is pressed, the route is called to get the locations and put them in expanders that allows all of the information besides the daycare id and country code to be hidden until you open it. The /locations/{daycare_id} POST route can also be seen here with the "Update Price", "Update Opening Time", and "Update Closing Time" popovers that will open to show a time/number input to call the route and update these values in the database. 

![addlocationpage](/AddNewLocation.png)

This pages shows off the /locations POST request route. The user will add the attributes through the input fields and when they press the "Add Location" button it will add a row to the DaycareLocations table with the values they inputted. 

![birthratepredictor](/InitialBirthPredictor.png)  ![birthratechange](/ChangedSpending.png) 


This page is our birth rate predictor, which uses our first ML model to predict the birth rate based on the different factors the user inputs. It uses the /m1weights GET request route in the View Model Weights expander. 

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

