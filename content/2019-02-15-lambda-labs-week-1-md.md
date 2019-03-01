---
title: Lambda Labs --- Week 1
date: 2019-02-15T06:17:18.483Z
cover: /assets/week1-appdiagram.jpg
slug: labs-week-1
category: Lambda Labs
tags:
  - week 1
---
# Part 1 - Individual Accomplishments this Week

Github Handle: [eileencuevas](https://github.com/eileencuevas)

This week, I spent a lot of time reading and diagramming things out! Because our app was already built, we, as a team, had less choices to make regarding the libraries and frameworks used to make our "portion" of the app. The previous Team Home had used GraphQL, Auth0, Apollo, Prisma, and MongoDB -- all technologies that I had never used before! It certainly made looking at the code harder than usual, not to mention gave me a hard time with deploying the site on my Netlify account! Luckily, I managed to figure out how to deploy after several long discussions with my teammates over Zoom. The next step: configure it so that we can actually log in. 😕

## Tasks Pulled

Since our project requires us to add on new functionality to an already existing app, my goal this week was to understand the existing code. As such, all of my pull requests this week either adds comments to existing code or updates READMEs in order to better help my teammates:

* Ticket 1: README updates following deployment
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/249)
  * [Trello](https://trello.com/c/B4tcDzao/26-deploy-frontend-with-netlify)
* Ticket 2: Comments!
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/262)
  * [Trello](https://trello.com/c/7elFi5mj/18-learn-graphql-apollo-prisma-eileen)
* Ticket 3: More Comments!!
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/266)
  * [Trello](https://trello.com/c/7elFi5mj/18-learn-graphql-apollo-prisma-eileen)
* Ticket 4: Nothing but Comments!!!
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/267)  
  * [Trello](https://trello.com/c/7elFi5mj/18-learn-graphql-apollo-prisma-eileen)

## Detailed Analysis

<center>

![Environment Variables on Netlify](/assets/week1-env.jpg)
_Some of these names are kinda vague..._

_</center>_

The task I definitely struggled the most with this week was the first Ticket, regarding deployment. I spent a lot of time digging through the existing code to find out exactly where and how Auth0 was being implemented, and even after following the directions that was left for us in the README, I still had to dig around the internet for even more information! After signing up for numerous accounts (thank you for existing, password managers), I managed to gather all of the necessary ingredients I needed for my environment variables on the front end, and it eventually managed to load to the landing page and display the Auth0 signup modal!

<center>

![Comments in App.js](/assets/week1-appjs.jpg)
_Still have some doubts about where things are coming from_

_</center>_

After updating the frontend part of the README, I went off to help my two teammates focused on the backend this week. After much, much, _much_ more digging around, we managed to determine where exactly in the code we needed to change some hard-coded things, fixed them, and got the backend deployed as well. The only thing we couldn't manage to do was have the frontend and backend liked up to each other smoothly like it is in the original Team Home's deployed app, but that's a problem for next week.

# Part 2 - Milestone Reflections

In terms of helping out with the TDD that was due earlier this week, I went through most of the document and answered the questions so that others could edit it later. In doing this, we were able to complete the TDD and produce a very thorough draft by the end of the first day. In terms of research, I helped out with discovering how Basecamp works and its main features that would rival our own app. I was sent an invite to a Basecamp group created by Nedim and I went to town adding things and deleting things in order to realize the full potential of Basecamp. The functionality required by our application is very similar to Basecamp, so it is important that we learn everying that Basecamp can do in order to know what standard our app has to be at (and even surpass).
