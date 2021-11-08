# Project 3 - *Interactive Sandbox App of Awesomeness* - DRAFT

[I. Overview](#overview)

[II. Structure](#structure)

[III. Design & Interaction (*All pages*)](#design-interaction)

[IV. Content](#content)

- [Home Page](#page-home)
- [Documentation Page](#page-documentation)

[V. Sandbox App Functionality & User Experience](#functionality):

[VI. Code](#code)

[VII. Media](#media)

[VIII. Demo Video](#video)

[IX. Rubric](#rubric)

<a id="overview"/>

<hr><hr>

## I. Overview

- You will create a compelling interactive media experience that allows the user to explore a media-related theme (of your choice)
  - It should be (or approaching) "portfolio quality" - something you would not be embarrassed to show a potential employer
  - Let's call the 3 lines above "Impact" - which is what your app should have
  - Ideally the experience will run in all modern browsers, but at a bare minimum it must run in recent versions of Chrome.
  - The objective of this project is for you to demonstrate your mastery of HTML5/CSS/JS/Canvas "rich media" programming in a web browser context
  - You will be evaluated on:
    - the quality of the experience you create
    - the soundness of your programming
    - meeting the requirements detailed below
    - how far you went beyond what we did in class, as described below

<hr>

<a id="structure"/>

## II. Structure

1) 3 distinct web pages
    - About (**home.html** or **about.html**) - a "landing" page that tells the users what the app can do
    - App  (**app.html**) - the main functionality of your app 
    - Sources (**documentation.html** or **sources.html**) - documentation of your sources and a link to your demo video

2) A **src** folder

3) A **styles** folder

4) You might also have **fonts/**, **images/** or **data/** or **src/components/** folders


<a id="design-interaction" />

<hr>


### III. Design & Interaction (*All pages*)

1) Global Navigation System with "you are here" cues

2) Pleasing graphic design:
    - must use the [Bulma](https://bulma.io/) CSS framework
    - must be mobile friendly (Bulma does this by default)
    - an *embedded* font must be used - for example from https://fonts.google.com:
      - be cautious about using an ornamental or cursive embedded font for UI labels
      - instead, utilize the embedded font on ornamental elements, like a title or copyright notice
    
3) Widgets are well labeled and follow interface conventions, for example:
    - radio buttons are for mutually exclusive options, checkboxes are for when you want to let the user choose *multiple* options --> https://delib.zendesk.com/hc/en-us/articles/203430309-Radio-button-vs-checkbox-what-s-the-difference-
    
4) Users must be able to figure out how to use the app with minimal instruction:
    - be sure to provide instruction and tooltips if necessary
    
5) User errors must be handled gracefully:
    - for example, if the user forgets to type in a search term before clicking the Search button, the app should tell the user something like "Please enter a search term first"
    
6) Users must know what *state* the app is in at all times
      
<a id="content"/>

<hr>

## IV. Content Requirements

<a id="page-home"/>

### IV-A. Content Requirements (*Home page*)

- Tell the user what your Interactive Sandbox App does
- Have some sort of "brand" for your page:
  - it could be a `navbar-brand` like in the Bulma template - an image or font awesome icon
  - it could be a stylized logo you create yourself
- You might want to use a Bulma `hero`
- There must be at least one image on this page (in addition to whatever appears in `navbar-brand`)
- *Optional: Consider adding some sort interactive content or "flare" to this page - an image carousel, random quotes from happy users, etc*

<a id="page-documentation"/>

### IV-B. Content Requirements (*Documentation page*)

- Have the following sub-headings on your page (see the [example Desktop screenshots of sources.html](#desktop-screenshots) below
  - PROJECT REQUIREMENTS:
    - provide a link to this page
  - RESOURCES UTILIZED:
    - cite any and all resources you used on this project, the specific link, including:
      - fonts and images
      - reference sites - ex. developer.mozilla.org
      - "help" sites - ex. stackoverflow.com
      - code snippet sites - ex. CodePen or gists.github.com or copying starter code from the Bulma site etc
      - tutorial sites - ex. w3schools.com
      - video sites - ex. YouTube or LinkedIn Learning or Udemy
      - blog postings etc
    - Exception: you need not cite any IGME-330 resources/tutorials/HWs:
      - but you MUST cite resources from other courses including IGME-235 
  - API:
    - Link to the API Home, documentation, and endpoints used (but don't include your API key!)
  - NOTEWORTHY:
    - Talk the project up - list the technologies you used (web components, Bulma, fetch, promises, etc)
    - Be sure to emphasize what you did outside of what we covered in class
  - GRADING
    - Describe how you met project requirements
    - Describe how you went "above and beyond" project requirements
    - In the comments field of the dropbox, grade your Project 1 submission
  - TO DO
    - List any features that you would have liked to add if you had time
    - These could potentially be added to the app for Project 2, or over break/summer when you have time

<a id="functionality"/>

<hr>

## V. Sandbox App Functionality & User Experience (*App page*)

- Explore **one** of the *themes* that we covered in class:
  - *Dynamical Systems*:
    - Chaotic Systems --> see [HW - Lorenz Attractor](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-lorenz-attractor.md)
    - Periodic functions --> see [HW - Sine Wave](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-sine-wave.md)
    - Phyllotaxis --> see [HW - Algorithmic Botany](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-algorithmic-botany.md)
  - *Emergence*:
    - Conway's *Game of Life* --> see [HW - Life](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-canvas-life.md)
    - Reaction Diffusion --> RESOURCE: Coding Train [Coding Challenge #13: Reaction Diffusion Algorithm in p5.js](https://www.youtube.com/watch?v=BV9ny785UNc)
  - **OR** ??? (getting permission in advance is required) - here are some ideas:
    - Evolution - YouTube [Primer's Evolution Playlist](https://www.youtube.com/watch?v=oDvzbBRiNlA&list=PLKortajF2dPBWMIS6KF4RLtQiG6KQrTdB)
    - Economic - YouTube [Primer's Economics Playlist](https://www.youtube.com/watch?v=PNtKXWNKGN8&list=PLKortajF2dPCAHWOVNqWY2DSEdoyyj1eV)
    - Generative Art - here's a great blog post to give you some ideas --> https://www.artnome.com/news/2018/8/8/why-love-generative-art
    - Particle systems/falling sand app: 
      - https://github.com/pineapplemachine/websand
      - https://modernweb.com/creating-particles-in-html5-canvas/  (BUT, you will need to convert this code to ES6 classes)
    - https://medium.com/better-programming/heres-what-i-learned-from-30-days-of-creative-coding-a-codevember-retrospective-8c05a8497d24
    - [Intro to Creative Coding](https://github.com/mattdesl/workshop-p5-intro/blob/master/README.md)
    - Shiffman, of course: https://www.youtube.com/user/shiffman/featured
  - *Sprites* - do you need sprites for your Project? - [canvas-6.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-6.md) might help!
  - **Audio Visualizer?**
    - See the myCourses dropboxes for a 3-part "starter":
      - https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-2195-1.md
      - https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-2195-2.md
      - https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-AV-2195-3.md
      - https://github.com/tonethar/IGME-330-Master/blob/master/notes/web-audio-visualizer-home.md
  
  <a id="game" />
  
  - **Game?**
    - An interactive game, most likely in the "casual" genre, is also acceptable as a project
    - *Cage Clicker* could be a good starter -  https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-cage-clicker-1.md
    - We like this definition of a game:
        - *"A game is a series of interesting choices"* - https://en.wikiquote.org/wiki/Sid_Meier - and you should strive to give your players some - examples:
          - *"When should I use one of my limited supply of  smart bombs to clear the screen?"*
          - *"Do I try to grab the powerup, or avoid that projectile?"*
          - *"Should I build a farm, or wait to save up enough to build a factory?"*
    - Other elements found in fun games you will probably have in yours:
      - A difficulty level that's not too hard, nor too easy
      - Score
      - Levels
      - Satisfying user control with mouse and/or keyboard (see 235 "Key Daemon" aka [Smooth Keyboard Control](https://github.com/tonethar/IGME-235-Shared/blob/master/tutorial/pixi-js-0.md#vi-demos) demo)
      - *Feedback loops* that change the flow of the gameplay - https://learn.canvas.net/courses/3/pages/level-4-dot-4-feedback-loops
      - *Emergent gameplay/complexity* (i.e. the players *learning* something that can improve their level success in the game) - https://learn.canvas.net/courses/3/pages/level-4-dot-5-emergence
- *Impact:*
  - This app is an *interactive sandbox*, similar to a physical sandbox where the user can experiment, create and destroy with no given objective.
    - or if adding game elements, be sure that the controls allow for the player to control the elements of the game to the greatest reasonable degree, possibly allowing for "options" in the way that the game can be played (for example, adjusting difficulty with a slider).
  - The app must do something that would be meaningful to the user, allowing them to explore the chosen theme in a compelling way
  - The code & functionality must go significantly beyond any of the provided "starter" code above
  - The creator of this app should take this assignment seriously ("engage"!) and do their **best work**
  - Here are some examples of the reverse (e.g. these are *counter examples* to be avoided):
    - not implementing specific requirements in the [rubric](#rubric) below
    - barely meeting "the minimum" on many elements of the rubric - for example:
      - writing *exactly* 3 utility functions
      - creating *exactly* 3 controls
      - using *exactly* 3 semantic HTML elements
      - having *exactly* 5 CSS style rules 
      - and so on, rather than letting the amount of these to be driven by what the app requires to work well and look good
    - copying/pasting CSS styles and layout from the demos and exercises, rather than creating their own
    - minimal modification/extension of the in-class code that was provided


<hr>

### V-A. Functional Requirements 

1. On the app page, you WILL automatically save the last term searched by the user and other UI *state* in the browser's local storage - this was covered in IGME-230/235 here --> [Web Apps 9 - WebStorage API](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-9.md):
    - this will also be true of the other controls on the page (&lt;select> tags, radio buttons, checkboxes etc)
    - we are going to test this capability by typing in a search term, selecting some checkboxes, doing a search, and then closing the browser window. When we re-open the window, the user's last search term must be visible, and the rest of the UI should be in the same *state*
    - ***\*THIS REQUIREMENT HAS BEEN DEFERRED TO [PROJECT 2](project-2.md)\****

2. Other required controls - there WILL be a MINIMUM of 3 controls that a user can use to affect the experience
<hr>


<a id="code" />

## VI. Code

1) Code style/standards - [IGME-330 - Course Code Style Requirements](./code-style.md)
    - ES6 modules - multiple distinct code files in a **src** folder - ex. **src/app.js**, **src/favorites.js**, **src/loader.js**, **src/my-component.js**:
      - *each component gets its own JS file*
      - *No JS code is allowed in your HTML file*
        - Instead, use a `<script>` element to load in the JS code you wrote - ex. `<script src="src/app.js" type="module"></script>`
      - your modules will use the [`import`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) and/or [`export`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) keywords as needed
 
2) Ajax
    - Use [`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API):
      - you may use `.then()` or `await` according to your preference
      - you MUST handle errors with either `.catch()` or `try/catch`
      - *do NOT use `XHR` or `jQuery.ajax()` with this project*

3) `localStorage` - you have already done this in IGME-235 - [9 - WebStorage API](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-9.md)

4) Utilize at least 3 [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components) classes in your project

    
<hr>

<a id="media"/>

## VII. Media
- Procedural drawing via the [CanvasRenderingContext2D](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D) that we have been utilizing in class is required. (Processing, Pixi.js, WebGL *et al* are NOT allowed):
  - canvas methods must be used for rectangles, arcs and lines
  - `ctx.save()` and `ctx.restore()` must be used
  - avoid using canvas convenience methods such `ctx.fillRect()` and `ctx.strokeRect()`
- HTML Validation
- CSS Validation
- Images optimized:
  - jpeg,gif,png only
  - scaled down to appropriate dimensions for web delivery
  - *for example, a not cropped or scaled 12MP 4032 x 3024 image is too big, and not allowed*
 - Uses the [Bulma](https://bulma.io/) CSS framework

<a id="video"/>

<hr>

## VIII. Demo Video

- A 1 to 2-minute narrated “demo reel” of the completed project is required
- Post it to YouTube & put the URL in the dropbox comments field
- If you decide to upload a video file instead, it must be in the MP4 format
- The easiest way to record a demo reel is to use Zoom - here is a 2-minute video on how to do this: https://www.youtube.com/watch?v=D617OXKhSYw
  - another popular option for creating videos is [OBS](https://obsproject.com/download)
  - don't forget to "Share Screen" so that I can see you interacting with the project
  - don't forget to record your narration too, and try to use a better microphone than the one that came with your laptop `:-)`
- Please don't stress out over this requirement - I am the only one who will see the video - I won't be sharing or posting these
- **10% deducted from project 1 grade if this video requirement is not completed**



<a id="rubric" name="rubric" />


<hr>

## IX. Grading Rubric


Your project will be graded on the following criteria:

| Criteria | Weight | Your Score |
| -------- | ------ | ---------- |
| **A. [Functionality - App & Favorites Pages](#functionality)** | **40** | |
|    1. [App Page](#page-app) implements all required functional requirements
|    2. App Page saves/restores last search term and other UI *state* (DEFERRED TO [P2](project-2.md))  | |
|    3. App Page has other required controls | |
|    4. [Favorites Page](#page-favorites) uses local storage to display favorites  | |
|    5. Favorites Page has required "Delete Button"  | |
|    - *Web Service does not work (App Page)* | *(-30)* |
|    - *Does not save/restore UI state (App Page) (DEFERRED TO [P2](project-2.md))* | *(-10)* |
|    - *Missing required # of controls (App Page)* | *(-10 each)* |
|    - *Favorites not stored in localstorage (Favorites Page)* | *(-15)* |
|    - *Missing Favorites "Delete" button (Favorites Page)* | *(-5)* |
| **B. [Content - Home & Documentation Pages](#)** | **10** | |
|    1. Required content is present on [Home](#page-home) & [Documentation](#page-documentation) Pages | |
| **C. [Design & Interaction](#page-design-interaction)** | **20** | |
|    1. Global Navigation System with "you are here" cues: | |
|    2. Pleasing graphic design (embedded font, Bulma, mobile friendly) | |
|    3. Widgets are well labeled and follow interface conventions | |
|    4. User errors must be handled gracefully | |
|    5. Users must be able to figure out how to use the app with minimal instruction | |
|    6. The *state* the application is in is obvious | |
|    - *Missing "state" cues like status text or "spinners"* | *(-5)* |
|    - *Missing embedded font* | *(-5)* |
|    - *Bulma not used or utilized ineffectively* | *(-20/-?)* |
|    - *Interface looks "amateurish"  or like GIF Finder HW* | *(up to -15)* |
|    - *Widgets NOT well labeled/do not follow interface conventions* | *(-?)* |
|    - *User errors NOT handled gracefully* | *(-?)* |
|    - *App NOT intuitive to use* | *(-?)* |
|    - *App state NOT obvious* | *(-?)* |
| **D. [HTML/CSS/Media](#media)**  | **10** | |
|    1. Valid HTML | |
|    2. Valid CSS | |
|    3. Images properly optimized | |
|    - *Fails HTML Validation* | *(-5)* |
|    - *Fails CSS Validation* | *(-5)* |
|    - *Most CSS is NOT in an external stylesheet* | *(-5)* |
|    - *Images larger than 100KB* | *(-2 each)* |
| **E. [Code](#code)**  | | |
|    - *ES6 Module pattern not used* | *(-20)* |
|    - *`fetch()` not used* | *(-20)* |
|    - *Code Conventions NOT followed* | *(-1 to -5 per incident)* |
|    - *Code shows errors in console* | *(-5 per incident)* |
|    - *App does not function on banjo and/or locally* | *(-10 to ?)* |
|    - *App has fewer than 3 web components* | *(-5 each)* |
|    - *Web component NOT in its own JS file* | *(-5)* |
| **F. [Impact](#)**  | **20** | |
|    - If the app meets the requirements above, we will award a 10% in this category, which means the base overall grade is 90% | |
|    - *App functionality and programming goes beyond what we did in class* | *(+1 to +10)* |
|    - *App UI design goes beyond what we did in class* | *(+1 to +10)* |
|    - *App is "portfolio quality" (or nearly so)* | *(+1 to +10)* |
| **Maximum Possible Total Points** | **100** | |
| **Deductions** | **&darr; Don't lose points for any of these! &darr;** | |
| *Deduction if required prototype was not submitted to dropbox on time* | *(-10)* | |
| *Deduction if video is not submitted to dropbox on time* | *(-10)* | |
