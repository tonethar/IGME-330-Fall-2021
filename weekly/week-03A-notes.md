# Week 3A - Finish Up XHR

## I. Review the HW
- Ajax HW
  - [HW - Ajax-3 - loading and parsing XML files](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-3.md)
  - XML parsing:
    - `xhr.responseXML`
    - 5 top rules of *well-formed* XML
    - Is HTML well-formed XML?
    - Any questions?
- [Technobabble IV](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-4.md)
  - CSV parsing - Any questions?
- [Technobabble V](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-5.md)
  - XML parsing - Any questions?

<hr>

## II. Upcoming Homework
- You should complete these in the order below (due soon):
  - [HW - Ajax-4 - loading and parsing JSON files](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-4.md)
  - [HW - Technobabble Generator VI - JSON](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble-6.md)
  - [HW - Ajax-5 - the `fetch()` API](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-ajax-5.md)

<hr>

## III. Breakout Groups

- Your mission (with a partner) is to write code that downloads and displays info about popular Star Wars characters
- A common progrtamaming ant-patern  


## III-A. Screenshot if complered Version

<hr>

<hr>

## III-B. Start Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no">
	<title>Chained XHR Calls</title>
	<style>
	body{
	  font-family: sans-serif;
	}
	button{
		font-size: 1.2rem;
	}
	</style>

</head>
<body>
	<h2>Chained XHR Calls to Star Wars API</h2>
	<hr>
	<button id="my-button">Star Wars Data</button> <-- Click button to load!
	<h3>Star Wars Character Info</h3>
	<p>Character Name: <span id="output-1">???</span></div>
	<p>Homeworld Name: <span id="output-2">???</span></div>
	<div id="output-3">
		<h3>Films that this homeworld appeared in:</h3>
	</div>

<script>
const output1 = document.querySelector("#output-1");
const output2 = document.querySelector("#output-2");

const baseURL = "https://swapi.dev/api/people/";

const loadPerson = url => loadTextXHR(url,personLoaded);

const loadTextXHR = (url,callback) => {
	// you wrote this last time
}; 

const personLoaded = e => {
	// write this
	// make sure that the character exists - #17 does not - https://swapi.dev/api/people/17
	// if they exist, show character name
	// if they exist, load planet
};

document.querySelector("#my-button").onclick = () => {
	output1.innerText = "";
	output2.innerText = "";
	loadPerson(baseURL + getRandomInt(1,20));
};

// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random
function getRandomInt(min, max) {
  min = Math.ceil(min);
  max = Math.floor(max);
  return Math.floor(Math.random() * (max - min + 1) + min);
}

</script>
</body>
</html>
```

<!--
## I. Overview

1) Review [HW-SG-1](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-1.md):
  
    - look at "Smiley" submissions
    - concepts covered - this was mostly a review of what we have been doing in class (which is a good thing!)

<hr>

2) Talk about canvas transformations - here are the notes - [Canvas III - Transformations](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-3.md)
  
     - we will be doing a demo of translate/rotate/scale in class
     - the demo "start" code is in the link above, and up in myCourses there is a "clip" file with some code you can copy/paste 
     - there is an accompanying HW assignment - look in myCourses dropbox for "3A inclass Checkoff" - it is due tonight

<a id="hw" />

<hr>

3) Other Homework

    - [Animated Sine Wave HW](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-sine-wave.md) is due Wednesday night - it doesn't take too long
    - [Canvas SG-2](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-2.md) is assigned - see myCourses dropbox
    - 3 "optional" extra credit assignments - some of them are good Project 1 "starters":
      - they are all bonus "extra credit" items
      - the dropboxes for these close Monday night
      - ***you MUST do at least one of them (but you can do all three if you want, for <u>super power-up credits & achievements</u>!)***
      - here they are (for your edification):
        - [Extra Credit - Random Walker](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-random-walker.md)
        - [Extra Credit - Conway's Life](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-canvas-life.md)
        - [Extra Credit - Lorenz Attractor](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-lorenz-attractor.md)
  
<!--
- Review Periodic Functions & Phyllotaxis HW:
  - [HW - Sine Wave](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-sine-wave.md)
    - look at submissions
  - [HW - Algorithmic Botany](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-algorithmic-botany.md) 
    - look at submissions
- [Project 1](../projects/project-1.md) assigned! 
  - Let's discuss!
  - See dropboxes for due dates
-->

<!--
## II. Lecture/Demo - the JavaScript IIFE
- Stands for "Immediately Invoked Function Expression"
- Using these is one of the requirements for Project 1
- See [IIFE Notes](https://github.com/tonethar/IGME-330-Master/blob/master/notes/IIFE-notes.md) & demo
-->

<!--
## III. Demo - Modifying your "Screen Saver with Controls"
- Go ahead and grab your "Screen Saver with Controls" code from last week:
  - First, we'll re-factor the code by getting rid of ["magic numbers"](https://en.wikipedia.org/wiki/Magic_number_(programming)#Unnamed_numerical_constants) (e.g. Unnamed Numerical values or constants)
  - Next, we'll wrap all of our JS code in an IIFE
  - Then we'll create an ES5 style external "library" of reusable functions named **"abcLIB.js"** by using an IIFE (*abc* will be your initials):
    - time allowing, we'll also take a quick look at how RiTa.js structures their library using an IIFE: https://rednoise.org/rita/download.php
-->

<!--
**Try it:** Once everything is working, move the remaining JS code in your HTML to an external JS file named **index.js**, and then import it with a &lt;script> tag
-->

<!--
## IV. Videos
- These videos were originally linked to on 2A, and will re-cap what we covered in section III. above:
  - [Screen Saver With Controls-5 (22:06)](https://video.rit.edu/Watch/screen-saver-with-controls-5):
    - getting rid of "magic numbers" by adding `canvasWidth`, `canvasHeight` variables, and a `drawParams` object
      - https://en.wikipedia.org/wiki/Magic_number_(programming)
    - using `Object.freeze()` to create an [immutable object](https://en.wikipedia.org/wiki/Immutable_object)
    - using an IIFE ("immediately invoked function expression") to remove our variables and functions from global scope:
      - https://developer.mozilla.org/en-US/docs/Glossary/IIFE
  - [Screen Saver With Controls-6 (15:35)](https://video.rit.edu/Watch/screen-saver-with-controls-6):
    - Creating an ES5 Style JS Library with an IIFE
-->

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-02B-notes.md**](week-02B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-03B-notes.md**](week-03B-notes.md)
