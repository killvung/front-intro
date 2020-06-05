# Project-Front
Front is the system I came up to capture all fitness data across multiple resoucres. FRONT is the abbreviation of 
- Fitness
- Recap
- Offer
- Novel
- Telling

## Motivation:
I use multiple apps to track down my fitnesss activities, such as biking, running, walking, you name it! Often I found it difficult to switch between different application in order to analyze my data for purposes, for example, trackdown statistics like weekly total miles, has paces for running been improved, plot all routes on the map etc. Given my education background and working experience. It is possible for me to implement a system to centralize all the data and further experiment with them.

## V1
Influenced by the hacker culture back in college, I wrote a POC instantly to display all my walking routes in Austin great area and display the top 5 longest walking routes. killvung.github.io/nuxt-front
Components:
Client
- Vue front with Nuxt (nuxt-front)
- OpenLayer
Services
- Python Backend with Flask boilerplate (front-api) for all fitness data (routes, distances)
- Apollo GraphQL Server (apollo-server) as a middleman to direct data
Database:
- Mongo Atlas to quickly stored raw data captured from datasource

To build a SPA with semi-complicated UI, Nuxt and Vue would be a great chose compare to Rxxxx. OpenLayer is also used for displaying the map with all plotted routes. Realizing there would be a lot of complex data coming in from backend, I use Apollo GraphQL to dynamically fetch the data I needed, so I don't have to manually pick and choose through REST APIs. I used Python for my backend services so in the future I may be able to experiment the data with science ;-) 

## Retrospect
#### Too many hops
- Turn out there are too many hops (even for 2) between client and backend, and it's quite unnecessary. The Apollo GraphQL Server itself is sufficiently enough to read and translate data rather than let python backend services handling it. Indeed, I pythoh backend services for future analysis can be isolated with its own. 
#### Frontend will be complicated
- The current implementation for the frontend will not handle big and complicated logics (Dashboard, SideBar, Widgest...).

## V2
(On going)
