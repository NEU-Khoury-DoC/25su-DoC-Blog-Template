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
## Project Phase 4

1. Created mock data
2. Updated database tables to fit created data
  - inactive attribute made deletedDaycare table obsolete
  - additional attributes to some tables
  - less attributes in DaycareLocations
  - created DaycareData
3. Updated existing routes to work with changes to database
  - updated fields in existing routes
  - deleted unecessary routes
4. Created routes for mock data (daycare_data_routes)
  - daycare data put route
5. Legislation Finder page
  - created routes for it
  - implemented get route on page
  - multiselect filtering
    - created route for multiselect filtering
    - mapped country to country code so graph filter would work
  - additional filters created
6. Affinity Resources page
  - fixed filters so they work
7. Fixed tab page titles (used to say wrong thing at top. now don't)
8. Created Daycare Profile page
  - created route that would get from DaycareLocations AND DaycareData
  - created page that called route and listed out all of the data
  - ran into issue in Business Planner page when clicking button to switch to profile page (asked Fontenot to debug)
    - ended up making daycare locationo expanders always appear on page instead of appear after button is clicked to fix issue
      - guess that issue lies with st.session_state somehow, but unsure
  - updated page so that it would only show one year's data at a time using year select box
  - created update data button that is only visible for current year
    - messed with session state until it only showed up when i wanted and worked when updating attributes
      - accidentally was calling route that updated based on daycareData id, not daycare_id
  - created delete daycare button that would ask user if sure before deleting and marking this daycare as inactive then returning to planner page
9. Daycare Finder page
  - created Daycare Finder page
  - added monthly_price as a filter in route
  - created two tabs for page: one to find daycares based on filters and one to compare two daycares
    - fixed filters so they worked in first tab
    - in second tab: made filter for country that would populate first and second location select boxes with daycares in that country
      - get data for each location in a container side by side using columns
10. Add Location page
  - updated the page for new database (less things to add)
  - updated database so default for a location to not be inactive
11. Parent Affinity Resources page
  - made filter display full country name instead of just country code
  - mapped country name to country code
12. SQL database file insert updates
  - after John redid some things in the database and added own insert statements, i got rid of duplicates
13. Model 1 Birth Rate Predictor
  - given new weights for m1, so I converted the new csv to SQL insert statements and got rid of the old insert statement
  - attempted to implement model in same way as before but one value no longer existed
    - old way of implementation was wrong. need to standardize values
      - ran into issues when standardizing values. gave to Emma to finish implementing since she understood model better
14. Business Planner Page
  - updated business planner page so that it only showed that user's daycares instead of all daycares
15. Daycare Research Page
  - created page
  - implemented two mock data visualizations made by DS team
  - added title and brief description of page and what user should do
  - added descriptions in columns next to each plot
16. Politician Research pag
  - created page
  - implemented visualization of weekly working hours by sex made by DS team
  - added link to this page in sidebar
  - created dataframe for country benefit expenditures
  - created CPI over time visualization
  - organized visualizations into tabs on page
17. Parent Daycare Profile page
  - created page (version of daycare profile that shows less information and can't be edited)
18. Deleted unecessary pages and routes and tables
19. Presentation prep
  - redid database schema for presentation