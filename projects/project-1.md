# Project 1 - *VanillaJS App of Awesomeness*

[I. Overview](#overview)

[II. Functionality](#functionality)

[III. User Experience](#user-experience)

[IV. Code](#code)

[V. Media](#media)

[VI. Examples](#examples)

[VII. Rubric](#rubric)

[VIII. Documentation & Submission](#submission)

<a id="overview"/>

## I. Overview

For this project you are creating a JavaScript driven Web application that utilizes one or more Web services.

- Your goal is to create an application that does something useful, and is easy to use, functional, and aesthetically pleasing.
- The app should serve a purpose - i.e it should be useful to *someone*
- Ideally the experience will run in all modern browsers, but at a bare minimum it must run in recent versions of Chrome.
- The objective of this project is for you to demonstrate your mastery of HTML5/CSS/JS "rich media" programming in a web browser context
- You will be evaluated on:
    - the quality of the experience you create
    - the soundness of your programming
    - meeting the requirements detailed below
    - how far you went beyond what we did in class, as described below

<hr>

<a id="functionality"/>

## II. Functionality


<hr>

<a id="user-experience"/>

## III. User Experience

<hr>

<a id="code"/>

## IV. Code

1) Code standards:
    - ES6 modules - at least 4 distinct code files in a **src** folder - ex. **src/loader.js**, **src/main.js**, **src/utils.js**, **src/classes.js**:
      - *No JS code is allowed in your HTML file*
      - Instead, use a single `<script>` element to load in the JS code you wrote - ex. `<script src="src/loader.js" type="module"></script>`
      - your modules will use the [`import`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) and/or [`export`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) keywords as needed
    - declare variables with `const` & `let` only:
      - *never use `var`*
    - Select DOM elements (aka "DOM Traversal") with `document.querySelector()` and `document.querySelectorAll()`:
      - *never use `document.getElementById()`, `document.getElementsByTagName()` wtc, or [jQuery](https://jquery.com)*
    - ES6 classes - at least 2 - put them in **classes.js**
 
2) Ajax
    - Use [`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) and [`fetch.then()`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
      - *do not use [`XHR`](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) or `await fetch(...)` or `jQuery.ajax()` with this project*

3) PHP
    - a PHP "wrapper" script to your web service is required
    - it must be run from the banjo web server

4) Other prohibited (in addition to what was mentioned above):
    - *inline event handlers - ex. `<button onclick="doStuff()">Do Stuff!</button>`*
    


<hr>

<a id="media"/>

## V. Media


