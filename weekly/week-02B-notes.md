
# Week 2B - Review of TB-2 & TB-3 and XHR

## I. Review the HW
- [Technobabble II](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-2.md)
  - Any questions?
- [Technobabble III](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-3.md)
  - Media queries (CSS `display` property)
  - Creating one function that will be called by both buttons (need to pass parameters from an event handler)
- Ajax HW
  - [HW - Ajax-1 - loading and parsing text files](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-1.md)
    - When would you ever load unstructured text?
      - Most commonly, as HTML fragments
    - Let's look at the "HTML creation" code - both the "long way" and the "one-liner"
  - [HW - Ajax-2 - loading and parsing CSV files](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-2.md)
    - When would you ever use a CSV file?
      - when working with large amounts of data, it is very common to export it from a spreadsheet and save it as CSV
      - when the data set is large, keeping data locally as CSV can be much more efficient than hitting up (for example) a web service repeatedly
    - look at array [destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)

<hr>

## II. Upcoming Homework
- You should complete these in the order below (due with a week, prior to start of class 3B):
  - [HW - Technobabble Generator IV - CSV](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-4.md)
  - [HW - Ajax-3 - loading and parsing XML files](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-3.md)
  - [HW - Technobabble Generator V - XML](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-5.md)
  - [HW - Ajax-4 - loading and parsing JSON files](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-4.md)
  - [HW - Technobabble Generator VI - JSON](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-6.md)

<hr>

## III. Breakout Groups

- Your mission (with a partner) is to write code that follows the **DRY** software development principle:
  - Clicking the "Load Taffy Info" button in the screenshot below will load and display the contents of the **taffy-facts.txt** file
  - Clicking the "Load Viking Info" button will load and display the contents of the **viking-facts.txt** file
  - You will create a `loadTextXHR()` helper function named that accepts 2 parameters - `url` and `callback`
    - `url` is the path to the file you want to download with `XHR`
    - `callback` is the function you want to have called when the file has downloaded. This callback function will update the appropriate part of the page with the downloaded HTML fragment
  - the two buttons in the screenshot below are both calling the same `loadTextXHR()` function, but passing in different values for the 2 parameters


<hr>

### III-A. Screenshot of completed version

- Here we are using the Bulma CSS framework - https://bulma.io/documentation/

<hr>

![screenshot](../_images/HW-xhr-helper-function.png)

<hr>

### III-B. Start Files

- See myCourses!

<!--
- Any questions?
  - You all just finished [Core Skills #4](https://github.com/tonethar/IGME-330-Master/blob/master/notes/4-adding-controls.md) (Controls: Button, checkbox, mouse clicking on the canvas):
    - another new thing was `ctx.save()` and `ctx.restore()` - and you will see how usefull these are next week when we cover canvas transformations (translate, rotate, scale)
    - Let's look at how to fix the "Play Button Spamming" issue
  - [Core Skills #5](https://github.com/tonethar/IGME-330-Master/blob/master/notes/5-write-some-code.md):
    - is due soon
    - mostly about adding more controls and helper functions, re-factoring the code, D.R.Y.
    - allows you to demonstrate your understanding of what we've done so far
    - don't put this off until the last minute
- Let's look at some more canvas - [canvas-2.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-2.md)
- Finish up *Shape Viewer*
- Preview of Next week:
  - canvas transformations, drawing gradients
  - procedurally drawing flowers - Phyllotaxis



# Week 2B - Periodic Functions & Algorithmic Botany



## I. Overview
Topics:
- Review the *SG-1* HW
- Look at how to draw Sine waves using canvas
- Get you started on Algorithmic Botany (Phyllotaxis)



## II. Presentation



- Review SG-1



- [HW - Sine Wave](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-sine-wave.md) - Here we are going to explore common periodic functions by building both a static sine wave, and an animated one, and maybe give you some ideas for Project 1. Be sure to follow along!



3. Phyllotaxis - [HW - Algorithmic Botany](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-algorithmic-botany.md)
-->

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-02A-notes.md**](week-02A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-03A-notes.md**](week-03A-notes.md)
