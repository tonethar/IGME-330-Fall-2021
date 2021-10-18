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
  - "NoSQL" in this case means that all of your data is stored in what is essentially a single JSON object, as opposed to being broken out into separate SQL tables (ex.  `Person` and `Address` or `BlogPost`)
  - "sync data in realtime" - means that data changes can be immediately (within milliseconds) propogated to all of the users of your web app
  - the realtime database will also continue to work when the user is offline (by caching changes) and will automatically sync itself with the cloud when the user re-connects
- Even though Firebase is NoSQL, our app still needs Firebase to do the same things that a SQL database does - specifically the **CRUD** operations:
  - ***C*reate** - in the *DogFinder* app page, we need to create a new favorite (in the cloud) everytime a user favorites a dog picture
  - ***R*ead** - on the DogFinder Community page, we need to download the `url` and `like` values for 10 most popular dog pictures
  - ***U*pdate** - if a user favorites a dog image that has already been favorited by someone else, we need to increase the `like` value by 1
  - ***D*elete** - if an *admin* needs to delete a favorite - maybe it's a mal-formed url, or maybe the image violates the site's standards (this has not been implemented by the DogFinder example)

### III-B. HW - *Intro to Firebase* walkthrough

- [1 - Intro to Firebase - the Realtime Database](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-1.md)
- Note that you first create a *project*, then an *app*:
  - "A Firebase project is the top-level entity for Firebase. In a project, you create Firebase apps by registering your iOS, Android, or web apps" - the idea being that you could build different apps for Web, iOS, Android, Unity, different OS versions etc - and have them all talk to the same backend
  - https://firebase.google.com/docs/projects/learn-more
- Note that you can use the Firebase realtime database control panel to perform all of the **CRUD** operations on your app's data 
- Let's walk through **firebase-test.html**
  - Note that we are using an `import` statement rather than a `<script>` tag to load in the Firebase libraries, and that we are specifying the symbols that wee need:
    - `import { getDatabase, ref, set, push, onValue } from  "https://www.gstatic.com/firebasejs/9.1.3/firebase-database.js";
  - Note how we initialize Firebase:
    - `const app = initializeApp(firebaseConfig);`
    - check out `app` in the debugger - it's a mostly *opaque* object that the **Realtime Database** will utilize - we won't be calling any methods on it
  - Note how we initialize the **Realtime Database**
    - `const db = getDatabase();`
    - check out `db` in the debugger - it's a mostly *opaque* object - we won't be calling any methods on it - instead we'll be passing it as a parameter into the various **Realtime Database** functions such as `set()` and `ref()`
  - Now we'll **CREATE** some data with **`set()`** - and **UPDATE** it too:
    - the `ref()` function (which we imported)
      - *returns a Reference representing the location in the Database corresponding to the provided path*
      - `ref(databaseRef, path)` returns a `DatabaseReference`
    - the `set()` function (which we inported)
      - *writes data to a database location*
      - `set(DatabaseReference, value)`
    - take a look in `writeUserData(userId, name, email)` and see how it adds "Ace Coder" to the Database
      - we create a reference to `users/abc1234` in the **Realtime Database** by passing in `db` and  `"users/abc1234"`
      - we use `set()` to *write* the "Ace Coder" data (provided as an object literal) to the **Realtime Database**
    - Go check the Firebase Control panel to see the changes
   - Note that by adding data with `set()` and providing a path that is a unique user ID,  we are essentially providing the unique *key* by which this data can be updated or deleted
     - this means that when we do a `set()` with the same user path, it will *over-write* the old user data, and NOT create new user data on `users/`
       - meanign that `writeUserData("xyz9876","Ima Graduate","ima@realworld.com");` would **Update** "Ima Student" to "Ima Gradute" (another **CR*U*D** operation)
     - test this by reloading the **firebase-test.html** page multiple times and then checking the `users/` path in the Firebase Control Panel - you should still only see these 2 users

#### `push()` -  another way to *Create* data in the cloud

- The following function is for adding high score data to the `scores/` path
- Note that below we use `push()` instead of `set()`
- When you use `push()` instead of `set()`, you are adding values to a *list*
- Firebase will generate a unique *key* for each value (rather than an idex) so that we can reference it later on if we want to
- This also means that we can duplicate values in the list - for example with the same `userId`, `game` and `score`
- test this by reloading the **firebase-test.html** page multiple times and then checking the `scores/ path in the Firebase Control Panel - you should see multiple instances of the same score

```js
function writeHighScoreData(userId, game, score) {
  const db = getDatabase();
  const scoresRef = ref(db, 'scores');
  const newScoreRef = push(scoresRef,{
    userId,
    game,
    score
  });
  // the unique ID generated by Firebase that we could use later to reference or change this value
  console.log("newScoreRef",newScoreRef.key);
}
```
 
 <hr>
 
### III-C. HW - *Firebase Highscore App* walkthrough

- [2 - Firebase Highscore App](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-2.md)
- Believe it or not, there are no new Firebase concepts here - it's just a working example of a (lame) game, and a UI for writing high scores to the cloud
  - In the first part, we reuse `writeHighScoreData()`, which will `push()` scores to the Firebase `scores/` path, which allows for each user to have mulitple scores on that path
  - In the second part, we create `writeHighScoreData2()`, which uses `set()` to create a `scores2/userId` path - which means that each `userId` can only have ONE score in the cloud

<hr>

### III-D. HW - *Firebase Highscore Viewer* walkthrough

- [3 - Firebase Highscore Viewer](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-3.md)
- A new **C*R*UD** operation - **Read** !
- Firebase makes it easy to be notified when any of your cloud values change - the `onValue` function (which we are importing)
  - *Listens for data changes at a particular location. This is the primary way to read data from a Database. Your callback will be triggered for the initial data and again whenever the data changes*
  - https://firebase.google.com/docs/reference/js/database.md#onvalue
  - `onValue()` takes 2 parameters - a **Realtime Database** path to "watch" for chnages, and a callback function to invoke when a change happens:

```js
const db = getDatabase();
const scoresRef = ref(db, 'scores');

function scoresChanged(snapshot){
	snapshot.forEach(score => {
		const childKey = score.key;
		const childData = score.val();
		console.log(childKey,childData);
	});
}

onValue(scoresRef,scoresChanged);
```

- Let's use the **firebase-high-score.html** page from last time to add some high scores to the `scores/` path
- Check **firebase-admin.html** - the new scores should instantly appear!


<hr>

## IV. What else?

- The HW assignments covered quite a bit, but there's still a little bit more about Firebase we'll cover at our next class meeting (because you may need it for P2):
 - `get(path)`
   - *Gets the most up-to-date result for this query.*
   - https://firebase.google.com/docs/reference/js/database.md#get
   - returns a *Promise* - remember those?
 - `update(path,values)`
   - *Writes multiple values to the Database at once.*
   - https://firebase.google.com/docs/reference/js/database.md#update
   - returns a *Promise* - remember those?

<hr><hr>


| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-08B-notes.md**](week-08B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-09B-notes.md**](week-09B-notes.md) 
