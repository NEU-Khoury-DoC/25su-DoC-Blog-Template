---
title: "Project - Phase I"
date: 2025-05-20
draft: false
description: "Our Idea, Data, Personas"
slug: "phase1post"
tags: ["project", "Setup"]
authors:
  - "aidankelly"
  - "seanbehan"
  - "gabbymontalvo"
  - "mariasamosrivas"
showAuthorsBadges: false
---

# EuroTour: Data Driven European Tourism Platform

![Image of European landmarks](european_image.jpg)

## Project Description
This project delivers a data driven web app that leverages machine learning and country level European datasets. The app is uniquely structured via a diverse range of users interested in road-based travel, infrastructure, and tourism planning. It centers around three primary personas: casual road trippers, national tourism officials, and academic researchers.  <br><br>
For casual travelers, the app acts as a smart trip advisor. It generates a ranked list of countries based on predicted travel ease and enjoyment.  Using a machine learning model trained on variables such as fuel prices, traffic congestion, and road quality. Users can compare countries and plan optimal routes through regions that balance affordability, access, and attractions. <br><br>
For national officials, the app becomes a policy insight tool. It enables benchmarking of their country's road and tourism infrastructure against EU peers. An ML model predicts tourism growth based on road investment, fuel trends, and travel prioritization metrics. This will help officials allocate funding and shape tourism campaigns. <br><br>
Researchers from institutions like KU Leuven use the app to access and analyze multi-year datasets for academic projects. They explore longitudinal trends in tourism and sustainability, using advanced tools that allow them to filter, visualize, and export data for modeling, correlation studies, and publications. This application unifies diverse goals into one intelligent, accessible platform for travel, policy, and research.

## Overall Problem
Despite the vast amount of public data on tourism and road infrastructure within the E.U., there is no unified platform that transforms this information into a meaningful guidance tool for a diverse range of users. Casual road trippers often struggle to plan efficient/affordable trips due to overly technical datasets on road quality, traffic, and travel costs. <br><br>
Meanwhile, national officials tasked with promoting tourism and improving infrastructure lack accessible tools to benchmark their country’s performance, predict tourism trends, or assess the effectiveness of public investment in transportation. Academic researchers face yet another barrier: while they need historical and comparative data for modeling and publication, much of the available information is fragmented or lacks interoperability.


## User Personas

### European Traveler (Jacques Bon-voyage)

![Image of European Traveler](traveler.jpg)

**ROLE**: Casual tourist seeking a affordable and enjoyable travel experiences across Europe.
| GOALS | FRUSTRATIONS |
|---|---|
| -Ranking countries for <br> road trips based on personal <br> prioritization<br><br>-Showcase most popular <br> tourism attractions within<br> country via prioritization<br> <br>-Display predicted traffic trends<br> for country of travel. | -No interconnected way to <br> plan a trip abroad based <br> on personal preference<br><br>-No way to predict traffic time<br> in the future while planning<br><br>-Hard to get a concrete ranking <br> of popular tourist attratcions |

### “As European Traveler...
  - I want to rank countries for road trips based on my <br> personal travel preferences so that I can choose <br> destinations that match my style.
  <br>

  - I want to see the top tourist attractions prioritized <br> by popularity so that I know what’s worth visiting <br> in each country.
  <br>

  - I want a single, easy-to-use platform that helps me <br> plan my trip abroad according to what matters most <br> to me.
  <br>

  - I want future traffic estimates while planning so that <br> I don’t get surprised by unexpected delays.

<br>
<br>

### National Director of Tourism (Nina Petek)

![Image of National Director](official.jpg)

**ROLE**: Director of improving, funding and enhancing tourism throughout Slovenia
| GOALS | FRUSTRATIONS |
|---|---|
| -View trends of tourism in regards to<br> GDP spending.<br><br>-Predict future tourism interest in <br> Slovenia<br> <br>-View trends for gas prices and <br> traffic to understand tourism patterns | -Lack of clear, comparable benchmarks <br> for evaluating Slovenia’s tourism <br> performance against other EU countries<br><br>-Limited ability to anticipate <br> sudden changes in gas prices or <br> traffic disruptions that affect <br> tourist flow<br><br>-No interconnected way to view all these<br> benchmarks and data |

