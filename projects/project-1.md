# Project 1 - *VanillaJS App of Awesomeness* (DRAFT)

[I. Overview](#overview)

[II. Structure](#structure)

[III. Functionality & User Experience](#functionlaity)

[IV. Code](#code)

[V. Media](#media)

[VI. Examples](#examples)

<!--

[VII. Rubric](#rubric)

[VIII. Documentation & Submission](#submission)

-->

<a id="overview"/>

<hr><hr>

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

<a id="structure"/>

## II. Structure

1) 4 distinct web pages
    - About (**about.html**)
    - App  (**app.html**)
    - Favorites (**favorites.html**)
    - Sources (**sources.html**)

2) A **src** folder

3) A **styles** folder

<hr>

<a id="functionality"/>

## III. Functionality

<hr>

<a id="code"/>

## IV. Code

1) Code style/standards - [IGME-330 - Course Code Style Requirements](./code-style.md)
    - ES6 modules - at least 4 distinct code files in a **src** folder - ex. **src/loader.js**, **src/main.js**, **src/utils.js**, **src/classes.js**:
      - *No JS code is allowed in your HTML file*
      - Instead, use a single `<script>` element to load in the JS code you wrote - ex. `<script src="src/loader.js" type="module"></script>`
      - your modules will use the [`import`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) and/or [`export`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) keywords as needed
    - ES6 classes - at least 2 - put them in **classes.js**
    - Functions
    - Arrays
 
2) Ajax
    - Use [`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) and [`fetch.then()`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch):
      - you may use `.then()` or `await` according to your preference
      - you MUST handle errors with either `.catch()` or `try/catch`
      - *do NOT use `XHR` or `jQuery.ajax()` with this project*

3) PHP
    - a PHP "wrapper" script to your web service is required
    - it must be run from the banjo web server
    - it will accept at least 2 GET parameters (ex. **taco-finder-proxy.php?type=fish&limit=10&location=Rochester,NY**)

4) localStorage - you have already done this in IGME-235 - [9 - WebStorage API](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-9.md)

5) Utilizes at least 2 [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components)

6) Code Validation:
    - ESLint validation required

7) Other prohibited (in addition to what was mentioned above):
    - *inline event handlers - ex. `<button onclick="doStuff()">Do Stuff!</button>`*
    
<hr>

<a id="media"/>

## V. Media

- HTML Validation
- CSS Validation
- Images optimized:
  - jpeg,gif,png only
  - scaled down to appropriate dimensions for web delivery
  - *for example, a not cropped or scaled 12MP 4032 x 3024 image is too big, and not allowed*
 - Uses the [Bulma](https://bulma.io/) CSS framework

<a id="examples"/>

<hr>

## VI. Example Screenshots

### VI-A. Desktop Version

**about.html**

![screenshot](_images/p1-desktop-ss-1.png)

**app.html**

![screenshot](_images/p1-desktop-ss-2.png)

**favorites.html**

![screenshot](_images/p1-desktop-ss-3.png)

**sources.html**

![screenshot](_images/p1-desktop-ss-4.png)

<hr>

### VI-B. Mobile Version

**about.html**

![screenshot](_images/p1-mobile-ss-1.png)

**app.html**

![screenshot](_images/p1-mobile-ss-2.png)

**favorites.html**

![screenshot](_images/p1-mobile-ss-3.png)

**sources.html**

![screenshot](_images/p1-mobile-ss-4.png)




