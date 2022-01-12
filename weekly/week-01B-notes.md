# Week 1B - Technobabble I & II & III

## I. Finish up 1A
- Questions on syllabus/course expectations?
- Finish up JS/DOM Review
- Review "Greeter":
  - CSS selectors
  - string concatenation v. template literals
  - did the page load?
    - `<script>` on bottom of page
    - `.onload` handler
    - external script file
    - `defer` or `type="module"`
  - `function` keyword v. functions assigned as values of variables (i.e. function *literals*)
  - default form values if the user doesn't type in a name
  - passing values to functions from event handlers (a "Say Goodbye" button calling an `updateOutput()` function - time allowing!)
  - adding a "last name" field (we'll let you do this for the checkoff)

<hr>

## II. Review Technobabble I
- [HW - Technobabble Generator](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble.md)
- review the 10 questions at the end of the HW
- did anyone do it their "own way" rather than the way we did it on the video?
- so many ways to handle "did the page load"?
  - move <script> tag to top and break the code
  - `window.onload` event handler to fix the code
  - move JS to an external file:
    - then add `type=module`
- event *handlers* v. event *listeners*
  - declared functions are “first-class data types” (can be assigned to variables, passed as parameters, returned from functions)
- code refactoring:
  - the `randomElement()` helper function got rid of a lot of duplicated code
  - advantages of using template strings over string concatenation
- quick demo:
  - move the code to an external JS file (done above)
  - move the CSS to an external CSS file
  - embed a font into the page (should be review from 235)

<hr>
  
## III. Start Technobabble II & III

- [HW - Technobabble Generator II](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-2.md) - improves the user experience, especially on mobile, let's go work on that now
- [HW - Technobabble Generator III](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-3.md) - adds a new button that appears only on larger screens - see the hints and screenshots - we'll let you do this one on your own

<!--
## I. Overview

- Welcome to day 2! 
- First we'll see if there are any questions about the Technobabble HW, and take a peek at a few submissions
- Then we will continue our review of basic JavaScript and the DOM, and cover the material in the 3rd and 4th videos from last time:
  - see the [Week 1A - JS review notes](week-01A-notes.md#js-review-notes)
  - and [Week 1A - JS review videos](week-01A-notes.md#js-review-video-links)
  - if we don't get to cover all of this material during the class time, you are expected to get this material by watching the video links at the bottom of this page
  - here is the start code for today's demo (and Homework)

**say-hello-2.html**
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Greeter</title>
    <style>
      *{font-size:1.5em;}
    </style>
  </head>
<body>
  <button>Click Me!</button>
  <input id="firstName" placeholder="Type in your name">
  <p id="output">???</p>
  <script>
    'use strict';
  </script>
</body>
</html>
```

<hr>

## II. Homework
- Easy!
- Take the final version of what we created in the last video (the **say-hello-3.html** file):
  - Change the "Click Me" button text to "Hello" 
  - Add a "Last Name" field the user can type into
  - When the user clicks the "Hello" button they will greeted with both their first and last name
  - If no value is entered for the "First Name", the default value will be "James"
  - If no value is entered for the "Last Name", the default value will be "Bond"
  - Add a second button with the text of "Goodbye"
  - When the user clicks the "Goodbye" button, it will function nearly identical to the "Hello" button, except it will display "Goodbye `<firstName>` `<lastName>`"
  - see myCourses dropbox for due date
  - Hints:
    - Because that you now have 2 buttons, you will need to give them unique `id` values
    - Don't forget that id selectors start with a `#`
    - Can you get this done with just *one* function that updates the `#output`, instead of *two*?
  - See screenshot below

<hr>

- Click the "Hello" button:

![screenshot](_images/1B-hello-goodbye-1.png)

<hr>

- Click the "Goodbye" button:

![screenshot](_images/1B-hello-goodbye-2.png)


-->


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-01A-notes.md**](week-01A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-02A-notes.md**](week-02A-notes.md)
