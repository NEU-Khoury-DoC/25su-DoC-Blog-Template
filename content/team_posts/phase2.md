---
title: "Project - Phase II"
date: 2025-05-27
draft: false
description: "Building the foundation to our project"
slug: "phase2post"
tags: ["project", "author"]
authors:
  - "aidankelly"
  - "seanbehan"
  - "gabbymontalvo"
  - "mariasamosrivas"
showAuthorsBadges: false
---

# Updates to Phase One
Through the duration of Phase two our team realized that with our initial design, users would all be using the app in a very similar way that made each persona seem irrelevant to how they were interacting with the data. Understanding this, we decided to pivot our idea to surround European tourism. Specifically we were focusing on creating an data driven european tourism app in which each user would interact with the app uniquely. With this new app, we had to also rethink our personas as how they would interact with this new app was different than our old personas. These new personas are similar to the other ones but their goals and wants that the app must satisfy differs to the older personas. 

## New User Personas

### European Traveler (Jacques Bon-voyage)
### National Director of Tourism (Nina Petek)
### European Tourism Researcher (Ellie Willems)

## Updates to Datasets
Since our focus for the project went from road deaths/road saftey to developing a data driven driven european tourism platform, the data also needed to change. In light of this, our group found a variety of new data for road congestion (number of cars on road), road spending by GDP, average fuel price, and tourism participation. These new data sets allow us to develop the tourism driven app around the 3 personas while also being unique to the 3 of them. 

These changes can be viewed in more detail in the phase one deliverable <br>

# Phase II Deliverable
The main focus of this phase of the project was to thoughtfully explore potential features that could be implemented in the app, based on the cleaned data and the data models developed by our group.

## Wireframing of EuroTour
Our team created wireframes to visualize what we envisioned the app would look like by the end of the development process, based on the available data and the features required to meet user needs and project requirements. Each wireframe page is a page that would be displayed on the app with the user interface displayed

1. Home Page
- ![Home Page of Wireframe](HomePage.JPG)
<br>
This is the base page where all users will see when the application is first opened up. This is the default page and the login screen

2. European Traveler Page 1
- ![First Page of Traveler Wireframe](TravelerPage1.JPG)
This is the first feature the user can encounter when signed in as the European Traveler. On this page, users can input their personal preferences such as prioritizing saving money, reducing travel time, or visiting popular destinations and receive a ranked list of countries based on those values

3. European Traveler Page 2
- ![Second Page of Traveler Wireframe](TravelerPage2.JPG)
This is the third feature the user can encounter when signed in as the European Traveler. On this page, the user can input the country they are visiting, the start and end date of their trip, and their prefered travel time (day/evening/night) and recieve a traffic prediction (time estimation).

4. National Director of Tourism Page 1
- ![First Page of Director Wireframe](DirectorPage1.JPG)
This is the first feature the user can encounter when signed in as the National Director of Tourism. On this page, the user can select a country, input a start and end date and recieve a double-lined trend chart of tourist numbers and GDP spending in correlation with the years range

5. National Director of Tourism Page 2
- ![Second Page of Director Wireframe](DirectorPage2.JPG)
This is the second feature the user can encounter when signed in as the National Director of Tourism. On this page, the user can select from a multi-select box—choosing factors such as fuel prices, traffic levels, or road density. They must also specify a year and set the desired increase or decrease in GDP spending. This input will generate an interactive heat map that visualizes the projected impact of these changes on the country level by color.

6. European Tourism Researcher Page 1
- ![First Page of Researcher Wireframe](ResearcherPage1.JPG)
This is the first feature the user can encounter when signed in as the European European Tourism Researcher. On this page, the user can select which data they would like to download from the various data sets used on the websites. They can choose if they want all the data, the date range of the data, the country(s) of the data and then can download the data.

7. European Tourism Researcher Page 2
- ![Second Page of Researcher Wireframe](ResearcherPage2.JPG)
This is the second feature the user can encounter when signed in as the European European Tourism Researcher. On this page, the user can write notes about the research they are able to conduct on they app and also upload pictures to their note page. The note page will be given an auto generated tag at the top for filtering purposes.

<br>

## Global and Persona ER Models
<div style="width: 640px; height: 480px; margin: 10px; position: relative;"><iframe allowfullscreen frameborder="0" style="width:640px; height:480px" src="https://lucid.app/documents/embedded/b232c25c-6c0f-44d9-99cc-d8ebb671822c" id="rFzj1BL4b9vs"></iframe></div>
Use the cusor to zoom in/out or use the plus and minus sign (in order to see all the models). For clearity, the researcher is the same as the Global data model as the researcher can view all the data for a variety of her studies 
<br>

## Inital MySQL DDL Model
![mySQL DDL inital code](mySQLDDL.png)
Here is the link the to code of the Inital MySQL DDL model <br> [Link to mySQL DDL Code ](https://drive.google.com/file/d/1dUJhlQq0w4GWwUo47a5TZEtMl-E3PAmh/view?usp=sharing)


## Passenger Cars Present in Europe Over Time - Data Visualizations
![passengercarsscatter](passenger_cars.png)
Explanation of Choices:
- The Passenger Cars data file provides extremely in-depth features, like type of motor engery and size of engine.
- By taking advantage of the ability to include all motor energies and engine sizes into a category called "Total", this allows for a more holistic analysis of these features and how they interact with time.
- The most prominent and obvious factor to observe in this care would be how the number of passenger cars increases with time.
- By choosing to implement an interactive scatter plot where number of cars varies by size, it is easy to see how the number of cars has steadily increased across time.
- Observing this trend is not only important for supporting our inferences, but important with regards to coinciding with our user personas' goals.
- For example, our Researcher would greatly care about the interaction with these two features because it would support their inference that motor car usage has overall increased, which has further implications on road quality and fuel prices. This would lead our Research to interact with other aspects of our application, like turning towards data models about road quality, road density, and fuel prices.
- Our National Official would be interested in this kind of analysis in order to capitalize on this increased volume of cars and prospective tourism over time, supporting their goal of using this application to better the economy.


![passengercarsbar](passenger_cars_bar.png)
Explanation of Choices:
- Our second visualization about the passenger cars dataset also demonstrates changes in the two features that would be most prominent- Years and Number of cars.
- However, as a difference from the first one, the usage of bar charts dramaticizes the deviations from the baseline thanks to observing height.
- Again, with consideration for our user personas, our Road Tripper/Traveler might benefit more from this kind of vizualization.
- While the scatterplot might require a more detailed eye to pick up on what the sizes of each dot mean, what causes it to vary, and a stronger critical thinking process about how the two features interact, a simple bar chart can be easier to the untrained eye.
- A more casual persona such as our Road Tripper would be more inclined to observe a visualization like this where the differences and interaction is easier to observe.