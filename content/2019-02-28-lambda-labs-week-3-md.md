---
title: Lambda Labs --- Week 3
date: 2019-02-28T23:47:41.244Z
cover: /assets/week3-gaminglan.jpg
slug: labs-week-3
category: Lambda Labs
tags:
  - week 3
---
# Part 1 - Individual Accomplishments this Week

Github handle: [eileencuevas](https://github.com/eileencuevas)

Personal Branch: [`frontend/eileen`](https://github.com/Lambda-School-Labs/labs-team-home/tree/frontend/eileen)

This week, I spent a lot more time working on the backend than I have in previous weeks. I managed to fix some issues regarding updating documents that had occurred in the backend, as well as integrate the ability to include tags on documents. However, working on things in the backend did not mean I wasn't involved in the frontend! I worked on updating our activity timeline to accommodate our new features and added some media queries so that our app looked good no matter the resolution you used it in.

All in all, it was a productive week. I'm still not completely confident in my abilities to manipulate material ui, but I'm not as lost as when I first started Labs.

## Tasks Pulled

### Features added

* **Ticket 1** - An improved Activity Timeline with Documents, Folders and Document Comments
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/333)
  * [Trello](https://trello.com/c/VsBjgQlW/67-update-activity-timeline-so-that-it-displays-newly-created-documents-folders-and-document-comments)
* **Ticket 2** - Added the ability to sort folders and documents
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/334)
  * Trello [1](https://trello.com/c/fZmYAlED/70-document-sort-function) & [2](https://trello.com/c/iJPU7cOM/71-folder-sort-function)
* **Ticket 3** - Added Tags to `Documents` schema/models/resolvers
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/339)
  * [Trello](https://trello.com/c/0MTJHw4M/80-added-tags-to-documents)
* **Ticket 4** - Added some much needed media queries
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/347)
  * [Trello](https://trello.com/c/2fUTLsv2/49-look-at-and-standardize-styling-for-front-end)

### Bug Fixes

* **Ticket 5** - Fixed deleteDocument so that it no longer returns null
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/322)
  * [Trello](https://trello.com/c/9QXwgEQh/68-deletedocuments-mutation-returns-null-when-invoked)
* **Ticket 6** - The Dashboard's input now submits upon pressing the enter key
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/323)
  * Trello
* **Ticket 7** - Activity Timeline now displays comments.... again. Where did they go?!
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/352)
  * [Trello](https://trello.com/c/EINzskiw/82-activity-timeline-does-not-show-comments-anymore-only-folders-documents-messages)

## Detailed Analysis

This week's blog post is brought to you by the Ticket number 1!

> **[Ticket 1](https://github.com/Lambda-School-Labs/labs-team-home/pull/333)**
>
> * An improved Activity Timeline with Documents, Folders and Document Comments

<center>

![](/assets/week3-activity-timeline.png "Current View of Activity Timeline")
</center>

Updating the Activity Timeline proved to be a much more difficult challenge than I expected! Originally, the activity timeline had a query nested inside of a query so that both the messages and message comments would be retrieved from the backend. After these queries were completed, they would be added to a Set, which would then lead to them being added to an array, which was then mapped over to provide the information needed to display each Activity card with the right styling. I thought that this wasn't a good way to retrieve information using GraphQL, so I set out on a mission to make a new query that would return everything I needed. 

The result of that mission: total failure. It was scrapped by lunch the next day.

<center>

![](/assets/week3-oldcode.png "Old ActivityTimeline.js")

_If it ain't broke don't change it._

_</center>_

After lunch and a talk with my team, I decided to follow the example of the previous code, and have multiple queries. My execution involved three main queries: one for Messages, one for Documents, and one for Folders. Inside of the queries for Documents and Messages was another query, for the comments of said items. After the three queries were completed, the items would then be pushed into one array which would then be mapped over to provide the information needed for the Activity cards. It wasn't very pretty, nor was the size of the file any smaller, but it worked. And it continued to work until our database was manually reset the next day.

For whatever reason, our Activity Timeline refused to display any comments. It continued to display Messages, Documents and Folders without issues. If I expanded on the solution that was already in place (relying on Boolean variables to let React know when to render the Activity card components), no items would render in the Activity Timeline. For whatever reason, it seemed as if the queries for comments were not running, even though they would appear in our array of items. So I decided to try a different approach—instead of using an `if` statement that waited for multiple variables to equal `true`, I decided to have the same `if` statement check to see if our array of items had anything inside of it and then proceed to map and return our Activity cards. It seems to be working without issues now.

<center>

![](/assets/week3-activity-fix.png "Current Fix for ActivityTimeline.js")

_We loved `allTheThings`'s name so much we decided to keep it_

</center>

# Part 2 - Milestone Reflections

Our project _was_ a little different from other teams, as we inherited code from another team. Because of that, it was already organized into a "complete" product (or, was complete according to their MVP).  Our addition to this project became challenging _because_ it was already complete—things that we believed should be together in certain folders in the file structure were in completely different parts of the repository because that was how the previous team had organized it. So we had to figure out how our documents-related components would fit according to the existing structure and if it were really necessary to make certain organizational changes. My teammates agreed that our documents didn't share much in common with the existing message board-related components, and as such, we had to move things around as the existing code had nearly everything (including the Activity Timeline) filed away under the Message Board items. Once that was done, we only had to figure out what the main "container" of our components would be. Everything else seemed to fall into place, as how our components worked with each other seemed pretty self-explanatory: Folders would relate to Documents, Folder Details would relate to Folders, and Folder Details didn't relate to Documents for example.
