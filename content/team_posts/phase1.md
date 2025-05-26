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

# ASMG Project Introduction: Road Safety

## Project Description

Since automobiles became common in the early 1900s, automobiles have been one of the leading non-natural causes of death for humans across the developed world. Additionally, they have posed major safety and injury concerns beyond just deaths. In a world reliant on automobiles for travel, governments and independent agencies have continuously worked to make roads safer for all users, but their efforts still leave a lot of room for improvement. We are building an application to help address this problem by identifying patterns and attributes of roads across Europe that result in a larger number of accidents and fatalities. This application will consider data like car accidents, road deaths, road infrastructure spending, road quality, and road density for each country. With this information, users will be able to determine whether the roads and travel methods they plan to take are truly safe or if they should find an alternate route, and help governments determine which types of roads they should build more of to keep their citizens safe.

## Overall Problem
Fatalities in road-related instances can be mitigated by looking at the intersection of deaths with infrastructure spending, and provide meaningful information to address adjustments in monetary allocation, density and road quality correlation, and general safety for citizens of all kinds.


## User Personas

### EU Commission Official (Garret Warshaw)

**ROLE**: Senior policymaker in sustainable transport infrastructure for the European Commission.
| GOALS | FRUSTRATIONS |
|---|---|
| -Reduce road fatalities<br> and serious injuries<br><br>-Use road quality scores <br> to guide funding decisions<br><br>-Promote equitable <br> infrastructure investment <br> across all member states | -Political resistance <br> to redistributing funds<br><br>-Gaps in reliable and <br> comparable road data<br><br>-Funding disparities <br> between regions<br><br>-Slow implementation <br>of safety policies |

### “As an EU Commission Official…
  - I want to use road quality scores to compare member <br> states so that funding decisions are based on objective need.
  <br>

  - I want to highlight low-scoring regions in reports <br> so that I can push for more investment and reform.
  <br>

  - I want to monitor changes in national road scores <br> over time so that I can evaluate policy impact.
  <br>

  - I want to incentivize improvements in infrastructure <br> through score benchmarks so that member states stay accountable.

<br>
<br>

### European citizen (Aoife Lynch)

**ROLE**: Freelance nature photographer based in Ireland who frequently drives to remote and <br> rural areas across the EU for assignments.
| GOALS | FRUSTRATIONS |
|---|---|
| -Travel safely for work<br><br>-Use safety scores <br> to choose routes<br><br>-Avoid poor-quality <br> rural roads<br><br>-Plan shoots in <br> better-maintained regions | -No easy way to <br> compare road safety by country<br><br>-Unexpected hazards <br> on rural routes<br><br>-Low investment in <br> remote nature areas<br><br>-Inconsistent safety <br> across borders |

### “As a Nature Photographer…
  - I want to see safety scores for each country so that <br> I can choose safer destinations for my photo trips.
  <br>

  - I want to avoid countries or regions with low scores <br> so that I don’t risk delays or vehicle damage.
  <br>

  - I want to use the scores to push for better rural <br> infrastructure so that all regions get fair investment.
  <br>

  - I want to plan routes through high-scoring areas  <br> so that I travel with more peace of mind.

  <br>
  <br>


### Professional Trip Planner (Marcus Ellis)

**ROLE:** Professional itinerary designer crafting custom multi-country road trips across Europe
| GOALS | FRUSTRATIONS |
|---|---|
| -Leverage country-level <br> road quality scores<br><br>-Plan routes that maximize<br> safety and comfort<br><br>-Showcase well maintained <br>scenic roads | -Lack of reliable road <br> quality insights per country<br><br>-Time-consuming cross <br> border data gathering<br><br>-Surprises from poor <br> road conditions en route |

### “As a Professional Trip Planner…
  - I want to see each country’s road quality score so that I <br> can prioritize safer nations in multi-country itineraries.
  <br>

  - I want to filter destinations by a minimum score threshold so <br> that clients only visit regions with reliable infrastructure.
  <br>

  - I want timely updates to country scores so that my plans adapt <br> to recent infrastructure improvements.
  <br>

  - I want to export score-backed route summaries so that I can <br> provide clients with transparent safety justifications.

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