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

## Mock Data
Based on the feedback we got after our Phase 3 presentation, we decided to add more to the mock data we are generating. Now, daycares have more information than just shallow opening hours. Each location has 10 years worth of data on their budget, prices, enrollment rates, etc. We also were more descriptive with the mock data we already had by adding more precise locations (ex: city) and adding a description section to Policies and AffinityResources.

## Data Model
Because of our changes with the mock data, we needed to update our data model to better reflect the attributes we added. A new entity, DaycareData, was added as well as changes in attributes to other tables such as Policies and Affinity Resources. Additionally, we added a UserRoles entity that will authenticate the user to see certain pages (ex: Politician sees Politician pages but not Parent pages). We also made some changes to our REST API Matrix due to the changes to our model and just unexpected features we came up with during this phase. You'll see the full matrix below in the Phase 4 section of this post. 

## Visualizations

![percapita](/CaraVizPerCapita.png)

We edited a previous visualization that was created for phase 3, which was a choropleth heatmap which showed the amounts of grants each country in the EU recieved for childcare expenditure. The edit that we made was switching it to show the amount per capita rather than the total for each country, so that the number was not just reliant on the country's population.

## Models
In regard to our models, phase four is where they truly began to take shape! We completely integrated both our models. Model one evolved from phase two, with all cubed features being removed, as well as adding a year feature, making the model predict the birth rateg for 2024. Since phase three, we have further developed all pages of our app, creating different visualizations and features to add value to our users' experience. 


# Phase 4

## Data Model

### Final Schema
![finalschema](/database_diagram.png)

This is the final schema for our database. It includes a User entity, each of which has a role. These roles determine the pages that the user will see when they log in. Users may also have Notes that they make while navigating the app. Additionally, Users with the role of daycare_operator may have DaycareLocations, which represent a daycare that the user owns. DaycareLocations also have DaycareData, which is basic data that can be used for analysis of the daycare location. Additionally we have the entity Policies, which detail different policies that could influence the birth rate and is currently composed of mock data. Another entity using mock data is the AffinityResources entity, which stores different resources that a user with the role of parent may find useful. This includes affinity groups, charities, and articles. Our real data is stored in EUBirthData, EUCPI, Children_FamilyBenefits, and EUEmployment. These entities store the birth rate by year of a country, the Consumer Price Index (CPI) of a country by year, different benefits expenditures of a country, and weekly working hours of a country by numerous factors. Our ML Model weights are stored in Model1Weights and eu_family_employment_data. 


### REST API Matrix
| Resource | GET | PUT | POST | DELETE |
| ---------|-----|-----|------|------  |
| /locations | Gets all daycare locations from DaycareLocations (can be filtered by country) |  | Adds a new daycare location to DaycareLocations | |
| /locations/{daycare_id} | Gets all information stored about this daycare in DaycareLocations and DaycareData |  |  | Moves this location to a deleted locations table |
| /groups | Gets a resources from AffinityResources (can be filtered by type, country) |   | Adds a new resource to AffinityResources |   |
| /policy | Gets all policies from Poliies |   | Adds a new policy to Policies |  |
| /allpolicy | Gets all policies (can be filtered by multiple values for one attribute) | | | |
| /weeklyhours | Gets all weekly working hours (can be filtered by country)|  |  |  |
| /expenditure | Gets all expenditures from (can be filtered by type) |  |   |   |
| /m1weights | gets all the weights from the first ML model |  |  |  |
| /benefit | Gets all benefit expenditures (can be filtered) | | | |
| /cpi | Gets all of the CPI data (can be filtered by country and year) | | | |
| /data | Gets all of the daycare data from DaycareData (can be filtered by monthly price and year)| | | |
| /data/{id} | Gets all the daycare data from DaycareData for a specific data id (can be filtered) | | | |
| /daycaredata/{daycare_id} | Gets all the daycare data from DaycareData for a specific daycare (can be filtered) | Updates data for this specific daycare id | | |
| /notes | | | Creates a new note | |
| /notes/{user_id} | Gets this user’s note | | | Deletes this user's note|
| /api/birth-rates | Gets information about birth rates from EUBirthData | | | |
| /role/{role_id} | Gets all users with this role_id | | | |

This is our final REST API Matrix with all of the routes we created in our project. The Phase 3 blog post still has the old matrix for comparison. As you can see, there are a lot more routes this time around, and while many of them are GET requests, there are a good handful of other requests as well. 


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


## Model 2

In this phase, we fully implemented our second machine learning model, which was a recommendation model made for our day care owner and to be parent. In previous phases, we created a proof of concept and very rough skeleton code. In this phase however, we fully sought it through and made the concept work in the app as well. We experimented with a few different ways to create the recommendation model, and landed on using cosine similarity to match user preferences to normalized country-level statistics. Because of this, every new user input dynamically produces updated results, which shows as a ranked top 5 list of best countries that matches the user's preferences. For the day care user, it also shows a bar graph with market fit scores by country as well as a full analysis on all of the country's similarity scores. For the to-be parent, it shows a comparison bar chart of match scores by country, a plot of feature comparisons across top countries, as well as a choropleth heat map showing country's match scores. This real-time matching approach allowed us to continuously test the model’s behavior without a train-test split.

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




## Link to our App!

Here is the link to access our app repo: https://github.com/johnncp/25su-DoC-Project-Team-Cool25.git
