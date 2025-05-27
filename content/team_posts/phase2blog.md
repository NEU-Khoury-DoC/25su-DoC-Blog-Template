---
title: "Project - Phase II"
date: 2025-05-27
draft: false
description: "Proof of Concept - Gathering Data and Designing"
slug: "phase2post"
tags: ["project", "Setup"]
authors:
  - "katherineahn"
  - "anoushkaabroal"
  - "arthurhuang"
  - "shivenajwaliya"
showAuthorsBadges: false
---
# Project Updates
We began this phase by revisiting and refining our user archetypes, making each persona more specific and realistic. We added names, contextual details, and motivations that better aligned with the updated features of our app. For example, our original traveler persona was reframed as Archibald Bridgemont, a parent relocating to Europe with his family, a change that made more sense for features like personalized healthcare system matching. Similarly, Nancy the policymaker was rewritten to focus less on a single country and more on globally informed, evidence-based reform, reflecting our system’s international comparison and forecasting capabilities. Gale, the student, was also given more context and academic grounding, reinforcing his need for tools like time-series charts and visual comparisons.

These refined personas helped us anchor our technical decisions to real, use-driven goals. Updates to the full set of personas can be viewed in our [Phase I blog post](https://arthur-t-huang.github.io/Care-Compass-Blog/team_posts/phase1post/)

We also went back and articulated our data sources better, and found a new, more comprehensive data set as well, that changed some of the technicalities we wanted in our inital plan. Due to this, we also changed those concepts to match our new vision in our first blog post. 

This shift in data informed several important technical updates. Most notably, we moved away from our original idea of allowing users to assign custom weights to healthcare factors and instead implemented a k-nearest neighbors (k-NN) model to generate personalized country recommendations based on user priorities. We also introduced a time series forecasting model that enables users to view historical trends and predict future values for key healthcare indicators.

Together, these updates helped us move from a loosely scoped concept to a more concrete, implementable system with clearly defined features tied directly to our personas.

# Data Sources:
At the end of Phase I, we had gathered data from two datasets, households impoverished by out of pocket payments, and general practitioners per 10,000 population. For Phase II, in addition to cleaning and visualizing these two datasets, we have also gathered, cleaned, and graphed out data from 9 new datasets, as updated in our [blog post for phase 1](https://arthur-t-huang.github.io/Care-Compass-Blog/team_posts/phase1post/#data-sources). 8 of these new datasets were pulled from the World Health Organization API, the other dataset web scraped from the Global Health Security Index, to give us that overall score we were looking for. For each of the World of Health datasets, the gatherer information was fitted into a dataframe which had distinct country and date columns, since every W.H.O dataset contained these two values. Additionally, the Global Health Index dataset contained 300+ columns of factors which were used to help calculate the overall score for a country (ex. Antimicrobial resistance, Access to potable water, etc). Some of these factors were then visualized in comparison to the the overall score of a country, and we plan on including factors with high correlation to overall score to the slider feature mentioned in the [blog post for phase 1](https://arthur-t-huang.github.io/Care-Compass-Blog/team_posts/phase1post/#data-sources).
We have visualized a couple of the datasets in different ways as they relate to the wireframes that we plan to implement: 
We have visualized a couple of the datasets in different ways as they relate to the wireframes that we plan to implement: 

# ER Diagrams:
Below are localized ER diagrams for each personna: the green diagram corresponding to the mover Archibald, red diagram corresponding to the student Gale, and the blue diagram corresponding to the policymaker Nancy.

![image](moverER.png)
![image](studentER.png)
![image](policymakerER.png)

Further, the global ER model is seen here:

![image](globalER.png)

The relational diagram was further derived as:
![image](relationalDiagram.png)

Based on our global data model, a first pass of our SQL DDL can be seen below.

<pre> DROP DATABASE IF EXISTS carecompass_database;
CREATE DATABASE carecompass_database;
USE carecompass_database;

-- create country table
DROP TABLE IF EXISTS country;
CREATE TABLE country
(
    id   INT PRIMARY KEY,
    name        VARCHAR(50),
    region      VARCHAR(50),
    strengths   VARCHAR(50),
    weaknesses  VARCHAR(50),
    score       FLOAT,
    info        VARCHAR(50),
    time        DATETIME
);

-- create users table
DROP TABLE IF EXISTS users;
CREATE TABLE users
(
    id               INT PRIMARY KEY,
    name             VARCHAR(50),
    userType         VARCHAR(50),
    qualityWeight    FLOAT,
    accessibilityWeight FLOAT,
    affordabilityWeight FLOAT,
    outcomeWeight       FLOAT,
    countryID       INT,
    FOREIGN KEY (countryID) REFERENCES country (id)
);

-- create score projection table
DROP TABLE IF EXISTS score_project;
CREATE TABLE score_project
(
    time    DATETIME,
    targetScore     FLOAT primary key
);


-- create overall score table
DROP TABLE IF EXISTS overall_score;
CREATE TABLE overall_score
(
    overallScore FLOAT PRIMARY KEY,
    qualityScore FLOAT,
    accessibilityScore FLOAT,
    affordabilityScore FLOAT,
    outcomeScore FLOAT
);

-- create factors table
DROP TABLE IF EXISTS factors;
CREATE TABLE factors
(
    factorID    INT PRIMARY KEY,
    name        VARCHAR(50),
    score       FLOAT,
    weight      FLOAT,
    countryID   INT,
    overallScore   FLOAT,
    targetScore     FLOAT,
    FOREIGN KEY (countryID) REFERENCES country(id),
    FOREIGN KEY (overallScore) REFERENCES overall_score(overallScore),
    FOREIGN KEY (targetScore) REFERENCES score_project(targetScore)
);


-- create comparator table
DROP TABLE IF EXISTS comparator;
CREATE TABLE comparator
(
    country1ID  INT,
    country2ID  INT,
    country3ID INT,
    FOREIGN KEY (country1ID) REFERENCES country(id),
    FOREIGN KEY (country2ID) REFERENCES country(id),
    FOREIGN KEY (country3ID) REFERENCES country(id)
);

-- create country_compare table
DROP TABLE IF EXISTS country_compare;
CREATE TABLE country_compare
(
    countryID   INT,
    Country1_ID   INT,
    Country2_ID    INT,
    Country3_ID   INT,
    FOREIGN KEY (countryID) REFERENCES country(id)

);

-- create user_score table
DROP TABLE IF EXISTS user_score;
CREATE TABLE user_score
(
    userID   INT,
    overallScore    FLOAT,
    FOREIGN KEY (userID) REFERENCES users(id),
    FOREIGN KEY (overallScore) REFERENCES overall_score(overallScore)
);
 </pre>

Our current wireframes can be viewed here: [Download the pdf](assets/wireframe.pdf)

