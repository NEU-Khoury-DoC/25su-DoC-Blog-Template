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
With an expansive network of public health knowledge at our fingertips, evaluating and comparing healthcare coverage internationally may prove to be an extensive and strenuous process. Our project aims to derive succinct, intuitive insights from complex public health data, making it more accessible to a broader audience of users. 

We are building an application that evaluates the healthcare systems of countries based on data derived, which fall into **four core factors**:
- access
- quality of care
- affordability
- outcomes. 
For each factor, key indicators are aggregated and a score is calculated, which may then be combined for a composite score for a given country. For example, given key indicators for _‘Outcome’_ being life expectancy and infant mortality, these may be normalized, weighted, and aggregated to compute one _‘Outcome’_ score. This factor may then contribute 25% of the total score, with the other core factors representative of the other 75%. The country scores are further visualized through heat maps and other comparisons.

Additionally, users may explore customizing the weights used for scoring for each of the four factors, making it personalized to their own priorities and focused use of the app; if a user is only interested in affordability and quality, but still wants to consider access and outcomes, the weights may be 30%, 30%, 20%, 20%, respectively. Another feature of the app includes a side-by-side comparison of nations’ scores and key indicators. 

The application converts raw public healthcare data to insights to drive equitable improvements and informed populations regarding healthcare around the world.



# Personas/Archetypes: 
## 1. Student studying _Global Health_
**Description:** This profile is a student who is interested in researching healthcare systems in various countries. They want to make comparisons between systems in order to properly report back to their class and inform them about the benefits and drawbacks of the healthcare systems between countries. They continue with the intention to come up with an ideal (or “the _best_”) healthcare system.
**User Stories:**
- As a student, I want to compare healthcare quality across multiple countries, so that I can identify which systems produce the best outcomes.
- As a student, I want to access key health indicators like coverage and affordability in one place, so that I can easily cite and present data for class projects.
- As a student, I want to generate graphs comparing health system performance, so that I can visually support my claims in presentations.
- As a student, I want to compare healthcare outcomes across income brackets within a country, so that I can analyze inequality in access and quality.
- As a student, I want to track changes in health system performance over time, so that I can assess the impact of past reforms or crises.


## 2. Traveler(s) checking health systems abroad
**Description:** This profile is a traveler who wants to make sure that they will be safe abroad in terms of healthcare security. They can be nervous about all of the potential dangers of traveling, so they want to see if the care they receive is of a good quality. This traveler may have a family, so they also just want to know the general coverage and accessibility that they would be able to receive.  
**User Stories:**
- As a traveler, I want to understand the accessibility of healthcare where I go, so that I can know if I can rely on the healthcare system, even if I stay in a more remote location while traveling. 
- As a traveler, I want to see whether the target country offers healthcare access for foreigners to determine if any additional travel insurance is necessary to consider. 
- As a traveler, I want to search for countries by healthcare safety score or reliability, so that I can plan my trips around places with higher health standards.
- As a traveler, I want to input my chronic condition (e.g., asthma, diabetes) and see if relevant support or medications are accessible abroad, so that I can travel with confidence.


## 3. Policymaker analyzing current healthcare installments
**Description:** This profile is a policy maker who’s aiming to improve upon their nation’s current healthcare policies. They want to analyse how the systems of other countries compare to those of their own in order to identify areas in which their nation can place heavier focus on, as well as point out successful practices from other countries that can be adopted by their nation.
**User Stories:**
- As a policymaker, I want to understand where my country lacks in healthcare systems, so that I can better create healthcare legislation for future generations. 
- As a policymaker, I want to track changes in health system performance over time, so that I can assess the impact of past legislation. 
- As a policymaker, I want to discern how my country compares to peers in our given region / socioeconomic group.
- As a policymaker, I want to adjust the weighting of the core four factors to align with current policy goals, so I can evaluate areas of policy that may not be as effective as intended.
- As a policymaker, I want to set target scores for each core factor so I can track my country’s progress in healthcare improvement. 

# Models: 
**Personalized Scoring Recommendations** - Countries to travel to given the scoring preferences (weights)

**Clustering** - Group similar healthcare systems

**Predictive Modeling** - Predict how a country’s score might change in the next 5 years based on trends and present day policy

**Principal Component Analysis (PCA)** - reduce multi-dimensional healthcare data into 2D plots 


# Data Sources: 

**Data Source 1:**
Generalist medical practitioners, per 10 000 population:

The following dataset provides the number of general medical practitioners in relation to the total
population of the country for a list of countries in Europe as well as in neighboring regions.
This data can serve as a measure of the prevelance of accessabile health services in different countries and regions and can be used in conjuction with other gathered data in order to determine a numerical ranking/evaluation of a countries healthcare system.

Dataset Json:
![image](dataset1.png)



**Data Source 2**


