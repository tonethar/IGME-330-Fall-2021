# Week 9A - Firebase

## I. Firebase HW (due soon!)

- [1 - Intro to Firebase - the Realtime Database](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-1.md)
- [2 - Firebase Highscore App](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-2.md)
- [3 - Firebase Highscore Viewer](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-3.md)

<hr>

## II. Project 2

- [Project 2 (with *Community* page example)](../projects/project-2.md#examples)
- [Project 1 & 2 - Tips & Tricks](../projects/p1-tips.md)
- [Course Code Style Requirements](../projects/code-style.md)

<hr>

## III. Firebase Notes

### III-A. Overview

- "The Firebase Realtime Database is a cloud-hosted NoSQL database that lets you store and sync data between your users in realtime."
  - "cloud-hosted" means that it can be accessed by multiple users and devices from anywhere on the Internet
  - "NoSQL" in this case means that all of your data is stored in what is essentially a single JSON object, as opposed to being broken out into seperate SQL tables (ex.  `Person` and `Address` or `BlogPost`)
  - "sync data in realtime" - means that data changes can be immediately (within milliseconds) propogated to all of the users of your web app
  - the realtime databse will also continue to work when the user is offline (by caching changes) and will automatically sync itself with the cloud when the user re-connects
- Even though Firebase is NoSQL, our app still needs Firebase to do the same things that a SQL database does - specifically the **CRUD** operations:
  - ***C*reate** - in the *DogFinder* app page, we need to create a new favorite (in the cloud) everytime a user favorites a dog picture
  - ***R*ead** - on the DogFinder Community page, we need to download the `url` and `like` values for 10 most popular dog pictures
  - ***U*pdate** - if a user favorites a dog image that has already been favorited by someone else, we need to increase the `like` value by 1
  - ***D*elete** - if an *admin* needs to delete a favorite - maybe it's a mal-formed url, or maybe the image violates the site's standards (this has not been implemented by the DogFinder example)

### III-B. HW Intro to Firebase walkthrough

- [1 - Intro to Firebase - the Realtime Database](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-1.md)
- 




<hr><hr>


| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-08B-notes.md**](week-08B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-09B-notes.md**](week-09B-notes.md) 
