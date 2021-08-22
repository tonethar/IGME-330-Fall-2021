# Week 2A - Ajax, XHR, common data formats

<!--
## I. Overview

- Welcome back!
  - Questions?
- HW:
  - [Core Skills #4](https://github.com/tonethar/IGME-330-Master/blob/master/notes/4-adding-controls.md) is now up in myCourses, and is due Wednesday night
  - [Core Skills #5](https://github.com/tonethar/IGME-330-Master/blob/master/notes/5-write-some-code.md) is now up in myCourses, and is due Sunday night
  - To make room, the [Study Guide-1](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-1.md) due date was pushed back from Wednesday night to Monday night
- Attendance/Intro
  - Taking attendance alphabetically
  - Be ready:
    - have your camera on
    - tell us what you prefer to be called
    - tell us one thing you’ve done recently (SFW!) such as:
      - someplace interesting you visited OR
      - a book you read, movie you saw, video game you beat OR
      - a co-op you were on OR ... (SFW!)
- JS/DOM Review:
  - Review [Technobabble](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble.md):
    - Why use `const` instead of `let`?
    - Is `words1` mutable?
      - Let's test it!
    - How can you make an array or object *immutable*?
    - String concatenation v. Template Strings
    - Event Handler v. Event Listener
  - Review [HW-1B-Greeter](https://github.com/tonethar/IGME-330-Spring-2021/blob/main/weekly/week-01B-notes.md)
    - look at "do it in 1 function" answers
    - we'll see this again in *Shape Viewer* below (probably next time)
- Canvas Concepts (In-class exercise):
  - Shape Viewer:
    - Drawing State Properties: `ctx.fillStyle` & `ctx.strokeStyle` & `ctx.lineWidth`
    - Draw rectangles with `ctx.fillRect()` & `ctx.strokeRect()`
    - Draw rectangles with `ctx.beginPath()`, `ctx.closePath()`, `ctx.rect()`
    - Draw circles with `ctx.arc()`
    - Draw polygons with `ctx.moveTo()`, `ctx.lineTo()`, `ctx.fill()`

<hr>

## II. Start File

**shape-viewer.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Shape Viewer START!</title>
	<style>
	body {font-family: Arial, Helvetica, sans-serif;}
	canvas{
		border:1px solid gray;
		margin-left: 10px;
		margin-top: 10px;
		box-shadow: 3px 3px 6px rgba(0,0,0,0.5);
	}
	
	button{
		margin-left:2em;
		margin-top:1em;
		width:100px;
		height:40px;
		font-size:18px;
	}
	
	</style>
	
	<script>
		// #0 - in this class we will always use ECMAScript 5's "strict" mode
		// See what 'use strict' does here:
		// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions_and_function_scope/Strict_mode
		'use strict';
		
		// #1 call the init function after the pages loads
		// this is called an "event handler"
		window.onload = init;
	
		let ctx;
		function init(){
			// #2 Now that the page has loaded, start drawing!
			console.log('init called');
			
			// A - canvas variable points at <canvas> tag
			const canvas = document.querySelector('canvas');
			
			// B - the ctx variable points at a "2D drawing context"
			ctx = canvas.getContext('2d');	
			
			// C - all fill operations are now in yellow
			ctx.fillStyle = 'yellow'; 
			
			// D - fill a rectangle covering the entire canvas with the current fill color
			ctx.fillRect(0,0,500,300); 
			
			// #3 Hook up buttons
			document.querySelector('#red').onclick = drawRedBox;
		}
		
		function drawRedBox(){
			const color="red";
			ctx.save();
			ctx.fillStyle = color;
			ctx.fillRect(20,20,460,260); 
			ctx.restore();
		}
		
	</script>
</head>
<body>
	<canvas width="500" height="300">
	Get a real browser!
	</canvas>
	
	<section id="controls">
	  <button id="red">Fill Red</button>
	</section>
	
	
	<h2>Shape Viewer!</h2>
	<section id="assignment">
		<p>Stuff to do:</p>
		<ol>
			<li>(10%) Create a new style rule that will increase the vertical space between <code>&lt;li&gt;</code> tags on the page - try setting the <code>margin-bottom</code> property.</li>
			<li>(20%) Get the "Fill Green" button working. Clicking it should draw a green rectangle on the canvas. In your code, use the hexadecimal value for green rather than the CSS keyword.</li>
			<li>(20%) Add a new button titled "Fill Blue" to the page. Clicking it should draw a blue rectangle on the canvas. Be sure to draw the rectangle using <code>rect()</code> - and NOT <code>ctx.fillRect()</code></li>
			<li>(20%) Add a new button titled "Triangle" to the page. Clicking it should fill a magenta triangle with a 10-pixel thick green stroke on the canvas. Be sure that you can see ALL 10-pixels of the stroke.</li>
			<li>(20%) Add a new button titled "Circle" to the page. Clicking it should fill a 100-pixel radius purple circle with a 5-pixel thick white stroke on the canvas. Be sure that you can see ALL 5-pixels of the stroke.</li>
			<li>(10%) Because portions of the triangle and circle shapes may still be visible when you click other buttons, add code to effectively "clear" the image by re-drawing the 500x300-pixel yellow background. Add this to any function where its necessary.</li>
			<li>Challenge: At this point you have 3 buttons calling three different functions that all do basically the same thing. 
			The is wasteful and violates the <abbr>D.R.Y.</abbr> principle of Software engineering ("<b>D</b>on't <b>R</b>epeat <b>Y</b>ourself"). 
			Generalizing your code so that you have 1 function instead of 3 (i.e. <em>Procedural Abstraction</em>) would probably be a good idea. 
			Go ahead and replace <code>drawRedBox()</code>, <code>drawGreenBox()</code>, and <code>drawBlueBox()</code> with a function named <code>drawBox()</code>. 
			All three buttons should call the same <code>drawBox()</code> function, and draw the appropriate color box based on the button that was clicked. (This is trickier than you might think, and there are at least 3 ways to do it)</li>
			
		</ol>
	</section>
</body>
</html>
```

<hr>

## III. Screenshot of Done Version

![screenshot](_images/2A-shapeviewer-done.png)


<!--
Today we will: 
- Take a look at the *ScreenSaver* submissions
- Answer any questions from last week
- (Here are some additional review questions about JS and the DOM - we don't have time to review all of them today - but you should look these over at some point  [review-1.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/review-1.md))
- Talk about *Randomness & Aesthetics*
- Learn a little more about the Canvas API
- Refactor and add features to our screen savers
-->

<!--
## II. Required Reading & Assignments (*see myCourses for due dates*)
 Shape Viewer HW [HW-shape-viewer.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-shape-viewer.md)
- This is a potential [Project 1 - *Interactive Sandbox*](../projects/project-1.md) "starter" [HW-Lorenz Attractor](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-lorenz-attractor.md)
- Study Guide-2 [HW-SG-2.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-2.md)
-->

<!--
## III. Extra Credit Opportunity (*see myCourses for due dates*)
- This is a potential [Project 1 - *Interactive Sandbox*](../projects/project-1.md) "starter"  [HW-Random Walker](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-random-walker.md)
-->

<!--
## IV. Presentations
- [Randomness and Aesthetics](https://github.com/tonethar/IGME-330-Master/blob/master/notes/randomness-1.md)
- [Canvas-2 More Canvas](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-2.md) - drawing rings, polygons, `ctx.arcTo()`, `ctx.lineJoin`, line dashes
-->

<!--
## V. HW Assignment - *Screen Saver with Controls*
We will keep working on the Screen Saver:
- add a checkbox to control whether or not rectangles appear
- add **Pause** and **Play** buttons
- create a `drawRectangle()` helper function
- write code that "spray paints" rectangles onto the canvas when we click on it (e.g. like Jackson Pollock, but with digital rectangles instead)
- see videos "Screen Saver with Controls 1-4" below!
- see dropbox for due date
-->

<!--
**Here's the HTML & CSS for the UI - for your copy/paste pleasure!**

```html
<section>
  <button id="playButton">Play</button> <button id="pauseButton">Pause</button>
</section>
<section>
  <span><input type="checkbox" id="rectanglesCB" checked><label for="rectanglesCB">Create Rectangles</label></span>
</section>
<section>
  <p>Click on the screen to "spraypaint" rectangles (you probably want the screensaver to be paused)</p>
</section>
```

```css
body{
  font-family: sans-serif;
}
	
canvas{
  border:1px solid gray;
}
	
button{
  font-size:1.2em;
}

section{
  margin:.5em 0 .5em 0;
}
```
-->


<!--
**This helper code will come in handy when we want to determine where the user clicked on the canvas:**
```js
canvas.onclick = canvasClicked;

function canvasClicked(e){
  let rect = e.target.getBoundingClientRect();
  let mouseX = e.clientX - rect.x;
  let mouseY = e.clientY - rect.y;
  console.log(mouseX,mouseY);
}
```

## VI. Totally optional stuff you should do on your own

**\*\*Here are some optional (challenges) for you:\*\***

- add checkboxes to control the production of lines and circles
- create functions named `drawLine()` and `drawCircle()` (similar to `drawRectangle()` from the demo)
- create a `drawRing()` method that accepts an `innerRadius` and an `outerRadius` parameter (among others) and creates a ring like we did in Canvas-2 above.
- add a `linedash` parameter to `drawRectangle()`, `drawLine()` and `drawCircle()`, and utilize it if the developer passes in an array
- create a `drawTriangle()` function that accepts `width` and `height` parameters (among others) and draws a triangle like we did in Canvas-2 above

    
## VII. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D

## VIII. Videos of lecture & demos

We aren't always going to have video links, but here is a re-cap of today's major topics:

- [Screen Saver With Controls-1 (12:33)](https://video.rit.edu/Watch/screen-saver-with-controls-1) - Adding a checkbox
- [Screen Saver With Controls-2 (06:53)](https://video.rit.edu/Watch/screen-saver-with-controls-2) - Adding Pause & Play buttons\*
- [Screen Saver With Controls-3 (14:01)](https://video.rit.edu/Watch/screen-saver-with-controls-3) - Creating a helper function 
- [Screen Saver With Controls-4 (08:59)](https://video.rit.edu/Watch/screen-saver-with-controls-4) - Adding mouse interaction

<hr>

The following two videos continue with the Screen Saver, and show you a technique for creating an external JS library using an IIFE - *Immediately Invoked Function Expression*. This is a requirement of Project 1. We will be covering this topic in class next week, but the video links are provided in case you are interested in learning this now:

- [Screen Saver With Controls-5 (22:06)](https://video.rit.edu/Watch/screen-saver-with-controls-5) - Getting rid of "magic numbers" and using an IIFE to remove our variables and functions from global scope
- [Screen Saver With Controls-6 (15:35)](https://video.rit.edu/Watch/screen-saver-with-controls-6) - Creating an ES5 Style JS Library with an IIFE

<hr><hr>

 \* ***If you code the Play button the way we did in the video, there's a problem. Click the Play button repeatedly and you'll see what the issue is. Go ahead and try to fix this - you can do so with just one line of code.***
 
 -->
 
<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-01B-notes.md**](week-01B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-02B-notes.md**](week-02B-notes.md)
