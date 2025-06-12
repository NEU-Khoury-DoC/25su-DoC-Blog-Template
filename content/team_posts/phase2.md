---
title: "Project - Phase II"
date: 2025-05-27
draft: false
description: "Our Idea"
slug: "phase2post"
tags: ["project", "Setup"]
authors:
    - "alpberrak"
    - "elianne_mejia"
    - "JessicaPoblete"
    - "mahika_modi"
showAuthorsBadges: true
---

# Project Updates
As a result of the feedback we received, we made several changes to the refugee, Mohammed, and lawyer, Mark, user personas. 
## [Mohammed](https://droidbait66.github.io/Team10/team_posts/phase1post/#mohammed-is-a-17-year-old-boy-from-syria-he-is-a-practicing-muslim-his-parents-were-recently-killed-due-to-bombings-in-his-area-and-he-is-seeking-asylum-with-his-5-year-old-sister-and-10-year-old-brother)
* Three of our user stories utilized the same application feature, so, we condensed these user stories into one. Rather than three separate pages 
for country ranking, asylum acceptance probability, and aslyum application demographic statistics, these will all be shown on one page which illustrates all of these data. 
* We added two new stories which will allow our users to view data regarding religous cliamte and demographics and also information about education systems/ rankings. 

## [Mark](https://droidbait66.github.io/Team10/team_posts/phase1post/#mark-is-a-german-lawyer-seeking-pro-bono-opportunities-he-wants-to-provide-legal-aid-for-refugees)
* Our user stories reffered to four separate lawyers as opposed to one persona utilizing four separate features. We fixed the stories so that they all refer to one lawyer
persona, Mark. 
* Our user stories were also very vague and failed to outline specific features that Mark would use to help with finding pro bono work opportunities.
    * We included a feature that allows users to historical trends of asylum rejection rates by country and citizenship, total received applications per country, asylum decision types, and acceptance rate per applicant demographic group (ie. age, sex, country origin).

# Application Data Model
> You can click onto the embedded window to zoom in and interact with the ER Diagram
## Global ER Diagram
<div style="width: 640px; height: 480px; margin: 10px; position: relative;"><iframe allowfullscreen frameborder="0" style="width:640px; height:480px" src="https://lucid.app/documents/embedded/00122d2e-26cf-4b2d-b323-85e488f38ce4" id="F_ejIwe8t0XN"></iframe></div>
> This is our Global Entity Relationship Diagram. We have combined all three of the following ERDs to demonstrate how every entity and user connects to one another.

## Localized Persona ER Diagrams
### Mohammed
<div style="width: 640px; height: 480px; margin: 10px; position: relative;"><iframe allowfullscreen frameborder="0" style="width:640px; height:480px" src="https://lucid.app/documents/embedded/bdcc45e0-9301-4c3e-a8f4-fc0492508b8c" id="t.ejCRtsS0Nl"></iframe></div>
> This is the ERD for our Asylum Seeker user persona. It includes a user's country, religion, education level, and application decision.

### Eric
<div style="width: 640px; height: 480px; margin: 10px; position: relative;"><iframe allowfullscreen frameborder="0" style="width:640px; height:480px" src="https://lucid.app/documents/embedded/4b2cc4d6-3c1a-4f4b-9b3c-cf97f70a00b9" id="6hfjvwmu4BLg"></iframe></div>
> This is the ERD for our EU diplomat user persona. It includes a diplomat, an asylum seeker, and the amount of money/aid directed towards helping refugees.

### Mark
<div style="width: 640px; height: 480px; margin: 10px; position: relative;"><iframe allowfullscreen frameborder="0" style="width:640px; height:480px" src="https://lucid.app/documents/embedded/84f22a6b-54ea-4171-afe9-62ad01adfd8d" id="Ygfj1ZcDe-SY"></iframe></div>
> This is the ERD for our Lawyer user persona. It includes a lawyer, an asylum seeker, and the pro bono opportunities that are available.


## Application DDL 
["Click_Here"](https://raw.githubusercontent.com/eliannemejia/OpenPort/refs/heads/main/database-files/openport_db.sql)

# Wireframe Drafts

## Home Screen
["homeScreen"](https://github.com/DroidBait66/Team10/blob/main/assets/homeScreen.pdf)


## Refugee Persona
["refugee_screens"](https://github.com/DroidBait66/Team10/blob/main/assets/refugeeScreens.pdf)

## Lawyer Persona
["lawyer_screens"](https://github.com/DroidBait66/Team10/blob/main/assets/LawyerScreens.pdf)

## Diplomat Persona
["diplomat_screens"](https://github.com/DroidBait66/Team10/blob/main/assets/diplomatScrens.pdf)


# Datasets

## Dataset: Social Spending Dataset EDA 

* The Social Spending Dataset contains the percentage of their GDP that certain countries contribute to their Social Programs. The dataset contains data from 2011-2022. Right off the bat, we noticed that there were upwards spikes during the pandemic in 2020 which seemed to have mostly leveled off in the following years. Prior to the pandemic, we noticed that it mostly differed from country to country with peaks in certain years and decreases in others. The summary statisitcs displayed that the mean spending was 23.47% with a standard deviation of 5.79. The highest spending country was France and the lowest was Slovakia. We noticed something particulary interesting in the graph that contained Norway due to it's steady fall in spending post the pandemic. 

![Social Spending Line Plot 1](/social_spending_1.png)
![Social Spending Line Plot 2](/social_spending_2.png)

## Dataset: Asylum Data

![EDA](/EDA.png)
According to the data from this API the relation between age and decision differ greatly depending on the age group. Those who apply when they are less than 14 have a slightly higher chance of being rejected based on count, with rejection being favored by 51%. Meanwhile for the age group of 14 to 17 years old the count for rejected and for positive decisions are almost exactly equal, with positive decisions occuring slightly more frequent on average. As the age groups increase there seems to be a trend of a higher rejection count, for example for ages 18 to 34 there are about 59% more rejected applicants than accepted, this is similar for ages 35 to 64. And finally for ages 65 and older rejection is still favored but only by around 53%. All of this combined shows that applicants are more favored if they are children or elderly, compared to middle aged.

![Histogram](/newplot.png)
According to the histogram it seems as if France accepts the most asylums but also rejects the most. This would make sense because France has a far higher population compared to some of the other countries like Malta. Since France not only has a large current population it also is a larger country by area. It would make sense that the larger countries would be able to accept more applicants, rather than the small countries. It also appears that a lot of the countries have similar positive and rejection decisions, such as Bulgaria, Finland, and Latvia. Meanwhile Sweden has significantly more acceptances versus rejections making it a good country to apply to. And Italy has significantly more rejections versus acceptances making it a worse candidate country to apply to.
