---
title: "Project - Phase II"
date: 2025-05-27
draft: false
description: "Phase II"
slug: "phase2post"
tags: ["project", "Setup"]
authors:
  - "sophiefarrell"
  - "johnnguyen"
  - "emmakulla"
  - "miagiargiari"
showAuthorsBadges: false
---

# Changes Since Phase 1

## User Personas
We slightly altered the backgrounds of two of our users. Now, Eura Peon is considering moving countries; Cara Day is now the owner of a daycare chain instead of a single daycare and is considering going global by opening a daycare in another country. Additionally, some of our user stories have changed. We changed two user stories for both Eura Peon and Cara Day, so now Eura's second and third user stories are different and Cara's second and fourth user stories have changed. 

## Data Sources

We added a data source to the two that we started with. This dataset shows federal expenditure on family/children functions (such as birth grants, child allowances, etc.) per year in European countries. This dataset is broken down by expenditure type; it is reported annually and has multiple years. 


Description of data source: This dataset provides many detailed statistics on different expenditures aimed at families and children within EU member states. Itcategorizes these expenditures based off of what is provided, such as cash benefits and what kind. The data was collected annually and accessed on EUROstat. 



- Dimensions: Country, Year, Type of Benefit, Means-Testing
- Units: Monetary values presented in millions of euros, or euro per person
- Observations: Each data point represents the expenditure for a specific country, year, type of benefit, and means-testing status

Relevance: This dataset is relevant in understanding the allocation of recources towards child welfare across Europe. It can be used to assess how different countries offer family support within their social protection systems and how these benefits have changed over time. This is relevant for an aspiring parent, who might consider the different benefits countries offer for family support as possible considerations to relocate. This data is vital for politicians as well, to assess how different types of expenditure across countries correspond with birth rates.

# Wireframes
## Start Page Wireframe: 
![wireframe1](/homeWireframe2.jpeg)

This will be the first page users see when they open our site. It will have our logo on the sidebar, the name of our app at the top of the screen, and options for which user they want to sign in as. Each option will have the picture of the user, their name, and a short description of them. 

## Paul E. Tishan Wireframes: 
![wireframe2](/birthRatePredictor2.jpeg)

This screen will be shown after the user logs in as Paul E. Tishan and chooses to use the birth rate predictor. There will be a picture that represents Paul E. Tishan on the sidebar as well as the options to go back home, visit our about section, and logout. There are a lot of different inputs the user can adjust to change the predicted birth rate shown towards the bottom of the screen. Paul will use this to see what policy changes his country can make to increase birth rates, such as increasing the amount parents can receive in daycare grants. 

![wireframe3](/legislationWireframe2.jpeg)

This screen will be shown after the user logs in as Paul E. Tishan and chooses the legislation finder. The user can change the country with a dropdown menu. This will cause the graph on the right to show that country's birth rate over time and cause different laws that country has made regarding focus areas that affect birth rate. Focus areas include social protection benefits, birth grants, daycare grants, etc. The user can also change the focus area in order to filter the laws so they only show legislation passed about that specific focus. 

## Cara Day Wireframes: 
![wireframe4](/businessWireframe2.jpeg)

This screen will be shown after the user logs in as Cara Day and chooses business planning. The user can choose which country they want to see information about and what year in case they want to look at historical data. They can choose a store location so they can set/update the opening and closing times for that location, as well as set the cost that parent pay each month for their child to go to the daycare. I am considering adding in a "Add New Location" button so that the user can add a store in a new country like Cara Day is considering doing. 

![wireframe5](/parentResearchWireframe2.jpeg)

This screen will be shown after the user logs in as Cara Day and chooses parent research. The user can select a country and different articles about things that trouble parents will be shown. The articles will show the name of the article, the author, the date it was published, and a link to the article. 

## Eura Peon Wireframes: 
![wireframe6](/countryPredictorWireframe2.jpeg)

