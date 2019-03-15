---
title: Lambda Labs --- Week 5
date: 2019-03-15T02:26:22.167Z
cover: /assets/image-3-.png
slug: labs-week-5
category: Lambda Labs
tags:
  - Week 5
---
# Part 1 - Individual Accomplishments this Sprint

Github handle: [eileencuevas](https://github.com/eileencuevas)

Personal Branch: [`frontend/eileen`](https://github.com/Lambda-School-Labs/labs-team-home/tree/frontend/eileen)

This week, I spent all of my time putting the finishing touches on the styles of the site. I also spent time working with Kai on the brand new Landing page, helping him with writing the code for it and providing help with styling it. In addition to that, I also spent time helping with the other presentation aspects of the site, namely the logo and video. Because we were asked to rebrand the site at last minute, we needed a new logo, and I was in charge of implementing the logo that we chose in a matter that matches the color scheme of the site. This implementation was also used in the video we made (which I had to string together and render).

## Tasks Pulled

### Front End

* **Ticket 1** - Modal Scrollbars no more
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/409)
  * [Trello](https://trello.com/c/o5bScvY1/117-fix-modals-so-that-the-scrollbar-doesnt-show-up-outside-of-the-modal)
* **Ticket 2** - Folders' New Look
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/412)
  * [Trello](https://trello.com/c/5CzXNpln/116-change-folder-styling)
* **Ticket 3** - Mo' Material UI
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/417)
  * [Trello](https://trello.com/c/2fUTLsv2/49-look-at-and-standardize-styling-for-front-end)
* **Ticket 4** - The Big Landing Page Update
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/428)
  * [Trello](https://trello.com/c/mXBzAK3Q/108-landing-page-the-big-one)
* **Ticket 5** - New Logo!
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/433)
  * [Trello](https://trello.com/c/1inEXrXv/118-add-new-arq-logo)

### Bug Fixes

* **Ticket 6** - Fixes modals so that they go full screen again
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/418)
* **Ticket 7** - Removes Anchor Animations so that the page no longer refreshes automatically
  * [Github](https://github.com/Lambda-School-Labs/labs-team-home/pull/444)

## Detailed Analysis

Pick one of your tickets and provide a detailed analysis of the work you did. This should be approximately ¼ page of text, and include screenshots if appropriate

This week's Detailed Analysis is brought to you by the Ticket 3!

> [**Ticket 3**](https://github.com/Lambda-School-Labs/labs-team-home/pull/417)
>
> Material UI style changes for Inputs and Drop Down menus

The focus of this pull request was to make sure that everything looked as Material Design as possible. That included the few inputs located inside of the `SettingsView` component and the Sort forms that were located in the `MessageBoard`, `Folders`, and `DocumentContainer` Components.  

![](/assets/week5-input.jpg "Code for the Inputs in Settings View")

For the inputs located in the Settings Menu, I attempted to style them like I would style any component using Styled Components, which didn't end up well for me. I could change the color of the background and even change the color of the border to an extent, but I couldn't add any padding no matter how hard I tried! In order to make the inputs have as much padding as their input cousins located in the `Add` modals, I had to change the Inputs from the Material-UI Input component to the Material-UI Textfield component.

With that complete, I had to focus on my next ~~headache~~ mission, which involved the unstyled sort menus located throughout the site.

![](/assets/week5-sort.jpg "Code for Drop Down Menus")

For the sort drop down menus, I needed them to look similar to the input forms. I decided to use the `Select` Material-UI component by itself at first as it seemed like it would fit my needs with little issue. Like the inputs above, I had tried to style the component using styled components to no avail. I could not add a background color to `Select` no matter what I did. After some much digging, I managed to find a solution and get the sort forms to look like they currently do. In order to achieve this, I needed to put together two Material-UI components that would help me achieve this effect: `OutlinedInput` and `Select`. The `OutlinedInput` provided the rounded look I needed for the menu to look like our inputs while the `Select` component provided the rest. 

![](/assets/week5-sortform.png "Implementation of the Menu")

# Part 2 - Weekly Reflection

In all, working on this experimental team for Labs has been a big learning experience. We spent a lot of time dealing with issues stemming from choices made by the previous team as well as issues stemming from our own choices. We went into every week wondering if we should just replace entire sections of the previous teams' work, including the entire backend of the project. However, we knew that that would take an extraordinary amount of work to pull off successfully, so we continued to work around our limitations. Even though a lot of the design of the final site involves design choices that I would not make had my team been a non-experimental team, I'm still pretty proud of how far we've come.
