---
title: "Phase 4 Individual Deliverable"
date: 2025-06-13
draft: false
description: "The individual blog post for phase 4 of what I contributed"
slug: "sophiephase4"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "sophiefarrell"
showAuthorsBadges : false
---
# Project Phase 4

## Updates to Mock Data
The first thing I did in this phase of the project was create (or recreate) the mock data we needed. After the feedback from Phase 3, we changed a lot of the attributes of our mock data and even added a new entity, DaycareData, which could be used for analysis of DaycareLocations. Because of this, the mock data for DaycareLocations needed to change as some of its attributes were moved to DaycareData. I also added an inactive feature to DaycareLocations for deletion. Additionally, I added descriptions and cities to the entities Policies and AffinityResources since those would add mmore detail for our users to look at. Finally I created the mock data for Users since Phase 4 introduced the need to have multiple users of the same role. Because of these changes to the mock data, I needed to update our database to fit the data. This included changing the attributes of some entites, creating the DaycareData entity, and deleting the DeletedDaycareLocations entity since it was no longer needed. 


I also needed to update the existing routes we had to fit our data. The route for deleting a DaycareLocation changed to marking that location as inactive, for example. This included deleting unecessary routes, such as the put route for DaycareLocations since the attributes it would have updated no longer existed in that entity. While updating the existing routes, I also created new routes for the mock data. The DaycareData entity got multiple get routes and a put route. I also created a route that would get all the information in DaycareLocations and the corresponding information in DaycareData so you could see all of the information together. These are just a few examples of the updated routes in our project. 


## Pages

### Legislation Finder Page
The first page I started working on was the Legislation Finder Page. Previously, it only included the visualization of birth rate over time, not the actual legislation part of it. Now that our mock data was completed, I could work on implementing this. The first thing I did was create the implementation of the get route I already had to show all of the legislation there was in expander boxes. This worked very nicely and was quite easy since I had done it before. Next, I wanted to be able to filter the data by country using the same country multiselect that the visualization was using. This was difficult because the multiselect listed the country name, not the country code, so I had to reverse the map that John had made to make it work. My next issue was the multiselect part, since the route I had would only filter by one country, not multiple. I ended up creating a new route that would filter by multiple countries at the same time and implemented that instead. Then I created the filters for year and focus area, which was much easier, and implemented those. 

### Politician Research Page
I also created the Politician Research page. First, I implemented the visualization that was made by Mia that showed the difference in weekly working hours in a country based on sex. Then I created a dataframe that would show the different benefit expenditures a country had in a given year. Finally, I created my own visualization of the CPI of a country over time. I then decided to split these visualizations into tabs for ease of viewing. I also added a link to the sidebar for this page. 

### Daycare Profile Page and Business Planner Page
After that, I created the Daycare Profile Page, which would give more detailed information about a DaycareLocation using attributes from DaycareData. This is when I created the route that would get information from both entities. I updated the page so it would have a select box for year so it would only show the DaycareData of one year at a time. Additionally, I added the option to update details of the data (such as opening time, monthly budget, etc.) for the current year and the option to delete a location. 

Creating the page and it's formatting was simple and easy, however I ran into issues when it came to switching to this page from the Business Planner page. The locations were listed inside an expander, and the button within the expander on that page. When the button was clicked, it would not work. I asked Dr. Fontenot for help finding the issue and eventually he showed me how to use the streamlit session state to get the page to switch. This, however, meant that the daycare locations were always displayed on the page instead of displaying when a button when pressed. I updated the UI so it looked nicer and decided that was fine. Additionally on the Business Planner page I updated the locations shown so it would only show the current user's locations instead of all locations. 

### Add Location Page
I updated this page so that it would only ask for the name, city, and country of a location instead of the attributes that are now in DaycareData. This made the page much simpler, so in the future maybe more could be added to it. Additionally, I made the current user the owner of the daycare, while the previous version of the page did not assign an owner to the location. I also updated the database for this page so that the default value of inactive for a DaycareLocation is false. 

### Daycare Research Page
Additionally, I created the Daycare Research page, which displayed visualizations created by the DS team of enrollment over time of daycares in a particular country and staff vs enrollment of different daycares in the current year using the mock data created for these locations. The most difficult part of this page was making it visually appealing, so I added a brief description of what the page is for to the top and a description of what each visualization is next to each plot. The page also has a select box for country so the user can change which country they want to see information about. 


### Affinity Resources Page
Next I started work on the Resources page for our parent persona. At the time, it would display the data but the filtering system did not work. It was a simple fix since the root of the issue was the fact that the names of the attributes of the entity was put in wrong both on the page and in the route. Once this was updated, the filters worked perfectly. 

### Daycare Finder Page and Parent Daycare Profile Page
I also worked on the Daycare Finder page. Prevously, it would show all daycare locations in a code format and the options for filtering did not work. I updated the formatting for the displayed locations and connected the input boxes to the get route so they would actually do something. When looking at the daycare locations in the first tab, you can also select a button to view the daycare's profile page. This will take the user to the Parent Daycare Profile page, which is similar to the daycare owner's Daycare Profile page only it has less information and is unable to update or delete a location. 

Additionally, I decided to add a compare locations feature so I split the page into tabs, with one tab displaying all of the locations and the other comparing two. I made a filter for country that would populate the first and second location select boxes so they would only include daycares in that country. Additionally, I made the second daycare location select box unable to select the daycare that was selected in the first box. Then I displayed the information in two side by side containers. 

## Model 1 Birth Rate Predictor
After getting feedback in Phase 3, we updated our first ML Model (a linear regression model that predicts birth rate) to factor in year. That was done by Emma, who then gave me the weights and asked me to update the model. I get rid of the original weights that were inserted into the Model1Weights entity and insert the new weights. Then I update the Birth Rate Predictor page so it no longer uses cash benefits per capita since that no longer has a weight. I show the page to Emma afterwards because the numbers it is outputting are strange, and we work together to try to fix the issue. At first we think it is because the page originally did not account for the squared values of the inputs, so we add those in. Then we try standardizing the data, which still doesn't help. Eventually, Emma decides to work on it on her own because she has more technical knowledge of the model and she fixes the issue. 

## Presentation
Finally, our group as a whole worked on the presentation. I created a new database schema since our old one no longer aligned with our database. Together, we assigned pages for each group member to talk about in our app demo. We also practiced presenting numerous times until we each felt confident in what we would say and the timing of our presentation. 