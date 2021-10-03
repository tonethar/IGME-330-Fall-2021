# Project 1 - Tips & Tricks

## Notes:

- [Project 1 Requirements](project-1.md)
- [Project 1 Coding Standards](code-style.md)
- We will keep updating this page - so check back periodically!

<br>

## Navigation:

- [**Code Tips**](#code-tips)
- [**Component Tips**](#conmponent-tips)

<hr><hr>

<a id="code-tips" />

## I. Code Tips

### I-A. General tips (and requirements)

- your `<script>` tags MUST be at the "top" of each HTML file (i.e. in the `<head>` section)
- your `<script>` tags MUST be be of `type="module"`
- ES6 modules:
  - by default, will [`defer`](https://www.w3schools.com/tags/att_script_defer.asp) code execution until the DOM has loaded, so you most likely DO NOT need any `window.onload` code anywhere in P1
  - run in ["strict mode"](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode) by default, so you WILL NOT need any [`"use strict";`](https://www.w3schools.com/js/js_strict.asp) declarations at the top of any of your code files
  - ES6 Module Notes are here - [ES6 Module Pattern](https://github.com/tonethar/IGME-330-Master/blob/master/notes/ES6-module-pattern-2211.md)
  - Look at this ZIP of ["Module Demos"](https://github.com/tonethar/IGME-330-Master/blob/master/notes/_files/Module%20Demos%202211.zip) - we looked at these on 6A
  - Recall that [HW - Web Components-3 - Build a component driven web app](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-3.md) also used ES6 modules


<hr>

### I-B. `loader.js`

- The "hamburger" code that was in **index.js** is something that every one of your P1 pages needs. You will need to convert this file over to an ES6 module for this project, which is easy! First, rename **index.js** to **loader.js**, and then make it look like this:

**loader.js**

```js
// Because every P1 page will link to this script,
// it's a great place to load your components! 
import "./components/my-component-1.js";
import "./components/my-component-2.js";
import "./components/my-component-3.js";

window.onload = () => {
  const burgerIcon = document.querySelector("#burger");
  const navbarMenu = document.querySelector("#nav-links");
  burgerIcon.onclick = () => navbarMenu.classList.toggle('is-active');
};
```

- Now link to it from every one of your P1 pages:

```html
<script src="src/loader.js" type="module"></script>
```
<hr>

### I-C. `app.js`

- **app.js**
  - contains your main app functionality
  - is linked to from **app.html**

```html
<script src="src/app.js" type="module"></script>
```

<hr>

### I-D. `favorites.js`

- **favorites.js**
  - contains your main app functionality
  - is linked to from **favorites.html**

```html
<script src="src/favorites.js" type="module"></script>
```

<hr>

### I-E. `utils.js`

- this will have code (functions and/or classes) that is utilized by your the other script files (**app.js** & **pavorites.js** and maybe others)
- you WILL NOT link to this **utils.js** with a `<script>` tag
- you will instead `import` this file into your other script files where it is needed - example:

```js
// first style - specify what you want to import
import {loadDataFetch,calcRating} from './utils.js';

// second style - import everything that was exported under the `utils` namespace
import * as "utils" from './utils.js';
```

- and don't forget to `export` functions/classes from **utils.js**

<a id="component-tips" />

<hr><hr>

## II. Component Tips
