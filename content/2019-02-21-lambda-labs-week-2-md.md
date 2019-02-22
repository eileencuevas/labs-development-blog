---
title: Lambda Labs --- Week 2
date: 2019-02-22T13:00:41.844Z
cover: /assets/approve.jpg
slug: labs-week-2
category: Lambda Labs
tags:
  - week 2
---
# Part 1 - Individual Accomplishments this Week

GitHub handle: [eileencuevas](https://github.com/eileencuevas)

Main Branch for Labs Team Home: [`frontend/eileen`](https://github.com/Lambda-School-Labs/labs-team-home/tree/frontend/eileen)

This week, after fixing the nightmare that was Auth0, I managed to finally get to work on the app! I managed to change some of the styling of the old app, as it was kind of distracting and not very user-friendly (as great as smooth gradient animations are in the nav bar, it _really_ catches your attention and moves it from the actual important stuff). Aside from learning where all of these styles came from, I also managed to refactor some of the navigation-related code so that it looked a little neater. Also, In terms of new additions to the app, I managed to use GraphQL to finally query things in the front end! Now, we can see all folders related to a team and all documents related to a team.

## Tasks Pulled

### Notable Accomplishments

* Ticket 1 -- Death of the Gradients
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/281)
  * [Trello](https://trello.com/c/2fUTLsv2/49-look-at-and-standardize-styling-for-front-end)
* Ticket 2 -- Streamlining the Settings Page
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/312)
  * [Trello](https://trello.com/c/2fUTLsv2/49-look-at-and-standardize-styling-for-front-end)
* Ticket 3 -- Let's see some folders!
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/296)
  * [Trello](https://trello.com/c/T8lgsETc/52-start-building-folder-components)
* Ticket 4 -- Let's see some documents!!
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/305)
  * [Trello](https://trello.com/c/yMmCN7UC/51-start-building-document-components)

### Housekeeping

* Ticket 5 -- Removing unnecessary components
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/287)
  * [Trello](https://trello.com/c/huJx4u4q/45-refactor-code)
* Ticket 6 -- Organizing Folder components, the right way
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/299)
  * [Trello](https://trello.com/c/huJx4u4q/45-refactor-code)

## Detailed Analysis

This week's Ticket Topic of Choice will be: 

**Ticket 3 -- Let's see some folders!**

In order to have such functionality implemented into our app, I needed to take things step by step. My first step, of course, would be to add the `Documents` tab that we now see in our app, as it didn't exist! Implementing that took some time, as I had to adjust some of the logic they used to allow the changing of displayed components based on the active tab, but not even ternary functions could stop me!

![Sveza Documents Page](/assets/week2-new-sveza.png)

_Ooh, fancy!_

After that, the next step required me to write out the query associated with getting all folders that "correspond" to the currently selected team. This gave me a slightly harder time because of my own mistakes: I had referenced the wrong variable in my query! After fixing that, I managed to display all the titles of the folders in the document tab.

![Wrong query displayed next to correct query](/assets/week2-query-mistake-vs-fixed.png)

_It's the little things that get you_

Finally, after getting the folders to show their name on our app, I decided to have some fun with them and style them to look like little folders. I originally needed them to be small rectangles so that my teammates and I could visualize how we wanted our documents to be stored in the folders visually after we implemented drag and drop, but I decided to go the extra mile and shape them into folders using `clip path`.

![Code for Individual Folder Styling](/assets/week2-folder-vs-code.png)

# Part 2 - Milestone Reflections

A major part of making a team feel less like a group of people working together and more like a team is **communication**. I knew that, in order for us to feel like we were part of a team, we had to contact one another at various points of the day to keep each other updated and we needed encourage others to voice their feelings on certain matters. We all agreed that this was important, so we agreed to do so via zoom chats.

We had a zoom link pinned in the chat once a day, and, in doing so, we basically spent all of our time inside the zoom every day. I even had my camera on all day, to show that I was physically there (even though my mind was occasionally on stuff that wasn't currently being shared on the zoom screen). Anytime anyone had a problem, that person would share their screen and we'd all try to help them with their issues. If some one had a question about which direction they needed to start heading in in terms of code, design, or organizational structure, they would share their screen and we'd all listen. Even I managed to get the opinions of everyone this way a couple of times, including this morning!

This morning, the group decided that the current settings page of the app didn't quite meet our standards in terms of the looks department. Since I wasn't quite sure what would look best for the settings page, I merely shared my screen and began changing the css of the settings page live using the chrome developer tools. My teammates would then annotate the screen regarding things that should move, and offer their ideas on what they thought looked good and what could be even better. After doing that and getting a settings page that they all agreed looked good, I then implemented our changes locally in the code.
