# Project 3 - *Interactive Sandbox of Awesomeness* - Overview & Tips

I. [Handy Links](#links)

II. [Executive Summary of Project](#summary)

III. [Checkpoint Feedback](#checkpoint-feedback)

IV. [AV Tips](#av-tips)

V. [Game Tips](#game-tips)

VI. [Resources](#resources)

<a id="links" />

<hr>

## I. Handy Links

- [Project 3 Requirements](project-3.md)
- [Project 3 Coding Standards](code-style.md)
- We will keep updating this page - so check back periodically!

<hr>

<a id="summary" />

## II. Executive Summary of Project

### II-A. Theme

- "*You will create a compelling interactive media experience that allows the user to explore a media-related theme (of your choice)*" - examples:
  - An audio visualizer - perhaps enhanced by user interaction via Teachable Machine --> https://teachablemachine.withgoogle.com/train
  - A game - *Cage Clicker* could be a good start on one --> https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-cage-clicker-1.md
  - A simulation:
    - Evolution - YouTube [Primer's Evolution Playlist](https://www.youtube.com/watch?v=oDvzbBRiNlA&list=PLKortajF2dPBWMIS6KF4RLtQiG6KQrTdB)
  - A Generative Art, Dynamical Systems or Emergence experience:
    - Here's a great blog post to give you some ideas --> https://www.artnome.com/news/2018/8/8/why-love-generative-art
    - More ideas --> [Intro to Creative Coding](https://github.com/mattdesl/workshop-p5-intro/blob/master/README.md)
    - Chaotic Systems --> see [HW - Lorenz Attractor](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-lorenz-attractor.md)
    - Periodic functions --> see [HW - Sine Wave](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-sine-wave.md)
    - Phyllotaxis --> see [HW - Algorithmic Botany](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-algorithmic-botany.md)
    - Conway's *Game of Life* --> see [HW - Life](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-canvas-life.md)
    - Reaction Diffusion --> RESOURCE: Coding Train [Coding Challenge #13: Reaction Diffusion Algorithm in p5.js](https://www.youtube.com/watch?v=BV9ny785UNc)
 
### II-B. Technologies
 - Must use:
   - JavaScript/ES6 Modules
   - Canvas
   - Bulma
   - Web Components
- Must have:
  - 3 HTML pages
    - about.html
    - app.html
    - documentation.html
  - 3 web components
    - One of these MUST be a global navigation component
  - multiple (at least 3) user interface *controls* and/or widgets so that the user can interact with the experience
  - app data loaded from a JSON file
    - rather than hard-coding values in your JS, data that your app depends on will be stored in a *local* JSON file (ex. **presets.json**, **levels.json** etc)
    - load this local data file via the `fetch()` API
    - see **presets-demo.zip** in myCourses
    - ex. The instructions for your game or experience
    - ex. Game Difficulty Settings (Easy/Normal/Impossible)
    - ex. Audio Visualizer Settings (slider positions, radio button and checkbox state)
    - ex. Conway's Game of Life patterns
 - Must demonstrate:
   - ***IMPACT*** and go beyond what we've done in class
   - The app must do something that would be meaningful to the user, allowing them to explore the chosen theme in a compelling way
   - The code & functionality must go significantly beyond any of the provided "starter" code above
   - The creator of this app should take this assignment seriously ("engage"!) and do their best work

<a id="checkpoint-feedback" />

<hr>

## III. General Checkpoint Feedback

### III-A. Go beyond the "starter" HW assignments

- ***show us what you can DO*** - you will only get project credit for code that ***you wrote***, which means that your projects MUST go well beyond any HW assignments or starter code
- ***don't overscope*** - a simple idea that is complete and well-executed often has more success than an elaborate idea which is only partially implemented

### III-B. Do not violate RIT's Academic Integrity Policy

- ***Cite ANY and ALL*** borrowed code fragments, resources, tutorials, YouTube videos, blogs, GitHub sites etc:
  - be sure to link to the actual page utilized, not just to an entire web site 
  - cite the resource on your project Documentation page AND
  - cite the resource as a code comment, right where you utilized it
  - you do not have to cite any code from the HW assignments

### III-C. How much time should you spend on this assignment?

- this is a ***project focused*** class with no quizzes or exams - project 3 is where you will demonstrate what you have learned this semester
- typically, weekly out of class work is expected to be 3 or 4 times total in-class hours - which works out to 8.5 to 10 hours a week
- allocating 3 weeks to the project (including the prototype) works out to roughly 25-30 hours of work in total
- you have nearly 2 weeks left


### III-D. Chrome Favicon Error Messages

- get rid of those annoying messages by adding a favicon to your site - https://favicon.io/emoji-favicons/


<a id="av-tips" />

<hr>

## IV. AV Tips

### IV-A. Creating reusable functions will help a lot

- DRY - multiple parts of your code can call these functions
- you can easily modify function parameters and test your ideas
- your UI can modify these function parameter values
- examples:

```js
function drawBars(ctx,audioData,barHeight=200,fillStyle="white", strokeStyle="black",lineWidth=1,numBars){
  ...
}

function drawLines(ctx,audioData,lineWidth=1,strokeStyle="white",magnitude=100,startIndex=0,endIndex){
  ...
}
```

### IV-B. You should go beyond squares, circles and rectangles

- Come up with different canvas drawing and bitmap effects than we did in the HW assignments - ***REMINDER: you will only get credit for code that you wrote*** 
    - the AV HW just used rectangles and circles (arcs) for drawing  - what else could you use?
    - lines with `moveTo()` and `lineTo()`
    - curves with 
- simple tinting and noise could be replaced with different bitmap effects
- emboss could be replaced with a different convolution effect

### IV-C. Sprites
 - Sprites - displayed with either canvas primitives or bitmap data - allow for experiences that are distict from the AV HW
   - see the Week 14 myCourses demo **filter-example-plus-wa.zip** (it utilizes sprites)

<a id="game-tips" />

<hr>

## V. Game Tips

<a id="resources" />

<hr>

## VI. Resources



