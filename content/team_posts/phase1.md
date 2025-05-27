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

### Fuel price levels, US$ /litre (via data360.worldbank)

![Image of calling API and dataframe.head()](fuel_price.png)
![Image of calling API and dataframe.head()](fuel_price1.png)

**Obeservations:** 81 <br>
**Numerical Features:** 2 <br>
**Categorical Features:** 2 

### Utility of this data regarding the user personas.
- Knowing the cost of fuels for each country, by liters, allows a casual roadtripper to <br> plan their route depending on how much the gas costs in each country. They are able to better create regulaton of different types of roads per country.

<br> 

- Knowing the deaths for each country, by road type, allows a European citizen to <br> avoid roads that may be dangerous when traveling around each country.

<br> 

- Knowing the deaths for each country, by road type, allows a Professional Trip Planner <br> to plan accordingly in favor of their clients depending on their concerns.

<br> 

### Road Quality by Country (via data360.worldbank)

![Image of calling API and dataframe.head()](RoadQual1.png)
![Image of calling API and dataframe.head()](RoadQual2.png)

**Obeservations:** 118 <br>
**Numerical Features:** 3 <br>
**Categorical Features:** 0

### Utility of this data regarding the user personas.
- Knowing the road quality by country allows a EU Commission Official to <br> advocate for policy regarding better regulaton of different types of roads per country.

<br> 

- Knowing the road quality allows a European citizen to <br> avoid countries that may have less developed roads or are of less quality in hopes to preserve their car and safety.

<br> 

- Knowing the road quality allows a Professional Trip Planner <br> to filter countries that are not ideal for travel when concerining car sustainability and saftey.
<br> 

### Transport spending by country and year (via OECD)


``` # Base URL
base_url = "https://sdmx.oecd.org/public/rest/data"

# Modifiers
agency = "OECD.ITF"
dataset = "DSD_INFRINV@DF_INFRINV"
version = "1.0"  # Assuming version 1.0, could be different
dimensions = ".A.INV.EUR.ROAD.V"

# Parameters
params = {
    "startPeriod": "1995",
    "endPeriod": "2023",
    "dimensionAtObservation": "AllDimensions",
    "format": "jsondata"
}

# Construct the URL
url = f"{base_url}/{agency},{dataset},{version}/{dimensions}"

# Make the request
response = requests.get(url, params=params).json() 
```

![Image of calling API and dataframe.head()](Transport1.jpeg)

**Obeservations:** 26 <br>
**Numerical Features:** 28 <br>
**Categorical Features:** 0

### Utility of this data regarding the user personas.
- Knowing transport spending by country and year allows a EU Commission Official to <br> understand where funding is being applied regarding transport and to make policy for better union spending.

<br> 

- Knowing transport spending by country and year allows a European citizen to <br> get a general understanding of how well maintained the roads within a country are and which countries they may want to avoid traveling in.

<br> 

- Knowing transport spending by country and year also allows a Professional Trip Planner <br> to filter countries that are not ideal for travel when concerining car sustainability and saftey.
<br>