---
title: "Project - Phase III"
date: 2025-06-05
draft: false
description: "Building functionality into our Project"
slug: "phase3post"
tags: ["project", "author"]
authors:
  - "aidankelly"
  - "seanbehan"
  - "gabbymontalvo"
  - "mariasamosrivas"
showAuthorsBadges: false
---

# Updates to Phase Two
While working through phase three, our group continued to develop how our user personas would interact with the app. We futher developed the researcher, who now will have a page to make research posts, a page to view the posts and a page to view trends between road saftey and tourism variables. These tourism variables includes passenger car data road quality and road density all on the country level. We also changed the ER relationship to limmit the scope of the reasearcher, include road death data and to merge all the new diagrams to the global ER diagram. This change also implies that we modified the mySQL database by adding new a new table for the RoadDeaths, for the Reseacher and the ResearchFindings. 

## Updating Maps
Updated visualizations from the number of passenger cars file and made visualizations for the number of trips per country data file. 

All these changes can be viewed on the phase two deliverable

 <br>

# Phase III Deliverable
The main focus of this phase of the project was implement the functionality via creating the API requests and creating the ML models. 

## Features Used in ML Models
Dicuss the features used in the ML and a reasoning as to why those features were selected. Also discuss any major/surprising issues found during ML model exploration

## Streamlit App Functionality

1. POST Request for Researcher
When the user is signed in as the researcher and is on the create posts page, they have the ability to create a post with a title and body text. When the user presses submit, a streamlit form will send the data as JSON through the POST request that is embeded in the submit button. This POST request will add the text and the post content to the mySQL database and will store it for the user to view on the view posts page

2. GET Request for Researcher
When the user is signed in as the researcher and is on the view posts page, a GET request will be made to the mySQL database to retreive all the posts in the post ResearchFindings table and display it to the user. The user is able to see all the attributes of the post as it is stored in the database like time, title, content, post id, but not the author id only the author name for security purposes.

3. PUT Request for Researcher
When the user is signed in as the researcher and is on the view posts page, if they are on a post they have made, they can edit the existing post on the streamlit website. This will prompt the user to make the changes in a streamlit form and when they submit, will send a PUT request in order to edit the existing post in the database. This will then update the post in real time.

4. DELETE Request for Researcher
When the user is signed in as the researcher and is on the view posts page, if they are on a post they have made, they can delete the existing post on the website. This will send a DELETE request to the API and will then delete the specific row in the mySQL database under the ResearchFindings table. The user is unable to recover the posts after they are deleted so we should make sure the user knows this.

5. GET Request for Traveler
When the user is signed in as the traveler and is on the where to travel page, they are able to input their desired level values for travel time, cost, and tourism population. Since this is wrapped in a Streamlit Form, when the user submits, the values from the sliderbar are placed into the GET request to the API and those values from the request are used as the values to generate a ranking (from the recommendation ML model) of the top 5 countries that match the users input. The recommendation ML model rankings are then used to highlight on a map the top 5 countries.

6. Another GET Request for Traveler 
When then is signed in as the traveler and is on the view travel data page, a GET request to the API will get the data from the mySQL table that is relevent to the country they are traveling in (via a dropdown selection) and it will display the data.

7. GET Request for Tourism Director
This endpoint uses time series modeling to forecast future tourism trends and visitor numbers. The predictions help tourism officials make strategic planning decisions and allocate resources effectively.


## REST API Matrix
![API Matrix Chart](Matrix.png)


