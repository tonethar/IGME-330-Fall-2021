# Project 1 - Tips & Tricks

- [Project 1 Requirements](project-1.md)
- [Project 1 Coding Standards](code-style.md)
- We will keep updating this page - so check back periodically!

## I. Code Tips

### I-A. `loader.js`

- The "hamburger" code that was in **index.js** is something that every one of your P1 pages needs. You will need to convert this file over to an ES6 module for this project, which is easy! First, rename **index.js** to **loader.js**, and the make it look like this:

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

## II. Component Tips
