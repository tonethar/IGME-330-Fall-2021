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

- You will create a compelling interactive media experience that allows the user to explore a media-related theme (of your choice):
  - It should be (or approaching) "portfolio quality" - something you would not be embarrassed to show a potential employer
  - Let's call the above bullet point "Impact" - which is what your app should have
  - Ideally the experience will run in all modern browsers, but at a bare minimum it must run in recent versions of Chrome.
  - The objective of this project is for you to demonstrate your mastery of HTML5/CSS/JS/Canvas "rich media" programming in a web browser context
  - You will be evaluated on:
    - the quality of the experience you create
    - the soundness of your programming
    - meeting the requirements detailed below
    - how far you went beyond what we did in class, as described below
  - Also see:
    - [Project 3 - Interactive Sandbox of Awesomeness - Overview & Tips](p3-overview-and-tips.md)
    - [IGME-330 - Course Code Style Requirements](code-style.md)

<hr>

<a id="structure"/>

## II. Structure

1) 3 distinct web pages:
    - About (**home.html** or **about.html**) - a "landing" page that tells the users what the app can do
    - App  (**app.html**) - the main functionality of your app 
    - Sources (**documentation.html** or **sources.html**) - documentation of your sources and a link to your demo video

2) A **src** folder

3) A **styles** folder

