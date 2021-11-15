# Project 3 - *Interactive Sandbox of Awesomeness* - Overview & Tips

## Notes:

- [Project 3 Requirements](project-3.md)
- [Project 3 Coding Standards](code-style.md)
- We will keep updating this page - so check back periodically!

<hr>

## I. Executive Summary of Project

### I-A. Theme

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
 
### I-B. Technologies
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