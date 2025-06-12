---
title: KA - Blog Post IV
date: 2025-06-12
draft: false
description: "Phase IV Updates"
slug: "blog4"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "katherineahn"
showAuthorsBadges : false
---

For the Phase IV deliverable, I worked to continue to refine our web application to make it more user-friendly and realistic. This included adding mock data for the Users and CountryInfo tables: the users were assigned a ‘roleID’, a value 0-2, which indicates which user archetype they are; the CountryInfo table was filled with both general and healthcare information for each country. This mock data proved useful when it came to filtering for the user archetypes in the GET route that called for users to login, as well as creating the ‘Country Profile’ page. For logging into the app, I created a get_all_users GET route, which gets all users with optional filtering by user role, which returns a list of users that was added to dropdown login menus. I then worked on the ‘Country Profile’ page wherein a resident or student may select a country, and is given a brief overview of the country, its healthcare system. Further, our team added to the page countries with similar scores (using cosine similarity), and relevant articles to the country. To achieve this, I created and implemented the get_country GET route that takes in a three-letter country code to get all the detailed information about the country, as well as mock articles related to that country. Within the Student persona, I wrote and called the get_all_features GET route to return one dictionary of dictionaries of the six features (life expectancy, infant mortality, total health expenditure per capita, etc.). This was further used to create a dataframe on the ‘Country Comparator’ and ‘Target Values’ page to display the current scores of provided countries. Additionally within the student persona, I created an additional feature of users on the ‘Country Profile’ page to favorite an article, which can then be seen on the ‘Favorite Articles’ page. I achieved this by creating new POST, GET, and DELETE routes that work to add an article to the Favorites data table, get the articles in that table for a given user, and delete/unfavorite an article. Overall, I consistently ran through the pages to ensure changes made were effective and useful to users’ experience using the Care Compass app. 

Outside of project work, I spent one of the two free days exploring Antwerp! While the weather was less than ideal, it was still a fun experience to be walking around and shopping for souvenirs in the lovely city. While walking around, there were a multitude of interesting statues, some of which we embodied (as seen below). 

![Antwerp](KA_PhaseIV.JPG)

Additionally, I went to my first soccer game this past week! The game was Belgium vs. Wales, and ended with Belgium taking the win. It was quite the exciting match up and I feel lucky to have been able to experience the excitement and roar of the Belgian crowd.

![Soccer](KA_PhaseIV_soccer.JPG)