4) You might also have **fonts/**, **images/** or **data/** or **src/components/** folders


<a id="design-interaction" />

<hr>


## III. Design & Interaction (*All pages*)

1) Global Navigation System:
    - has "you are here" cues for each page 
    - implemented with [Bulma](https://bulma.io/)
    - is a Web Component

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
- *Optional: Consider adding some sort interactive content or "flair" to this page - an image carousel, random quotes from happy users, etc*

<a id="page-documentation"/>

### IV-B. Content Requirements (*Documentation page*)

- Have the following sub-headings on your page (see the [example Desktop screenshots of sources.html](#desktop-screenshots) below
  - **PROJECT REQUIREMENTS**:
    - provide a link to this page
  - **RESOURCES UTILIZED**:
    - cite any and all resources you used on this project, the specific link, including:
      - fonts and images
      - reference sites - ex. developer.mozilla.org
      - "help" sites - ex. stackoverflow.com
      - code snippet sites - ex. CodePen or gists.github.com or copying starter code from the Bulma site etc
      - tutorial sites - ex. w3schools.com
      - video sites - ex. YouTube or LinkedIn Learning or Udemy
      - blog postings
      - GitHub sites
      - etc
    - Exception: you need not cite any IGME-330 resources/tutorials/HWs:
      - but you MUST cite resources from other courses including IGME-235 
  - **JS LIBRARIES** (if applicable):
    - Link to each library's home page
  - **NOTEWORTHY**:
    - Talk the project up - list the technologies you used (web components, Bulma, fetch, promises, canvas, specific JS libraries etc)
    - Be sure to emphasize what you did outside of what we covered in class
  - **GRADING**
    - Describe how you met project requirements
    - Describe how you went "above and beyond" project requirements
    - But don't self-grade your project here, or ask for a particular grade
    - In the comments field of the dropbox, ***DO be sure to self-grade your Project 3 submission***
  - **TO DO**
    - List any features that you would have liked to add to the app if you had time, or might add in the future

<a id="functionality"/>

<hr>

## V. Sandbox App Functionality & User Experience (*App page*)

### V-A. Themes
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
    - See [Project 3 Overview & Tips - AV Tips](p3-overview-and-tips.md#av-tips)
  <a id="game" />
  
  - **Game?**
    - An interactive game, most likely in the "casual" genre, is also acceptable as a project
    - *Cage Clicker* could be a good starter -  https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-cage-clicker-1.md
    - See [Project 3 Overview & Tips - Game Tips](p3-overview-and-tips.md#game-tips)

<hr>

### V-B. Functional Requirements

- multiple (at least 3) user interface *controls* and/or widgets so that the user can interact with the experience
- app data loaded from a JSON file
  - rather than hard-coding values in your JS, data that your app depends on will be stored in a JSON file (ex. presets.json, levels.json etc)
  - load this data via the `fetch()` API
  - see **presets-demo.zip** in myCourses:
  - ex. Game Difficulty Settings (Easy/Normal/Impossible)
  - ex. Audio Visualizer Settings (slider positions, radio button and checkbox state)
  - ex. Conway's Game of Life patterns


<hr>

### V-C. Impact

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



<a id="code" />

<hr>

## VI. Code

1) Code style/standards - [IGME-330 - Course Code Style Requirements](./code-style.md)
    - ES6 modules - multiple distinct code files in a **src** folder - ex. **src/app.js**, **src/favorites.js**, **src/loader.js**, **src/my-component.js**:
      - *each component gets its own JS file*
      - *No JS code is allowed in your HTML file*
        - Instead, use a `<script>` element to load in the JS code you wrote - ex. `<script src="src/app.js" type="module"></script>`
      - your modules will use the [`import`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) and/or [`export`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) keywords as needed
 
2) Ajax
    - Use [`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) to load app data (see **presets-demo.zip** in myCourses):
      - you may use `.then()` or `await` according to your preference
      - you MUST handle errors with either `.catch()` or `try/catch`
      - *do NOT use `XHR` or `jQuery.ajax()` with this project*

3) Utilize at least 3 [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components) classes in your project

    
<hr>

<a id="media"/>

## VII. Media
- Must use the [Bulma](https://bulma.io/) CSS framework
- Procedural drawing by *directly accessing* the [CanvasRenderingContext2D](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D) that we have been utilizing in class is required. (Processing, Pixi.js, WebGL *et al* are NOT allowed):
  - canvas methods must be used to draw rectangles, lines, arcs, curves, images and so on depending on the needs of your project
  - `ctx.save()` and `ctx.restore()` MUST be used frequently/where appropriate (for example, in functions that modify the drawing state in some way)
  - `ctx.translate()`, `ctx.rotate()`. and `ctx.scale()` will probably be used
  - avoid using canvas convenience methods such `ctx.fillRect()` and `ctx.strokeRect()`
- All pages must pass HTML Validation
- All pages must pass CSS Validation
- Images optimized:
  - jpeg,gif,png only
  - scaled down to appropriate dimensions for web delivery
  - *for example, a not cropped or scaled 12MP 4032 x 3024 image is too big, and not allowed*


<a id="video"/>

<hr>

## VIII. Demo Video

- A 1 to 2-minute narrated "demo reel" of the completed project is required
- Post it to YouTube & put the URL in the dropbox comments field
- If you decide to upload a video file instead, it MUST be in the MP4 format
- The easiest way to record a demo reel is to use Zoom - here is a 2-minute video on how to do this: https://www.youtube.com/watch?v=D617OXKhSYw
  - another popular option for creating videos is [OBS](https://obsproject.com/download)
  - don't forget to "Share Screen" so that I can see you interacting with the project
  - don't forget to record your narration too, and try to use a better microphone than the one that came with your laptop `:-)`
- Please don't stress out over this requirement - I am the only one who will see the video - I won't be sharing or posting these
- **10% deducted from project grade if this video requirement is not completed, -5% if I cannot hear or understand you**



<a id="rubric" name="rubric" />


<hr>

## IX. Grading Rubric


Your project will be graded on the following criteria:

| Criteria | Weight | Your Score |
| -------- | ------ | ---------- |
| **A. Overall Theme/Impact** | **50** | |
|    1. Does the app have an coherent and identifiable theme?
|    2. Does the app work as intended and it is reasonably engaging (both visually and otherwise)?  | |
|    3. Does the app have the required controls. Are the widgets well labeled and follow interface conventions? | |
|    4. Are users able to figure out how to use the app on their own? | |
|    5. Is the *state* the application is in obvious? | |
|    6. Does the app run without errors? | |
|    7. Does the app functionality and programming go beyond what we did in class? | |
|    8. Is the app at least approaching/approximating "portfolio quality" that you would not hesitate to show a potential employer?  | |
|    **Overall:** Excellent/Outstanding/"Wow" (A+ = 50/50), Very Good (A = 45/50), Good (35-40/50), Fair (25-35/50), Poor (15-25/50), Unacceptable (0-15/50) ||
| &nbsp; | &nbsp; |
| **B. Site Navigation & Content** | **20** | |
|    1. Required content is present on [Home](#iv-a-content-requirements-home-page) & [Documentation](#iv-b-content-requirements-documentation-page) Pages | |
|    2. Global Navigation System with "you are here" cues for each page | |
|    3. Bulma is utilized effectively
|    4. "Mobile Friendly" with Hamburger menu
| &nbsp; | &nbsp; |
| **C. [HTML/CSS/Media](#media)**  | **10** | |
|    1. Valid HTML | |
|    2. Valid CSS | |
|    3. Images properly optimized | |
|    - *Fails HTML Validation* | *(-5)* |
|    - *Fails CSS Validation* | *(-5)* |
|    - *Most CSS is NOT in an external stylesheet* | *(-5)* |
|    - *Images larger than 100KB* | *(-2 each)* |
| **D. [Code](#code)**  | | |
|    - *ES6 Module pattern not used* | *(-20)* |
|    - *App data not loaded from external file* | *(-10)* |
|    - *[Course Code Standards](code-style.md) NOT followed* | *(-1 to -5 per incident)* |
|    - *Code shows errors in console* | *(-5 per incident)* |
|    - *App does not function on banjo and/or locally* | *(-10 to ?)* |
|    - *App has fewer than 3 web components* | *(-5 each)* |
|    - *Web component NOT in its own JS file* | *(-5)* |
| **Maximum Possible Total Points** | **100** | |
| **Deductions** | **&darr; Don't lose points for any of these! &darr;** | |
| *Deduction if required prototype was not submitted to dropbox on time* | *(-10)* | |
| *Deduction if video is not submitted to dropbox on time* | *(-10)* | |
