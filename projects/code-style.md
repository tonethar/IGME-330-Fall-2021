# IGME-330 - Course Code Style Requirements

- Although we won't be using a linter to check out JS code in this course, there are still benefits to having a clear code style:
  - https://guide.meteor.com/code-style.html

<hr>

## I. Web file naming conventions

- "web" file names (HTML/CSS/JS/images etc) will be in all lower case letters, with words separated by dashes:
  - example **user-form.html** is ok, **userForm.html** is NOT allowed
  - spaces are NOT allowed in file names - ex. **user form.html** or **user%20form.html** are NOT allowed
  - capital letters are NOT allowed anywhere in file name (ex. camel case not allowed)
  - exceptions:
    - ES6 class names may begin in an uppercase letter (ex. **Sprite.js**)
    - font file names may have uppercase latters
    
<hr>

## II. JavaScript

- declare variables with `const` & `let` only:
  - *NEVER* use `var` in this class
- function, variable, constant and function parameter *names* will begin in a lower case letter - ex. `function queryService()`, `const numSprites = 10`
  - the above also applies to ES6 class method names, and class method parameter names
  - object literal property names will also begin in a lower-case letter, and spaces in property names are not allowed
  - camel casing for all of the above - ex `btnSeach` IS allowed
- class names always begin in an uppercase letter - ex. `Class Sprite{}`
- code shall be consistently indented and "line up" so that it is readable:
  - you can use 2-spaces, 4-spaces, or tabs - it just has to be  *consistent* and *readable*

<hr>

## III. DOM Traversal

- Select DOM elements (aka "DOM Traversal") with `document.querySelector()` and `document.querySelectorAll()`:
  - *NEVER* use `document.getElementById()`, `document.getElementsByTagName()` etc, or *jQuery* in this class
- Hooking up events:
  - *Event listeners* (ex. `myButton.addEventListener("click",doStuff)`) and *Event Handlers* (ex. `myButton.onclick = doStuff)`) are both allowed
  - NEVER use inline event handlers in the HTML - ex. `<button onclick="doStuff()">Click Me</button>`
