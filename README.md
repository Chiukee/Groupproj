Original App Design Project - README Template
===

# Covid-19 Stats app

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
The primary function of this app is to collect and display COVID-19 statistics of a given or praticular area. Areas include locations such as city and/or state. 
Area is also limited to locations within the 50 United States. 

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:** Health and Wellness
- **Mobile:** Phone, tablet
- **Story:** User check app to view statistics of COVID-19 infection rates in their area, as well as general information aobut COVID-19, symptoms, and hospitals/testing centers
- **Market:** 18-99, android, apple
- **Habit:** Frequent(at least once a week)
- **Scope:** Select cities within the United States

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User must be able to register(must choose between an organization or an individual)

* User must be able to log-in

* User must be given an option to change or retreive password

* User must be able to view COVID-19 statistics for their current location/address

* User must be able to put in an address, with zip code

* User must be able to scroll options icon screen

* User must be able to view and edit their data

An individual user:

*Must be able to find nearest testing center or hospital relative to the address they put in

*Must be able to fill out symptom checklist.
 -Depending on results of symptom checklist, user must be given a list of locations ordered by distance from nearest to farthest(between 0-10 miles) 
  of COVID-19 testing locations and hospitals.


An organization user:

*Must be able to display: 
Organization Name
Location
Mainline Phone number
Update the above information through an update button

**Optional Nice-to-have Stories**

* Individual user must be able to view additional information regarding COVID-19, including:
-prevention
-symptoms
-what to do if experiencing symptoms


### 2. Screen Archetypes

* Login 
  * User must be able to log-in
  * User must be given an option to change or retreive password
* Register - User signs up for an account  account
   * User must be able to register(must choose between an organization or an individual)
    
   
* Option Screen - User can see a list of icons here: Statistics, Symptoms checklist, COVID-19 info, User information
  * User must be able to scroll options icon screen
  
* Statistics screen
  * User must be able to view COVID-19 statistics for their current location/address
 
* User information Screen
  * User must be able to view and edit their data
  
* Symptoms checklist screen
    * Must be able to fill out symptom checklist.
    * Depending on results of symptom checklist, user must be given a list of locations ordered by distance from nearest to farthest(between 0-10 miles) of COVID-19 testing locations and hospitals.

* COVID-19 info screen
  * Individual user must be able to view additional information regarding COVID-19, including:
  -prevention
  -symptoms
  -what to do if experiencing symptoms
 

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Options Screen
* Symptoms checklist
* Statistics

**Flow Navigation** (Screen to Screen)

* Login 
  * Options screen
  
* Register - User signs up for an account  account
  * Options Screen
  
* Option Screen - User can see a list of icons here: Statistics, Symptoms checklist, COVID-19 info, User information
  * Statistics
  * Symptoms checklist
  * Covid-19 info 
  * User information
 
* Statistics screen
  * Statistics information screen
  * Options
 
* User information Screen
  * User settings
  * Options
 
* Symptoms checklist screen
  * Checklist quiz
  * Options
    
* COVID-19 info screen
  * Information screen
  * Options
 
## Wireframes
Picture of hand sketched wireframes: https://imgur.com/a/ShyPNtv

Wireframe interactive prototype: https://www.figma.com/file/d2voIoCu9fT6CyRbGnfYMj/Untitled?node-id=0%3A1

<img src="wireframe.gif" width=600>

### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 

### Models
## Schema 
### Models
patch-3
   #### Organization User
=======
[Add table of models]
#### Organization

 main
   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | Location      | String   | Location of Covid Testing Center |
   | author        | Pointer to User| image author |
   | image         | File     | image of location that user posts |
   | Description   | String   | Description of testing center and instructions |
   | Rating        | Number   | Rating of location |
   | Hours         | Datetime | Hours of operation |
   
 patch-3
   ####  Patient User
   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | Username      | String   | Username of User |
   | HasTravled    | Boolean  | True or False if User has traveled|
   | TraDescription| String   | if HasTravelled Description of travles |
   | Gender        | String   | Gender of User|
   | Image         | File     | Image of User |
   #### Book Appointment
   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | NameField    | String    | Takes first name and last name in textbox|
   | IfClicked    | Boolean  | True or False if User clicks bookAppointment|
   | TimeScroll   | Pointer to timelist  | Select time for appointment |
   
   
=======
 main
### Networking

#### List of network requests by screen

-  Statistics Screen
      - (Read/GET) Query logged in  list of nearest locations
      - (Create) Appointment for location
      - (Delete) Appointment
      -(Read/Get) New Local Facts in top of screen
      
      
-  User Profile Screen
      - (Read/GET) Query logged in user object
      - (Update/PUT) Update user profile image
      
-  Organization Profile Screen
      - (Read/GET) Query logged in user object
      - (Update/PUT) Update user profile image
      - (Update/PUT) Update Hours of Operation
      - (Update/PUT) Update Description 

-  Symptoms Screen
      - (Read/GET) List of possible symptoms with checks
      - (Update/PUT) Check Marks next to symptoms users have