This screen will be shown after the user logs in as Eura Peon and chooses country predictor. The user can adjust the weekly hours they'd prefer to work, select the benefits they find most important (ex: day care grants, birth grants, etc.), toggle on/off if they care about the birth rate of a country, and select the year in the future they want to get their top 3 for. This will generate the top 3 countries based on their inputs. By clicking on the country, the user will get a small paragraph about the country. This screen may also be able to be used for Cara Day when looking for the best location for her new store, but as of now it is designed for Eura Peon. 

![wireframe7](/resourceFinderWireframe2.jpeg)

This screen will be shown after the user logs in as Eura Peon and chooses resource finder. The user can input the country and focus area (ex: single mothers, working mothers, women in STEM, etc.) for the resources they would like to see. Then a list of resources will be generated, including helpful articles, charities that donate to the focus area inputted, afinity groups related to the focus group, etc. Each resource listed will be able to show the country it is from/in, when it was founded/published, what focus area it is under, and a link to the resource. 

# Data Visualization

![Eura Pean Average Public Cash Benefits for Family Function per Person By Country](/CashBenEU_BAR.png)

The bar chart showing average public cash benefits per person reveals that Poland ranks significantly lower than many other EU countries in terms of financial support for families. For Eura Pean, a single woman in Warsaw considering adopting a child, this result directly impacts her decision-making. Seeing that countries like Luxembourg, Germany, and the Netherlands offer far higher levels of cash benefits, Eura may feel that Poland’s support system could leave her financially strained, especially while managing a demanding job. These results provide her with evidence that relocating to a country with more generous parental support could make raising a child more financially feasible and secure, helping her weigh the true cost of parenthood as a single mother.

![Cara Day Birth Rate vs. Childcare Expenditure per Person by Country-Year](/BirthRateCARA_SCATTER.png)

This graph is a good and valuable tool for Cara Day because she is considering expanding her business to other countries. By plotting each country’s average public childcare expenditure per person against its birth rate for multiple years, the visualization lets Cara identify where family support systems are strongest. Countries positioned in the upper right corner of the graph—those with higher birth rates and greater investment in childcare like Denmark—signal markets with growing or stable populations of young children and supportive government policies. These are the best environments for a daycare business to thrive. Conversely, countries with low birth rates and minimal public spending on childcare may not offer sustainable opportunities for expansion. Additionally, because each data point is color-coded by year, Cara can observe trends over time, like whether countries are increasing investment or experiencing declining birth rates. This time-sensitive insight helps her anticipate future demand and align her business strategy accordingly. Ultimately, the graph empowers Cara to make informed, data-driven decisions about where to grow her daycare business based on real demographic and policy patterns across Europe.

![Paul E. Tishian Crude Birth Rate Per Country](/birthrate.png)
This line chart helps Paul by showing how birth rates have changed over time across every country, giving him a clear view of demographic trends in Europe. By tracking birth rates year by year, he can identify which countries are experiencing consistent declines, stability, or growth. This is useful for understanding how broader social or economic conditions may be influencing family planning decisions over time. It also helps Paul compare countries and consider where further analysis, such as modeling policy impacts, might be most relevant based on recent trends. Using this data, he can frame possible legislation to map that of countries who are experiencing growth in their birth rates.

# ER Diagrams

<span style="color:lightblue">Baby Blue:</span> Entity

<span style="color:red">Red:</span> Primary Key

<span style="color:orange">Yellow:</span> Foreign Key

