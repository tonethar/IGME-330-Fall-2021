# Project 2 - *VanillaJS App - now with Maps or Cloud Storage*

## I. Overview
- This project is a continuation of Project 1, with **at least ONE** of the following additions:
  - An integrated [Mapbox](https://www.mapbox.com/) map
    - you would choose this option if your API returns location data
    - The following HW will help you get comfortable with Mapbox:
      - [Mapbox I - Mapbox Intro](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-mapbox-1.md)
      - [Mapbox II - RIT Coffee Finder](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-mapbox-2.md)
      - [Mapbox-III - Virus Map (optional extra credit)](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-mapbox-3.md)
      - Note that the first two HW assignments above are required for EVERYONE even if you choose to use Firebase instead
  - App data stored in the cloud via [Firebase](https://firebase.google.com/docs/web/setup):
    - you will store some of your app data in "the cloud" (as opposed to localStorage that only stores data locally)
    - what kind of data to store? Maybe search terms for all users, "favorited" or highest rated links or images or Pokemon, etc...
    - The following HW will help you get comfortable with Firebase:
      - [1 - Intro to Firebase - the Realtime Database](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-1.md)
      - [2 - Firebase Highscore App](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-2.md)
      - [3 - Firebase Highscore Viewer](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-3.md)
      - [4 - Firebase "Draw & Share" App (optional extra credit)](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-4.md)
      - Note that the first three HW assignments above are required for EVERYONE even if you choose to use Mapbox instead

<hr>

## II. Requirements
- ALL of the Project 1 requirements are still in effect. If you did not meet them the first time around, here is your chance to get them done:
  - [Project 1](project-1.md)
  - [Course Code Style Requirements](code-style.md)
- Be sure to incorporate your Prof's Project 1 feedback into Project 2:
  - You may not yet have a firm grade on that Project, but you should have received feebdback about any obvious changes that were needed. If not, contact your prof.
- One of the Project 1 requirements for the App page, III-B - #2 - *On the app page, you will automatically save the last term searched by the user and other UI *state* in the browser's local storage*, was deferred to this project. Don't forget to complete this requirement.
- You must add Mapbox OR Firebase capability to your project (you can add both if you wish)
- You must update your *Sources* page to describe all of the changes you made since P1, and how you utilized Mapbox or Firebase on the project

### II-A. Mapbox Guidelines

- Don't make the map any bigger than it needs to be - the HW assignments used fullscreen maps - but you will likely only need a smaller map (ex. head to yelp.com to see how they use maps - they are not full screen)
- You must have markers in the map - these will likely show a user's search results
- The markers must be clickable and display useful information
- There must be map controls for the user
- New searches will probaby wipe out "old" markers from previous searches
- If you want to add layers to your map, see the **Mapbox-III - Virus Map** extra credit assignment

### II-B. Firebase requirements
- You must to save some sort of web site data to "the cloud" using Firebase (typed in user search terms, favorited Pokemon, etc):
  - **2 - Firebase Highscore App** covers how to *save* data to the cloud using Firebase
- You must add a **community.html** page that will display at least some of this data to your users
  - **3 - Firebase Highscore Viewer** covers how to *read* data from the cloud using Firebase
- Important Note:
  - *Individual data* - a user's favorites and other user data (such as the last term searched by that user and other UI state) are still stored in the browser's local storage and displayed on your **favorites.html** page
  - **community.html** will shows favorites (or other data) for ALL of the users

<hr>

## III. Rubric

- Same as Project 1, with 30% of the overall Project 2 grade being determined by the integration of Mapbox or Firebase into this project

<hr>

## IV. Get Started
- Make a copy of your **project-1** folder (or whatever you called it) and name it **project-2**
  - ***Start fixing any bugs and implement any missing requirements NOW***
- IMPORTANT: Do not delete or modify the files in your **project-1** folder on banjo - leave it be - we need to see what changes you make between Project 1 and Project 2
- Post to the "Project 2 Changes" discussion thread before it closes Sunday night:
  - tell us whether you are going to utilize Mapbox or Firebase
  - tell us what features you will implement with the above API
  - tell us what other features you plan to add to the project
  - -10% from project grade if not done

<a id="examples" />

<hr>

## V. Examples

**Community Page**

![screenshot](_images/p2-example-1.png)

- Note the limit of 10 community favorites being displayed at once - you will probably want to do something similar