### “National Director of Tourism…
  - I want to see how tourism trends relate to GDP spending <br> for E.U. countries so that I can evaluate the impact of investments.
  <br>

  - I want to predict future tourism interest in Slovenia <br> so that I can plan funding and marketing efforts effectively.
  <br>

  - I want to monitor gas prices and traffic trends to <br> understand how they affect travel patterns and visitor numbers.
  <br>

  - I want a single platform that integrates all relevant <br> data and benchmarks so that I can make informed decisions quickly.

  <br>
  <br>


### European Tourism Researcher (Ellie Willems)

![Image of European Tourism Researcher](researcher.jpg)

**ROLE:** A graduate reseacher at KU Leuven that aims to study trends regarding tourism in the E.U.
| GOALS | FRUSTRATIONS |
|---|---|
| -View trends based on her research (can <br> select a variety of indicators and <br> time periods to customize the analysis)."<br><br>-Download data/ trends for reports or <br> papers<br> <br>-Saving notes and research within the app <br> which automatically generates tags to <br> organize her work for easy retrieval<br> and simplicity.  | -Limited flexibility in selecting <br> specific indicators or time periods <br> for nuanced analysis<br><br><br>-Difficulty ensuring downloaded <br> data is in a format compatible <br> with academic tools<br><br>-Risk of losing notes or saved <br> research due to lack of reliable <br> syncing or backup. |

### “As a European Tourism Researcher...
  - I want to customize my analysis by selecting specific indicators <br> and time ranges so that my research reflects my goals
  <br>

  - I want to download datasets and visualizations in academic <br> friendly formats so that I can easily include them in reports and papers
  <br>

  - I want to save my notes and research within the app so that <br> everything stays organized and easily accessible.
  <br>

  - I want the app to automatically tag and categorize my saved <br> work so that I can quickly find related projects and avoid redundancy.

  <br>
  <br>


## Candidate Data Sources

### Fuel price levels, US Dollars per litre (via data360.worldbank)

![Image of raw api for fuel data 1](fuel_price.png)
![Image of raw api for fuel data 2](fuel_price1.png)

**Obeservations:** 81 <br>
**Numerical Features:** 2 <br>
**Categorical Features:** 2 

### Utility of this data regarding the user personas.
- Knowing the fuel cost per liter in each country helps a casual road tripper weigh whether they value saving money on travel or reaching their destination more quickly. The model can generate an ranking of the most
relevant countries based on the users informed decsion.

- Fuel prices affect how easily tourists can travel. By tracking these trends, a national tourism director can better understand when and why visitor numbers go up or down.

- Fuel price data helps a European Tourism Researcher study how changes in travel costs impact tourism trends across countries over time. This gives her insights into economic and behavioral patterns in European tourism and gives her another aspect of study regarding tourism.

<br> 

### Road Congestion (via EuroStat)

![Image of raw api for passenger data 1](passenger-data1.png)
![Image of raw api for passenger data 2](passenger-data2.png)

**Obeservations:** 6765 <br>
**Numerical Features:** 1 <br>
**Categorical Features:** 4

### Utility of this data regarding the user personas.
- Knowing the road congestion for a European Traveler will allow the user to make an informed decison on what they value more, saving money or saving time.

- Knowing the road congestion for a National Director of Tourism will allow the user to understand why certain countries have higher tourism numbers and how traffic conditions may impact the overall travel experience, helping guide infrastructure improvements and promotional efforts

- Knowing the road congestion for a European Tourism Researcher will allow the user to analyze how transportation factors influence tourism patterns and to identify correlations between infrastructure strain and visitor behavior across countries. She can then use this data by downloading it
or writing about it in the app
<br> 

### Trips By Duration (via EuroStat)

![Image of trips by durations 1](tripsbyduration.png)
![Image of trips by durations 2](tripsbyduration2.png)

**Obeservations:** 1046 <br>
**Numerical Features:** 1 <br>
**Categorical Features:** 4

### Utility of this data regarding the user personas.
- If a Casual European Traveler was to have access to this data
they could use it to help casual travelers plan their own trip length  whether to match popular itineraries.

- Knowing the trips by duration for a national offical would enable the user to view how long tourists are staying in the country and how a higher investment from GDP could increase the duration of their stay.

- Trip duration data helps a European researcher analyze traveler behavior and compare how long visitors typically stay in countries over time offering insights into economic impact and travel trends that she can write about on the app.
<br>