## Eura Pean: Expecting Parent
![Eura Pean ER Diagram](/P2_ER_EuraPean.png)
Ms. Pean is an [expecting parent](https://emmakulla.github.io/Team-Cool-25/team_posts/phase1post/#eura-pean). The ER diagram for her use case includes all data about employment, child-family benefits, and birth data across the EU and time. Her use includes an entity for `ChildcareOptions`, which she would use to compare benefits of various EU nations for expecting parents.

## Cara Day: Daycare Chain Operator
![Cara Day ER Diagram](/P2_ER_CaraDay.png)
Ms. Day is a [daycare chain operator](https://emmakulla.github.io/Team-Cool-25/team_posts/phase1post/#cara-day). The ER diagram for her use case includes all data about employment, child-family benefits, and birth data across the EU and time. Her use includes an entity for `BusinessPlanning`, which she would use to plan the `GeneralLogistics` of the service's facilities as well as plans for future `OperatingHours` with current birth rate trends.

## Paul E. Tishan: EU Politician
![Paul E. Tishan ER Diagram](/P2_ER_PaulETishan.png)
Mr. Tishan is an [EU Politician](https://emmakulla.github.io/Team-Cool-25/team_posts/phase1post/#paul-e-tishan). The ER diagram for his use case includes all data about employment, child-family benefits, and birth data across the EU and time. His use includes an entity for `PolicyAnalysis`, which he would use to plan the finances around a policy change, and details on the type, effect, and cost of the potential legislation.

## All Together: Harmonious Global ER Diagram
![Global ER Diagram](/P2_ER_Global.png)
No matter if our users want to grasp the current climate as a to-be parent, understand as a daycare operator, propose legislation as a politician, the data structure of our app seeks to help them understand their decisions that transforms their own life, those in their community, or the European Union’s ~450 million people.

# Entity-Relationship Diagram
![Global ERD Diagram](/P2_ERD_Diagram.png)
Transforming our Global ER diagram, this ERD clearly lists out the primary and foreign keys of our database design. It also incorporates data storage facilities for storing cleaned and pre-processed ML data features used for training and testing models.

# SQL DDL

Peek at our SQL DDL setup as the foundation for Eurobébé's database.

<span style="color:lightgreen">Green:</span> Machine Learning Data Storage

<span style="color:lightblue">Baby Blue:</span> Entity

<textarea style="width: 100%; height: 200px; resize: both; overflow: auto;">
  DROP DATABASE IF EXISTS eurobebe;
  CREATE DATABASE eurobebe;
  SHOW DATABASES;
  USE eurobebe;

  -- # USER:
  -- ### User
  CREATE TABLE User
  (
      user_id    INT PRIMARY KEY,
      name       VARCHAR(50),
      age        INT,
      occupation VARCHAR(60),
      country    VARCHAR(50)
  );

  -- # DATA:
  -- ### Year
  CREATE TABLE Year
  (
      year    INT PRIMARY KEY,
      user_id INT,
      FOREIGN KEY (user_id) REFERENCES User (user_id)
          ON UPDATE cascade ON DELETE restrict
  );

  -- ### EUBirthData
  CREATE TABLE EUBirthData
  (
      eubd_id          INT PRIMARY KEY,
      country_code     VARCHAR(10),
      birth_rate       DECIMAL(5, 2),
      crude_birth_rate DECIMAL(5, 2),
      year             INT,
      FOREIGN KEY (year) REFERENCES Year (year)
          ON UPDATE cascade ON DELETE restrict
  );

  -- ### EUEmployment
  CREATE TABLE EUEmployment
  (
      eue_id            INT PRIMARY KEY,
      year              INT,
      country_code      VARCHAR(10),
      workforce         INT,
      self_employment   DECIMAL(5, 2),
      work_hours_weekly DECIMAL(5, 2),
      sex               VARCHAR(10),
      industry_sector   VARCHAR(85),
      FOREIGN KEY (year) REFERENCES Year (year)
          ON UPDATE cascade ON DELETE restrict
  );

  -- ### Children_FamilyBenefits
  CREATE TABLE Children_FamilyBenefits
  (
      cfb_id          INT PRIMARY KEY,
      year            INT,
      country_code    VARCHAR(10),
      support_program VARCHAR(85),
      dependent_type  VARCHAR(50),
      euro_amount     DECIMAL(10, 2),
      FOREIGN KEY (year) REFERENCES Year (year)
          ON UPDATE cascade ON DELETE restrict
  );

  -- # FEATURES:
  -- ## Politicians:
  -- PolicyAnalysis
  CREATE TABLE PolicyAnalysis
  (
      analysis_id  INT PRIMARY KEY,
      user_id      INT,
      country_code VARCHAR(10),
      FOREIGN KEY (user_id) REFERENCES User (user_id)
          ON UPDATE cascade ON DELETE restrict
  );

  -- ### PolicyDetails
  CREATE TABLE PolicyDetails
  (
      details_id           INT PRIMARY KEY,
      cost_per_month       DECIMAL(10, 2),
      policy_type          VARCHAR(50),
      effect_on_birth_rate DECIMAL(5, 2),
      analysis_id          INT,
      FOREIGN KEY (analysis_id) REFERENCES PolicyAnalysis (analysis_id)
          ON UPDATE cascade ON DELETE restrict
  );

  -- ## Daycare Operators:
  -- ### BusinessPlanning
  CREATE TABLE BusinessPlanning
  (
      plan_id       INT PRIMARY KEY,
      daycare_id    INT,
      year_forecast INT,
      user_id       INT,
      FOREIGN KEY (user_id) REFERENCES User (user_id)
          ON UPDATE cascade ON DELETE restrict
  );

  -- GeneralLogistics 
  CREATE TABLE GeneralLogistics
  (
      oper_id            INT PRIMARY KEY,
      staffing_demand    INT,
      financial_analysis TEXT,
      plan_id            INT,
      FOREIGN KEY (plan_id) REFERENCES BusinessPlanning (plan_id)
          ON UPDATE cascade ON DELETE restrict
  );

  -- OperatingHours 
  CREATE TABLE OperatingHours
  (
      hours_id      INT PRIMARY KEY,
      plan_id       INT,
      year_forecast INT,
      daycare_id    INT,
      FOREIGN KEY (plan_id) REFERENCES BusinessPlanning (plan_id)
          ON UPDATE cascade ON DELETE restrict
  );

  -- ## Expecting Parents:
  -- ### ChildcareOptions
  CREATE TABLE ChildcareOptions
  (
      option_id      INT PRIMARY KEY,
      country_code   VARCHAR(10),
      cost_per_month DECIMAL(10, 2),
      user_id        INT,
      FOREIGN KEY (user_id) REFERENCES User (user_id)
          ON UPDATE cascade ON DELETE restrict
  );


  -- # INSERTING TEMPORARY "DATA":
  -- ## Users (politicians, daycare operators, to-be parents)
  INSERT INTO User (user_id, name, age, occupation, country) VALUES
  (1, 'Mark Fontenot', 80, 'Politician', 'France'),
  (2, 'Eric Gerber', 80, 'Daycare Owner', 'Germany');

  -- ## YEAR
  INSERT INTO Year (year, user_id) VALUES
  (2023, 1),
  (2024, 2);

  -- ## EUBirthData
  INSERT INTO EUBirthData (eubd_id, country_code, birth_rate, crude_birth_rate, year) VALUES
  (1, 'BE', 10.8, 10.9, 2023),
  (2, 'DE', 9.3, 9.4, 2024);

  -- ## EUEmployment
  INSERT INTO EUEmployment (eue_id, year, country_code, workforce, self_employment, work_hours_weekly, sex, industry_sector) VALUES
  (1, 2023, 'BE', 29500000, 11.2, 36.5, 'Female', 'Transportation'),
  (2, 2024, 'DE', 44800000, 9.8, 35.2, 'Male', 'Finance');

  -- ## Children_FamilyBenefits
  INSERT INTO Children_FamilyBenefits (cfb_id, year, country_code, support_program, dependent_type, euro_amount) VALUES
  (1, 2023, 'BE', '$ for families', 'Child under 18', 1912.12),
  (2, 2024, 'DE', 'Alien Assistance', 'First and Second Child of Asylum Seekers', 25.00);

  -- ## PolicyAnalysis
  INSERT INTO PolicyAnalysis (analysis_id, user_id, country_code) VALUES
  (1, 1, 'BE'),
  (2, 2, 'DE');

  -- ## PolicyDetails
  INSERT INTO PolicyDetails (details_id, cost_per_month, policy_type, effect_on_birth_rate, analysis_id) VALUES
  (1, 450.00, 'Universal Childcare', 2.3, 1),
  (2, 320.00, 'Parental Leave', 1.8, 2);

  -- ## BusinessPlanning
  INSERT INTO BusinessPlanning (plan_id, daycare_id, year_forecast, user_id) VALUES
  (1, 101, 2026, 2),
  (2, 102, 2028, 2);

  -- ## GeneralLogistics
  INSERT INTO GeneralLogistics (oper_id, staffing_demand, financial_analysis, plan_id) VALUES
  (1, 12, 'Projected: €580,000/year. Staff: €380,000. Operating: 1.5%', 1),
  (2, 18, 'Expansion needs €250,000 investment.ROI: 22%', 2);

  -- ## OperatingHours
  INSERT INTO OperatingHours (hours_id, plan_id, year_forecast, daycare_id) VALUES
  (1, 1, 2025, 101),
  (2, 2, 2026, 102);

  -- ## ChildcareOptions
  INSERT INTO ChildcareOptions (option_id, country_code, cost_per_month, user_id) VALUES
  (1, 'BE', 650.00, 1),
  (2, 'DE', 450.00, 2);
</textarea>

# ML Proof of Concept

Model 1: Paul’s Predictive Model - Supervised
Inputs:
- Weekly Working hours
- Public expenditure 
  - Possibly refine further to include the different types of expenditure (time off, cash benefits)
Y = B0 + B1 * X1 + B2 * X2
X₁: Average weekly working hours
X₂: Expenditure
Y: Birth rate
What data will we be using: Birth rate csv, Expenditure csv, Employment hours csv
Overall: Paul would input desired weekly hours and benefit spending → the model predicts the expected birth rate for his country.

Model 2: Cara & Eura’s Recommendation Model — Unsupervised
Inputs
- Desired working hours
- Importance of benefits (e.g., child care, healthcare, parental leave)
How it works:
A weighted scoring model (or regression-style recommender):
- Each country is scored based on how well it matches the user's preferences.
What data we will be using: Birth rate csv, Expenditure csv, Employment hours csv
Steps:
- Create feature table (country-level):
  - Weekly hours, parental leave, cost of childcare, etc.
- User inputs preference weights:
  - e.g., “Childcare cost = 5 (most important), parental leave = 3, healthcare = 2…”
- Normalize data (so features are 0–1)
- Score countries:
  - Weighted sum of how well each country fits
- Rank top matches
Overall: Recommends best-fit countries to move or expand to in the future (rank based off of similarity to the features of the most desirable ideal country to live in)

# Data Cleaning
Short discussions of how we cleaned our data!

Expenditure Data Source
- In order to clean the “Public Expenditure on family/children function” API I had to remove multiple years, take out all non-EU countries and other combined rows, remove missing values, and change a lot of codes that are very Eurostat-specific. First, we took out all years before 2015 because one of the datasets we had started in 2015 and we wanted them to be easily mergeable for when we did our visualizations. Next, we removed all countries that are not in the EU so that all the datasets could be consistent. Then we standardized all of the column names and country codes paying attention to capitalization. Next, we replaced all NaN values with 0 so that it held only numerical values. We also had to save the dataset to a CSV file so that I was able to use it for my visualizations. The most time consuming of cleaning it was changing all of the Eurostat-given cryptic labels to easily readable and understandable labels, like changing “KND_CHDC” to “Childcare Services” along with fifteen other features and all twelve units because they were also in cryptic codes. 

Birth Rate Data Source
- To clean the “Live Births and Crude Birth Rate” API, we first began by removing all non-EU countries. We also took out all the years before 2015, as that is the year in which we decided to evaluate all of our datasets, as that was the furthest back that all of our datasets went. All of the birth rate data for the EU countries was there, so there were no missing values that I was working with. Finally, we just formatted the CSV into the rows: country, frequency (just annually), year, birth_rate_per_thousand, and live_births. 

Work Hours Data Source
- Cleaning the “Average number of usual weekly hours of work in main job, by sex, age, professional status, full-time/part-time and economic activity” API was a bit of a hassle. First, just like the other datasets, we removed all non-EU countries and years before 2015. A difficult part about cleaning this data was re-naming columns for clarity, such as what “nace_r2” meant in regards to employment status. We dropped rows with missing values and converted any necessary string values to floats. Overall, the dataset is still relatively large, more filtering can be done, such as removing some of the many employment statuses and refining the dataset to just what will be relevant for our personas, something that is to be determined.
