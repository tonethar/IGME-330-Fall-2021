# IGME-330 - Course Code Style Requirements

## I. Web file naming conventions

- "web" file names (HTML/CSS/JS/images etc) will be in all lower case letters, with words separated by dashes:
  - example **user-form.html** is ok, **user-form.html** is NOT allowed
  - spaces are not allowed in file names - ex. **user form.html** or **user%20form.html** is NOT allowed
  - capitals not allowed anywhere in file name (ex. camel case not allowed)
  - exceptions:
    - ES6 class names may begin in an uppercase letter (ex. **Sprite.js**)
    - font file names may have uppercase latters
    
<hr>

## II. JavaScript

- declare variables with `const` & `let` only:
  - *never use `var`* in this class
- function and variable and constant names will begin in a lower case letter - ex. `function queryService()`, `const numSprites = 10`
  - camel casing - ex `btnSeach` IS allowed
- class names always begin in and uppercase letter - ex. `Class Sprite{}`

<hr>

## III. DOM Traversal

- Select DOM elements (aka "DOM Traversal") with `document.querySelector()` and `document.querySelectorAll()`:
  - *never use `document.getElementById()`, `document.getElementsByTagName()` etc, or *jQuery* in this class
- Hooking up events:
  - *Event listeners* (ex. `myButton.addEventListener("click",doStuff)`) and *Event Handlers* (ex. `myButton.onclick = doStuff)`) are both allowed
  - NEVER use inline event handlers in the HTML - ex. `<button onclick="doStuff()">Click Me</button>`
