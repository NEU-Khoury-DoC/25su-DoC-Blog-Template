---
title: "Anoushka Blog 4"
date: 2025-06-12
draft: false
description: "A Description of the Phase 4 deliverable"
slug: "anoushkablog4"   # if you use, needs to be different for every post
tags: ["authors", "config", "docs"]
authors:
  - "anoushkaabroal"
showAuthorsBadges : false
---

This phase of the project was all about getting our platform ready to be presented to a larger group. I had a hand in fully implementing the cosine similarity model onto the Customize_Move page, where the relocating resident can find country healthcare systems that are similar to their chosen country. The cosine similarity is calculated by taking the weights, and doing the Hadamard product between the weights and the chosen countries vector. Then, the result is compared/calculated with the hadamard product between the weights and every other country, to eventually get a full list of similarity scores in relation to the chosen country. I created a bar chart as well as a gradient map using Plotly express to allow the user to visualize these similarity scores in a more digestible and geographical manner. I also made sure to implement the route that gets the cosine similarity raw data from the database, and allows that information to be translated to the front-end user interface. This same model and route was also used to display information in the sidebar of the country profile page.

During this phase, I also spent some time learning about how to implement an autoregressive model, and worked with Arthur to transfer the model out of a jupyter notebook to a python script. I learned about how to create the X matrix with data from the Y matrix, and how to make the predictions with these new weights. I helped with making sure that the route to get all of the future predictions was up and running. In speaking with my other team members Shiven and Kat, I now have gained a better understanding of the database side of this project, and I have shared the knowledge that I have gained from creating these machine learning models.  

In terms of my time in Belgium, I am super grateful to have had this experience. I have gained so much from the speakers, and will take those perspectives on sustainable living, circular economies, and more into my life in the future. I have made so many great connections with my peers that I will cherish forever, and I can’t wait to keep in touch with them when we get back to the Boston campus. I am also extremely appreciative of my professors Dr. Gerber and Dr. Fontenot, as well as program assistant Sydney Schulz, for their guidance throughout this dialogue of civilizations program. I hope that one day I will visit Belgium again, but until then, I will bring my experiences back to Northeastern, and continue to learn and grow. 
 


![image](BrusselsFinal.png)



