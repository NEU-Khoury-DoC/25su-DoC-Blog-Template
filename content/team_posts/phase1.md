---
title: "Project - Phase I"
date: 2025-05-20
draft: false
description: "Proof of Concept"
slug: "phase1post"
tags: ["project", "Setup"]
authors:
  - "katherineahn"
  - "anoushkaabroal"
  - "arthurhuang"
  - "shivenajwaliya"
showAuthorsBadges: false
---

# Project Description:
With an expansive network of public health knowledge at our fingertips, evaluating and comparing healthcare systems across countries can be a complex and overwhelming process. Our project aims to simplify this by evaluating complex public health data and providing users access to succinct, intuitive insights, making it more easily accessible and understandable to a broader audience of users.

We are building an application that helps users explore and evaluate the healthcare systems of different countries based on **six core factors** from the Global Health Security Index:
- Prevention
- Detection and Reporting
- Rapid Response
- Health System
- Compliance with International Norms
- Risk Environment

We are utilizing the Global Health Security Index, which provides a standardized scoring system across six core healthcare factors to generate a composite assessment for each country. Rather than allowing users to customize weights directly, we leverage the index to implement a machine learning model using k-nearest neighbors (k-NN). This enables users to express their healthcare priorities through sliders, which are transformed into a preference vector and compared against normalized country data to identify the most similar healthcare systems.

The resulting country matches are visualized through ranked comparisons, interactive heat maps, and a side-by-side comparison tool for exploring differences in key health indicators. In addition, users can track how selected indicators have changed over time and view predictive forecasts for future performance, offering a forward-looking perspective based on historical trends.

The application converts raw public healthcare data to insights to drive equitable improvements and informed populations regarding healthcare around the world.


# Personas/Archetypes: 
## 1. Student studying _Global Health_
**Description:** Gale is a second year student at Northeastern University majoring global health. He is researching healthcare systems in various countries for his report for his Introduction to Global Health class. He wants to make comparisons between systems in order to properly report back to his class and inform them about the benefits and drawbacks of the healthcare systems between countries. Gale continues with the intention to come up with an ideal (or “the _best_”) healthcare system. 


**User Stories:**
- As a student, I want to compare healthcare quality across multiple countries, so that I can identify which systems produce the best outcomes.
- As a student, I want to access key health indicators like coverage and affordability in one place, so that I can easily cite and present data for class projects.
- As a student, I want to generate graphs comparing countries' health system performance, so that I can visually support my claims in presentations.
- As a student, I want to project changes in, specifically, a country's life expectancy over time, so I can monitor the longevity of the population and the overall health of the population.
- As a student, I want to track changes in health system performance over time, so that I can assess the impact of past reforms or crises.


## 2. Individual moving abroad
**Description:** Archibald Bridgemont is planning a long-term move to Europe with his wife and their young daughter, but hasn't yet chosen which country. He’s looking for a place with a strong and trustworthy healthcare system, where health risks are well-managed, medical needs are reliably met, and public institutions are stable and responsive. Because he values safety, preparedness, and long-term access to care, Archibald wants to explore countries that align with his personal healthcare priorities using clear comparisons and data-backed recommendations. This traveler may have a family, so they also just want to know the general coverage and accessibility that they would be able to receive. 


**User Stories:**
- As a future resident, want to express my healthcare priorities so that I can receive a personalized list of countries whose healthcare systems best match our needs. 
- As a future resident, I want to see a visual map showing how well different countries align with my selected health priorities, so I can easily compare options across the region. 
- As a future resident, I want to explore detailed country profiles with key healthcare insights and contextual information, so I can better understand what living there might be like and make an informed decision.
- As a future resident, I want to see which countries are most similar to a given one, so I can consider strong alternatives that align with my healthcare priorities.


## 3. Policymaker analyzing current healthcare institutions
**Description:** Nancy is a public health policymaker focused on improving her country’s healthcare system through evidence-based reform. She often looks beyond her borders to understand how other countries perform across key areas like prevention, emergency response, and health infrastructure. She’s especially interested in identifying countries with similar healthcare profiles to explore successful strategies that might translate well locally. Nancy also wants to monitor key health indicators over time and forecast future trends, helping her evaluate the impact of past policies and anticipate where new efforts are most needed. For her, global comparison isn’t just a reference point — it’s a tool for real-world decision-making. 


**User Stories:**
- As a policymaker, I want to select a country and view its performance across core healthcare factors, so I can assess its strengths and weaknesses in key areas like prevention and health infrastructure.
- As a policymaker, I want to see which countries are most similar to the one I’m analyzing, so I can explore proven strategies from comparable systems.
- As a policymaker, I want to view how a specific healthcare indicator has changed over time in a given country, so I can evaluate the impact of past policies or reforms.
- As a policymaker, I want to forecast the future trajectory of a selected healthcare factor, so I can anticipate challenges and plan more effectively.

# Models: 
**1. k-Nearest Neighbors (k-NN): Personalized Country Matching**
Used to match users with countries whose healthcare systems align most closely with their personal priorities. Users express their preferences across six key health system factors (e.g., prevention, response, infrastructure), and the system uses k-NN to calculate similarity between the user’s input and each country’s normalized profile.

Used by: Future Resident, Policymaker
Feature link: Slider-based input → ranked list of top-matching countries

**2. Predictive Modeling: Indicator Forecasting**
Used to project future values for specific healthcare indicators (e.g., life expectancy, total health expenditures) based on historical trends. This supports forward-looking insights for both students and policymakers.

Used by: Students, Policymaker
Feature link: Time series chart + k-year prediction overlay for selected indicators


# Data Sources: 
For our data sources, we have pulled together a variety of features that will be further explored through our Machine Learning Models. We list two of the data sources below as examples of our ability to successfully access the data. 

**Data Source 1:**
Generalist medical practitioners, per 10 000 population:

The following dataset provides the number of general medical practitioners in relation to the total
population of the country for a list of countries in Europe as well as in neighboring regions.
This data can serve as a measure of the prevelance of accessabile health services in different countries and regions and can be used in conjuction with other gathered data in order to determine a numerical ranking/evaluation of a countries healthcare system.

Dataset Json:
![image](Practioner_dataframe.png)



**Data Source 2:**
Households impoverished after out-of-pocket healthcare payments

The following dataset displays the percentage of households who are classified as impoverished after
enduring out of pocket medical payments. This data can serve as a critical factor in determining whether a country's healthcare system is afforable and avaliable for the general population.

Dataset Json: 
![image](impoverished_dataFrame.png)

These are two datasets that we would consider impelemting in reference to the factors we aim to focus on, as we also plan on including additional datasets from the World Health Organization throughout the course of this project. We simply chose these datasets to highlight, as they help showcase that we can query from the WHO data warehouse. We will probably have more than 3 datasets for each key factor.     

Other datasets include:
- Life expectancy in Years, from the WHO data warehouse 
- Infant Mortality Rates, from the WHO data warehouse 
- Total Health Expenditure, from the WHO data warehouse
- Catastrophic Health Spending in all wealth classes, from the WHO data warehouse
- Percentage of children vaccinated against measles, from the WHO data warehouse
- Live births per 100 population, from the WHO data warehouse 
- Percentage of Overweight and Obese children, from the WHO data warehouse
- Life Satisfaction Score (Scale 1-10), from the WHO data warehouse
- Healthcare "Scores" for countries, based on a myriad of features from the Global Health Index 


