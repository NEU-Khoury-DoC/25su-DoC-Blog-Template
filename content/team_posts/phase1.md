---
title: "Project - Phase I"
date: 2025-05-20
draft: false
description: "Our Idea"
slug: "phase1post"
tags: ["project", "Setup"]
authors:
  - "sophiefarrell"
  - "johnnguyen"
  - "emmakulla"
  - "miagiargiari"
showAuthorsBadges: false
---

![Baby Against EU Flag](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRYTFh9IKUTedGHA0wAe1EPjhTrtf_WCVADOw&s)


# Description

Is quality of life declining? Are politics uprooting longstanding systems? Do things just feel too unstable? Above all, our project draws these questions to an alarming trend: **declining birth rates** in various nations around the globe. South Korea has seen birth rates plummeted. In 2023, the EU saw its [largest decline in birth rate](https://ec.europa.eu/eurostat/web/products-eurostat-news/w/ddn-20250307-1#:~:text=In%202023%2C%203.67%20million%20babies,down%20from%201.46%20in%202022.) since 1961. Exploring this phenomenon deeper, we ask two questions: 

1. Given rising financial uncertainty, how do weekly working hours by sex, age, and professional status correlate with employment rates of parents across different countries in the EU? What nations with more **flexible working arrangements** show higher employment rates for adults with young children (especially mothers)?
2. Between educational attainment and employment rates, what is the relationship among parents with young children across different EU countries? 

Our research hopes to combine these complementary analyses to discover what successful policy frameworks that support families to be successful and economically cared for — especially against the diverse European cultural landscapes. Nurturing the project via Eurostat, we hope to reveal insights through data such as gender inequality (wage disparities, labor market participation), work-life balance (commuting burden, conditions of work), social support systems (social safety net, investment in human capital), or safety (crime levels).

# User Personas

## Eura Pean
Eura Pean is Polish citizen residing in Warsaw, Poland. Although not married, she is thinking about adopting kids from a local orphanage. She has recently taken a managerial position at her local bank, stretching her hours and has made her more cautious about the life-changing decision. She is seeking more research.

User Stories:
- As a local branch bank manager, I want to see how other women balance life at home and life at work, so that I can continue growing my career at the bank, which is a job I love.
- As Eura, I want to compare parental leave options across EU countries, so I can understand if my country's systems will support me as a to-be single mother.
- As someone who's a little worried about financial stability, I want to look at the different economic outcomes for children raised by people like me across the EU, so I can better understand how our systems might affect my adopted child's opportunities.
- As Eura, I want to understand birth rate trends among professional women across the EU, so I can be more informed with my decisions about the journey to parenthood.

## Paul E. Tishan
Paul is a policy maker in Brussels. He's working to raise the birth rate in his country through legislation. He hopes that by targetting factors related to the declining birth rate he can impact potential parents' decision to have children. 

User Stories:
- As Paul, I want to understand how employment hours affect family planning decisions, so that I can propose legislation that encourages work-life balance.
- As a politician, I want to identify countries with both high birth rates and flexible employment policies, so that I can model successful strategies in Belgium.
- As a policy maker, I want to use data to highlight how reducing average work hours might positively influence birth rates, so that I can justify reforms to labor policies.
- As Paul, I want to explore correlations between parental leave policies and birth rates, so that I can advocate for more supportive family benefits.

## Cara Day
Cara is the owner of a daycare in Nice, France. She loves the children that she takes care of every year, but she can't help but notice she has less applicants to attend her daycare than she did 15 years ago. She's curious about the reason why and would like to know how many applicants she'll get in the coming years. 

User Stories:
- As Cara, I want to know different factors that typically affect parents, so that I can have a better understanding of the children under my care and their needs. 
- As a daycare owner, I want to know how many children will apply to my daycare, so that I can prepare my daycare for more or less children by hiring new staff, buying supplies, etc. 
- As a daycare owner, I want to know how long parents of children work on average, so that I can set a reasonable time for parent pick up and drop off. 
- As a business owner, I want to understand why there are less parents than there were in the past, so that I can make plans for the future of my business. 


# Data Sources
The two datasets we chose to evaluate were retrieved from the Eurostat database. Meaning both were accessed from a public API using Python with no authentication or paywall required. 

## API Access

![datapic](/API.png)
## Data Source 1

Dataset one demonstrated average weekly hours worked by individuals in European countries. This dataset has work hours broken down by sex, age group, employment staus, and economic activity. The dataset is reported annually and covers multiple years. 
The structure of the data:
- Dimensions: Sex, age, employment status, worktime, economic status, country, year. 
- Units: Hours per week
- Observations: Many datapoints due to multi-dimensional combinations

Relevance: Helps investigate how working hours across demographics may influence family planning decisions and overall fertility rates. Politicians may use it in exploring policy impacts on the overall work-life balance. Parents may use it to compare average workload norms in different countries. Daycare workers can use this data to estimate the influx of children they will receive and the average hours parents will need care. 


## Data Source 2
Dataset two shows the crude birth rate (or number of live births per 1000 people) in a given population per year. This data contains annual data across European countries and regions, the birthrate is reported at the national level.
The Structure of the Data:
- Dimensions: geographic Area, Year, Sex
- Units: Live births per 100 people
- Observations: 53 geographic areas x 12 years = 636

Relevance: Will help to understand and help predict the declining birth rates, providing standardized and comparable measures of fertility that can be used as our dependent variable. This dataset is relevant to understanding how to respond to demographic changes.
