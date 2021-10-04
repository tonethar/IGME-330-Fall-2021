# Project 1 - Tips & Tricks

## Notes:

- [Project 1 Requirements](project-1.md)
- [Project 1 Coding Standards](code-style.md)
- We will keep updating this page - so check back periodically!

## TOC:

[**I - Code Tips**](#code-tips)

[**II - Component Tips**](#component-tips)

[**III - Bulma/CSS Tips**](#css-tips)

[**IV - Ajax Tips**](#ajax-tips)

[**V - Other Tips**](#other-tips)
 
<hr><hr>

<a id="code-tips" />

## I. Code Tips

### I-A. General tips (and requirements)

- your `<script>` tags MUST be at the "top" of each HTML file (i.e. in the `<head>` section)
- your `<script>` tags MUST be be of `type="module"`
- ES6 modules:
  - by default, will [`defer`](https://www.w3schools.com/tags/att_script_defer.asp) code execution until the DOM has loaded, so you most likely DO NOT need any `window.onload` code anywhere in P1
  - run in ["strict mode"](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode) by default, so you WILL NOT need any [`"use strict";`](https://www.w3schools.com/js/js_strict.asp) declarations at the top of any of your code files
  - ES6 Module class notes are here - [ES6 Module Pattern](https://github.com/tonethar/IGME-330-Master/blob/master/notes/ES6-module-pattern-2211.md)
  - here is the ZIP of ["Module Demos"](https://github.com/tonethar/IGME-330-Master/blob/master/notes/_files/Module%20Demos%202211.zip) - we looked at these on 6A
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

const burgerIcon = document.querySelector("#burger");
const navbarMenu = document.querySelector("#nav-links");
if (burgerIcon) burgerIcon.onclick = () => navbarMenu.classList.toggle('is-active');

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

- this will have code (functions and/or classes) that is utilized by your the other script files (**app.js** & **favorites.js** and maybe others)
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

### II-A. Don't "over engineer" your components
- Do not write more code then you have to
- Unlike our components HW assignments, most of your P1 components won't be need to be updated after the HTML page loads
- For example, if you have a `<p1-footer>` component that appears on every page of your P!, and it takes `year` and `authorname` attributes, and these values will NEVER change after each of the page loads - it means:
  - you won't need to "watch" for any attribute changes after `connectedCallback` is called
  - meaning you don't need to implement `observedAttributes()` or `attributeChangedCallback()`
  - meaning that you could set the state of the HTML (ex. the `year` and `authorname`) in the `constructor()`, thus you wouldn't need a `render()` helper method
  - and, if your component doesn't have any JavaScript, you won't even need to implement `connectedCallback` or `disconnectedCallback`

<hr>

### II-B. A `<p1-nav>` component

- A very useful component (not required, but it would be a good one to implement), because all of that `<nav>` HTML is repeated on each of your P1 pages (at least 4 times!):
  - But you will also need to move the "hamburger JS" from **loader.js** to your component
  - Hint: in the component constructor, initialize `this.burgerIcon` and `this.navbarMenu` and make them *properties* of the `<p1-nav>` component
  - Hint: a `currentPage` attribute would be really helpful - then you can (for example) make the current page name **bold** - so that the user has an additional "where am I?" cue 

<a id="css-tips" />

<hr><hr>

## III. Bulma/CSS Tips

### III-A. HW Assignments

- [HW - Bulma I - Intro to Bulma](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-bulma-1.md)
  - here is the Bulma walkthrough where you build a P1 starter site
  - there is not a dropbox for this nor a due date, but you will very likely need to go through this fairly soon in order to meet the Bulma requirement for Project 1
- [HW - Bulma II - Bulma & Web Components](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-bulma-2.md)
  - Covers how to get Bulma & Web Components working together

<a id="ajax-tips" />

<hr><hr>

## IV. Ajax Tips

### IV-A. HW Assignments

- [HW - Ajax-4 - loading and parsing JSON files](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-4.md)
- [HW - Ajax-5 - the `fetch()` API](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-5.md)
- [HW - Ajax-6 - `async` & `await` with the `fetch()` API](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-6.md)
- [HW - Ajax-7 - JavaScript Promises](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-7.md)

<a id="other-tips" />

<hr><hr>

## V. Other Tips

### V-A. App Usability

- Each page must have "you are here" cues
- "Let the user know what's going on"

### V-B. Spelling

- Fix spelling & grammar errors
- This includes your file names - ex. you should be spelling words like "component" and "utilities" correctly - we DO NOT want to see files named something like **footer-compnent.js**

<hr><hr>
