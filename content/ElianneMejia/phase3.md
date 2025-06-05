---
title: "Phase 3 Deliverable"
date: 2025-06-06
draft: false
description: "Individual Deliverable"
slug: "blog3"
tags: ["authors", "config", "docs"]
authors:
  - "elianne_mejia"
showAuthorsBadges: false
---

I took the lead on writing the routes and front implementation associated with the refugee persona. 

### API Routes

- **`GET /refugees/application_stats`**  
  Retrieves the top three countries based on average acceptance rate for the provided `age`, `sex`, `citizen`, and `geo` values. Allows refugees to find accurate information about which countries are accepting the most asylum seekers.

- **`POST /refugees/new_user`**  
  Creates a new user. The body of the request must include: `FirstName`, `LastName`, `UserRole`, and `Email`.

- **`POST /refugees/new_user/<int:uid>`**  
  Creates a new AsylumSeeker entry for the specified `uid`. The request body must include: `DOB`, `Sex`, `CurrentLocation`, and `Country of Origin`.

- **`GET /refugees/legal_aid_application/<uid>`**  
  Creates a new LegalAidApplication for the given `uid`. The request body must include a description of the legal aid being requested. This allows refugees to find a lawyer to help them gain legal residence.

- **`GET /refugees/users`**  
  Retrieves all users currently stored in the database.

- **`GET /refugees/asylum_seekers`**  
  Retrieves all AsylumSeekers currently stored in the database.

- **`POST /refugees/legal_aid_application/family/<int:fid>`**  
  Creates a FamilyMember entry for the AsylumSeeker with ID `fid`. The request body must include: `DOB`, `Sex`, `FirstName`, and `LastName`.

- **`GET /refugees/legal_aid_applications`**  
  Retrieves all legal aid applications currently stored in the database.

- **`GET /refugees/weights`**  
  Retrieves the weight vector for the logistic regression model.

- **`GET /refugees/final_prediction/<age>/<sex>/<citizen>/<geo>`**  
  Retrieves the predicted probability for a user with the given `age`, `sex`, and country of origin (`citizen`) to be accepted for asylum in the given country (`geo`). This is computed by the logistic regression ML model.  
  _Note: This is the route that calls the ML model._

---

### Front-End Implementation

#### Acceptance Probability Screen

![AcceptanceProbScreen](/acceptance_prob_screen.png)  
This screen uses the route that calls the logistic regression model. Refugees can see their predicted acceptance probability for their top three countries.

#### Legal Aid Application Screen

![LegalAidApplication](/legal_aid_app_screen.png)  
This screen allows refugees to apply for legal aid. Their application is added to our database and will be viewable by lawyers on their future dashboard (to be implemented).
