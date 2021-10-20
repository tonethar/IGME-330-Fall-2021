# Week 9B - Finish up Project 2

## I. Project 2
- [Project 2](../projects/project-2.md)
- [Project 1 & 2 - Tips & Tricks](../projects/p1-tips.md)
- [Course Code Style Requirements](../projects/code-style.md)

<hr>

## II. More Firebase - creating a `likes` counter for Dog Names

## II-A. Overview
- What we are going to build is "likes counter" for user submitted dog names
  - every time a use submits a new dog name, it is added to the `favorites/` path, and given a property of `likes: 1`
  - if this dog name already exists in Firebase, the `likes` property of that dog name is incremented by 1
  - here is a screenshot of the completed example app (on the left), and the Fiebase console (on the right)

<hr>

![screenshot](../_images/gab-dog-1.jpg)

<hr>

### II-A. Start Code

**gab-dog-1-start.html**

```html
<!doctype html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>GabDog</title>
	<style>
	*{
		font-family: sans-serif;
	}
	</style>
</head>
<body>
<h1>GabDog&trade;</h1>
<h3>We want to know - what's a good dog name?</h3>
<p>Name --> <input value="Rover" id="nameField"></p>
<button id="btnSubmit">Send Name to Server</button>
<hr>
<h3>Popular Names</h3>
<ol id="favoritesList"></ol>

<script type="module">

// TODO: ADD YOUR imports and Firebase setup code HERE

//

const writeFavNameData = name => {
  const db = getDatabase();
  const favRef = ref(db, 'favorites/' + name);
  set(favRef, {
      name,
      likes: 1
  });
};

function favoritesChanged(snapshot){
  // TODO: clear #favoritesList
  snapshot.forEach(score => {
    const childKey = score.key;
    const childData = score.val();
    //console.log(childKey,childData);
    // TODO: update #favoritesList
  });
}

const init = () => {
  const db = getDatabase();
  const favoritesRef = ref(db, 'favorites/');
  onValue(favoritesRef,favoritesChanged);
	
  btnSubmit.onclick = () => {
    writeFavNameData(nameField.value);
  };
};

init();

</script>

</body>
</html>
```

<hr>

### II-B. Notes

**gab-dog-1.html**

#### 1) - Get the basics working

- Add the Firebase/Firebase Realtime Database setup code
- Display the favorite dogs in `#favoritesList` - see screenshot above for an idea of what it should look like - but in this version, we can't record any more "likes" than 1
- The fact we can't increment `likes` on existing dog names is a probelm - so let's fix it!

<hr>

#### 2) - Get "`likes ++`" working the "super easy" way

- We'll use the [`ServerValue.increment()`](https://firebase.google.com/docs/reference/kotlin/com/google/firebase/database/ServerValue#increment_1)
- You'll need to `import` this function to use it - add `increment` to your ".../firebase-database.js" import
- Make `writeFavNameData()` look like this - it's only one small change to the code:

```js
const writeFavNameData = name => {
  const db = getDatabase();
  const favRef = ref(db, 'favorites/' + name);
  set(favRef, {
    name,
    likes: increment(1)
  });
};
```

- test it - incrementing `likes` should now work!

<hr>

#### 3) - Get "`likes ++`" working the "harder" way
- This technique will use `get()` and `update()`
- It's not technically needed for this example (because of `increment(1)` above), but this is good to know how to do in case you want to perform updates other than incrementing
- Make a copy of **gab-dog-1.html** and name it **gab-dog-2.html**
- You will need to import `get` and `update` in your ".../firebase-database.js" import
  - X


<hr>

### II-C. Documentation
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
| [**week-09A-notes.md**](week-09A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | :-/
