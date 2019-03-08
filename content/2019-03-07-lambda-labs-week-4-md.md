---
title: Lambda Labs --- Week 4
date: 2019-03-07T21:36:50.804Z
cover: /assets/week4-spiderman-meme.jpg
slug: labs-week-4
category: Lambda Labs
tags:
  - week 4
---
# Part 1 - Individual Accomplishments this Week

Github handle: [eileencuevas](https://github.com/eileencuevas)

Personal Branch: [`frontend/eileen`](https://github.com/Lambda-School-Labs/labs-team-home/tree/frontend/eileen)

This week focused on the UI/UX of our app, which was what my teammates assumed I would spearhead. And I did with no complaints! I love styling.

The biggest challenge for this week involved working around the existing styles and incorporating Material UI into our parts of the site. Material UI proved to be a little harder to wrap my head around than I anticipated, but it all worked out in the end. Mostly.

## Tasks Pulled

### Front End

* **Ticket 1** - Documents Modal's Fresh New Look 
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/364)
  * [Trello](https://trello.com/c/9BHUVdh2/88-changing-styling-for-modals)
* **Ticket 2** - Documents Tab's Fresh New Look
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/368)
  * [Trello](https://trello.com/c/9BHUVdh2/88-changing-styling-for-modals)
* **Ticket 3** - Message Board's Fresh New Look
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/376)
  * [Trello](https://trello.com/c/9BHUVdh2/88-changing-styling-for-modals)
* **Ticket 4** - Action Buttons and Animations Galore
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/387)
  * [Trello](https://trello.com/c/YmDqS3yT/90-put-the-floating-back-into-the-floating-action-button)
* **Ticket 5** - Inputs: Now with More Contrast
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/400)
  * [Trello](https://trello.com/c/XoJKnJWq/97-change-inputs-and-buttons-styling)

### Bug Fixes

* **Ticket 6** - Fixes the accidental renaming of certain Functions
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/371)

## Detailed Analysis

Pick one of your tickets and provide a detailed analysis of the work you did.  This should be approximately ¼ page of text, and at least three screenshots.

This week's Detailed Analysis is brought to you by the Ticket 4!

* > **Ticket 4**
  >
  >  - Action Buttons and Animations Galore
  * >
    >
    > [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/387)
    >
    >
  * >
    >
    > [Trello](https://trello.com/c/YmDqS3yT/90-put-the-floating-back-into-the-floating-action-button)
    >
    >

![](/assets/week4-documents-new.png "Current view of Documents Tab")

One of the bigger chanllenges in making the UI of the website look more "professional" was figuring out what to do about the buttons controlling the various modals of the site. The previous team had decided to use a **F**loating **A**ction **B**utton (or FAB) to control the modal that allowed users to add Messages to the Message Board, and, being that we were supposed to build on top of existing code, I thought that there was little harm in keeping the button as a FAB. Of course, their implementation of a FAB was missing the "F" and had a lot of empty space around it, so I thought that would make a great starting point in my quest for a more professional layout.

Taking inspiration from all of the documentation surrounding FABs on the Material Design website, I decided to move the FAB to the bottom right corner. There, it can float to its hearts content, and still look good regardless of screen width. Plus, it _is_ where I'd expect an action button to be, considering all the Android apps that I've used up to this point in my life have a FAB in the bottom right. Since two of our components have FABs, I had to add the appropriate logic that would allow both FABs to have the same positioning but appear only when a user is on their respective components, which proved to be easier than I thought. Once that was done, I moved onto what would be the main challenge of this implementation: adding the pizzazz that Material Design wanted out of its FABs.

![](/assets/week4-fab-zoom.png "Snippet of Many Zoom Components")

<center>
\_Zoom, Zoom, Zoom, Zoom\_
</center>

In terms of design guidelines, Material Design suggests that all FABs should have an animation upon changing from one component to another. This is to help the user feel as if the buttons themselves are changing as well, which lets the user know that the button can now do something different than the button before it. The animation I decided to go with was Zoom, which would give the FABs the ability to zoom in and off the screen as a user switches from component to component. The cool thing about Zoom is that it was already baked into the Material UI library, so I didn't need to add anything else on that end. The only thing about Zoom is that it only seemed to animate properly as long as all the FABs were located in the same component. I ended up moving all of the FABs and things associated with FABs into their own component for the sake of Material Design, but at least it looks nice.

![](/assets/week4-state.png "Snippet of State of FloatingActionButtons.js")

One of the things that were packed into the new FAB component was all of the add functionality modals that were located all over the app. This meant that I had to keep track of three different modals, and I had to make sure that they were called one at a time under certain conditions. To help facilitate that, I had to make this FAB component a classical component with three bools in its state. While the name of the bools were not as pretty as my zooming FABs, it definitely did the trick. And with that, my saga of putting the "Floating" back into Floating Action Button came to a close.

# Part 2 - Milestone Reflections

Because a lot of the styling decisions were already made ahead of our team being solidified, we didn't have to make as many decisions regarding UI that other teams in Labs 10 had to. As such, we chose to focus on making the UI that we already have look more clean, which involved changing details of various sizes. My teammates had expressed their displeased opinions on the looks of various parts of the site, and as the team's apparently unanimously appointed design lead, I hunted down the offenders one by one. Gradients were removed in favor of solid colors, random logos disappeared overnight, color schemes morphing to resemble the iOS app—I did all that I could to make the central focus of the app be its contents rather than its looks, and I think that I've managed to achieve that.
