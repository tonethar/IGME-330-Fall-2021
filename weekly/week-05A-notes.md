# Week 5A - Finish up (mostly) Web Components

## I. Review
- 4B Breakout Activity - Counters of Awesomeness (Instructions in myCourses)
- Project 1

<hr>

## II. Lecture/HW Notes
- [Web Components-4 - Walk through a `<my-list>` web component](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-4.md):
  - this is pretty straightforward, and there isn't a HW assignment associated with it, so we will cover it first
- [HW - Web Components-3 - Build a component driven web app](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-3.md):
  - the code is a little more elaborate, and there's a HW  assignment
<!-- - Web Components-5: web components and custom events -->

<hr>

## III. Demo
- Can you put Web Components *inside* of other Web Components?
  - You betcha!
  - Demo `<sw-app>`:
    - we get rid of **main.js**, and move all if the app functionality into `<sw-app>`
    - we also move the ajax code to **utils.js**:
      - we need to **`export`** `loadFile()` from **utils.js**
      - we need to **`import`** `loadFile()` into **sw-app.js** 

**sw-web-app.html**
```html
<body>
<sw-app></sw-app>
</body>
```

**sw-app.js**
```html
import "./sw-header.js";
import "./sw-card.js";
import "./sw-footer.js";
import {loadFile} from "./utils.js";

const template = document.createElement("template");
template.innerHTML = `
<style>
...
</style>
<sw-header data-title="Star Wars Character Finder"></sw-header>
<main>
  <select id="character-select"></select>
  <hr>
  <div class="card-list"></div>
</main>
<sw-footer data-title="Ace Coder" data-year="2021"></sw-footer>
`;

class SWApp extends HTMLElement{
  constructor(){
    super();
    ...
}
```




<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-04B-notes.md**](week-04B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-05B-notes.md**](week-05B-notes.md)  
