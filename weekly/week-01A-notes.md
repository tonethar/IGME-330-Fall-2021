# Week 1A: Course Introduction | JavaScript Review

Welcome to the course!

## I. Overview
Welcome to IGME-330 *Rich Media Web Application Development I*. In this "creative coding" course you will be building on top of IGME-230/235 and constructing compelling interactive experiences that can be viewed over the web. You will also be learning about how to build more robust and modular web software by utilizing more features of JavaScript ES6, Web Components, CSS frameworks such as Bulma, and MVVM frameworks such as Vue.js

<hr>

## II. Prerequisites
IGME-230 or IGME-235 is a pre-requisite, and you should have a solid understanding of these topics:
- HTML/CSS, and be able to post web files to `people.rit.edu` - if you forgotten how, [here are the instructions](https://github.com/tonethar/IGME-235-Shared/blob/master/notes/core-skills/ftp-upload-walkthrough.md)
- Basic JavaScript and the Web Browser DOM (Document Object Model)

### \*\*Important - Before class begins\*\*
- Review the topics in these ten [IGME-230/235 Web App tutorials](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-0.md#section4) - most of this material should have been covered in your IGME-230/235 section. If you need a refresher on any of these topics, just go through the applicable tutorials at the link above. If you have any questions at all, or would like to have an assignment checked for accuracy, go ahead and reach out to me via email.

<hr>

## III. Course Description & Topics

### Official description from SIS
*This course provides students the opportunity to explore the design and development of media-rich web applications that utilize both static and procedurally manipulated media such as text, images and audio. This course examines client and server-side web development and features common to such applications. Issues explored include framework characteristics, information management, presentation, interactivity, persistence, and data binding. Programming projects are required.*

### Course Topics

- Project 1 & 2
  - Review of JavaScript & [Browser DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) (Document Object Model)
  - ES6 JavaScript features such as [ES6 modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
  - [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components) *(let's look at some examples)*
  - [Bulma](https://bulma.io/)
  - [XHR](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest) (330 review) & [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
  - [Vue.js](https://vuejs.org/)  JavaScript MVVM framework
- Project 3 (Rich Media App or Game)
  - [`<canvas>` 2D drawing API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
    - Some examples of what canvas can do are here (links near top of page) - [Canvas 2D Essential Skills #1 - Intro to the Drawing Context](https://github.com/tonethar/IGME-330-Master/blob/master/notes/1-canvas-intro-to-drawing-context.md)
  - [WebAudio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
  
  <hr>
  
  - Honors Section:
    - the honors class size is smaller (limited to 20 students)
    - in the first few weeks, we'll also take a look at how parts of the jQuery library work, and in the honors section we will start building our own version (just one class day or so)
    - for Project 2, the regular 330 sections will be covering the Vue.js reactive web framework. In the honors section we will learn about Vue, and will also look at how to build our own reactive (data binding) JS framework, and the use of the JavaScript Proxy object in doing this.
    - for Project 3, instead of canvas we will use Three.js (a web 3D visualization library)
    - time allowing, the honors section will look at the TensorFlow.js machine learning library and build some apps that utilize it
    - Lastly, honors students will be required to create a tutorial video and accompanying page about an interactive media topic or technology that wasn't covered in class (One example - https://developer.mozilla.org/en-US/docs/WebAssembly). A partner will be allowed for this

<hr>

## IV. History of "Rich Media App Development" on the web

### How "Web Apps" used to be made
- Since 1995 there have been many ways to build web enabled applications, but this was mostly with proprietary platforms & tools such as:
  - [Java Applets](https://en.wikipedia.org/wiki/Java_applet) - This was a really "hot" technology in the early days of the web, but the Java runtime was huge and really slow to download in the [dial up](https://en.wikipedia.org/wiki/Dial-up_Internet_access) era
  - [Macromedia Director](https://en.wikipedia.org/wiki/Adobe_Director) - bitmapped animations - originally a CD ROM publishing tool, updated for the web
  - [Macromedia (later Adobe) Flash](https://en.wikipedia.org/wiki/Adobe_Flash_Player) - animated vector graphics - was more or less killed when Steve Jobs refused to allow it on the iPhone
  - [Adobe Flex](https://en.wikipedia.org/wiki/Apache_Flex) - used the Flash player, but with standard UI components that made construction of conventional web applications easier
  - [Microsoft Silverlight](https://en.wikipedia.org/wiki/Microsoft_Silverlight) - similar to Flex
  - (and just prior to the web, and in its early days, CD-ROM technology was the hot way to deliver interactive content using applications such as [Macromind VideoWorks](https://en.wikipedia.org/wiki/Adobe_Director), [Apple HyperCard](https://en.wikipedia.org/wiki/HyperCard), [Silicon Beach SuperCard](https://en.wikipedia.org/wiki/SuperCard) and [Macromedia Authorware](https://en.wikipedia.org/wiki/Adobe_Authorware))
- These platforms were popular for a time, because they were the only cross-platform way to create "media rich" web applications (and games) with sound, animation, and video:
  - recall that YouTube didn't really get going until late 2006! (when Google bought them). Meaning that prior to this time, deploying video to the web was very HARD without using a browser plug-in like Flash
- So what really put the above platforms "out of business" was that browsers gradually became more capable on their own and were given many "native" capabilities, which reduced the need to resort to 3rd party plugins 
- Other issues with these "rich internet" platforms included:
  - developers had to pay for an IDE
  - lower than desired adoption rates by users
  - Since 2010, the number of mobile Internet devices has exploded, and most of these don't support the above platforms because the mobile vendors considered them slow, insecure, buggy, and memory hogs
- Premature obsolesence hurts!
  - The Flash plugin no longer runs on any current browers, and is no longer supported by Adobe. So if you authored a Flash app back in 2011 (or even 2013, as NMID was still teaching it then) and wanted to update it, how would you do so?
    - Answer: You can't! You would have to first find an old Flash IDE to access the code and media files, and then you would have to port the entire codebase to another platform

 
### "Vanilla JavaScript"
- One way to minimize app obsolesence is to write code on a relatively stable application platform
- Much of this course will be taught in browser "Vanilla JavaScript", which is JavaScript that works without relying on any external frameworks such as jQuery or React:
  - https://snipcart.com/blog/learn-vanilla-javascript-before-using-js-frameworks
- VanillaJS relies on open [*web standards*](https://www.w3.org/standards/):
  - these tend to evolve predictably, and respect backward compatibility
  - no IDE is required!
  - no one company owns the platform!
- VanillaJS seems to "age well", much better than the "rich internet" platforms listed above
  - for example, a JavaScript/DOM "vanilla" web app written in the "aughties" (2000-2009) would still work today, or require only minimal modification to run
- VanillaJS now (finally) includes Web Components, which are supported by all of the major browsers)

      
### "Web Frameworks"
- How will web frameworks like [ReactJS](https://reactjs.org/), "age"? Probably not well!
  - in 10 years (or even 5), will a typical React app still run in a web browser?
    - *Probably NOT*
  - And if it didn't, how easy would it be to edit the JSX code (JSX=proprietary web components) and republish it?
    - *More than likely the code would have to be completely re-written, in "React 10"?,  and then re-compiled*
- Don't get us wrong here:
  - we LOVE making apps in Web Frameworks like Vue.js (which we will cover later on in this course) and ReactJS (which is covered in the next course IGME-430)
  - and in large swaths of the industry, frameworks like Angular and React are what is used to make web apps
- But, because web frameworks come and go, and web standards are much more stable, the best way to learn JS is to first learn "Vanilla JS":
  - then, no matter what hot new web framework comes along, you'll be able to easily learn it because you understand the foundational web technologies that this hot new web framework is built on top of

<hr>

## V. Pedagogy (how this course is taught!)
- ***You need to review the week's lecture notes *prior* to attending class for that week***
- A typical classroom day will be:
    - a review of the days topics (see the Github lecture notes)
    - a live demo by the professor that reinforces the day's topics
    - 2-way interaction (you could get called on at anytime)
- The assignments given in this class break into two categories:
    - homework assignments, in-class exercises, and "Check offs" (which are small HWs/ICEs) that focus narrowly on one or more concepts
    - two projects with more flexible requirements that allow you to exercise considerable freedom and creativity in demonstrating key skills and understanding
- A large part of this course is taught similar to a typical math course: there will be several small homework assignments given every week, and because these assignments build upon one another, it is essential that they be completed both on-time and in-order, thus they have strict due dates.
- Keep an eye on the dropboxes in myCourses for what and when things are due. HW assignments will not be accepted late without prior permission from the instructor:
    - if something comes up and you need an extension for any reason, you need to get in touch with us at least 24-hours *before* the assignment is due
    - **Reminder:** *all code files (HTML, CSS, JavaScript) must be zipped when put in a dropbox, because otherwise myCourses strips out the JavaScript and CSS, and you will likely get a zero on the assignment*
- The due dates for these assignments will be clustered around the same days, often on Sunday night. This means that you should plan ahead, and not try to tackle them all in the last hour before they are due.
- Please get to class on time! Lectures will begin promptly at the start of class.

<hr>

## VI. Communication Details

- What name do you call me?
  - "Professor", "Professor Jefferson", or "Tony" all work
  - "Professor", "Professor Bast", or "Noah" all work
- Slack
  - You've already been added to our Slack workspace:
    - This [IGME-330 Introduction to Slack](https://docs.google.com/document/u/1/d/e/2PACX-1vQqjfsmGnvlweL9-ruKtsLn1wExSF2vapG1sVFGBJullHnFvbBYtYb60U8gaE7igzDGyGxzzYCxMmON/pub) document will help you get started there. 
    - The direct link to our workspace is:  https://rit-igme-330-2201.slack.com
    - Begin by posting an introduction in the #introductions channel.
    - You can pay attention to the Status Messages of your Professors.  We will update appropriately (typically indicating Office Hours availability when we're online).
- Zoom Professionalism
  - Article link (paywalled): https://www.wsj.com/articles/seven-rules-of-zoom-meeting-etiquette-from-the-pros-11594551601
  - The PDF of this article is in myCourses
 - Participation/Engagement (10% of grade)
   - Zoom meetings
     - be on time
     - we request that you keep web cam on
     - keep microphone muted
     - you could get called on at anytime, so be ready to respond
     - if you leave your computer for any reason, type `brb` (a reason is not required or wanted). Otherwise, if we call on you and you are not there, you will be marked absent
    
<hr>

## VII. Required Reading & Assignments
* [syllabus.md](../syllabus.md)
* [Project 1 *Vanilla JS App*](../projects/project-1.md) - this is what we are working towards for the first 1/3 of the course:
  - let's look at a "90%" example
* Also:
  - Keep an eye on the *Content* section of mycourses.rit.edu for "done" in-class demo files
  - Keep an eye on the mycourses.rit.edu dropboxes to see what is assigned and when it is due
  - *Technobabble* is due before we meet again - see myCourses dropbox for due date:
    - https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-technobabble.md
    - Let's look at the "done" version - it's simple, but looks good on mobile and is responsive

<hr>

## VIII. Demo Starter Code

**starter.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Starter Page</title>
	<style></style>
	<script></script>
</head>
<body>
<p>... something awesome goes here ...</p>
</body>
</html>
```

<hr>

<a id="js-review-notes"></a>
 
## IX. JavaScript/DOM Review & Demo

- 1. What is JavaScript?
  - https://developer.mozilla.org/en-US/docs/Web/JavaScript
  - Used on both the client-side and server-side to create interactive web applications
  - Weakly typed:
    - after they are declared, variables can contain any type
    - JS uses *dynamic typing* to verify the type safety of a program at runtime, as opposed to compile time (static) typing
  - Multi-Paradigm:
    - *imperative* - a series of commands that describe how the program behaves (as opposed to *declarative* languages such as CSS or SQL)
    - *functional* - use functions to compose a program, avoid globals & mutable state
    - *event-driven* - program flow is driven by user and system events
    - *object-based* - an object literal, many built-in objects to use, and both prototypical and classical inheritance when the developer creates their own objects
    - *duck typed* - an object's suitability to be used for particular purpose is determined by the presence of certain methods and properties, rather than the type of the object itself
- 2. Setting up the development environment - easy!
  - A text editor
  - Chrome
  - create a web page, then run JavaScript in the console or type code into the &lt;script> tag
  - the console is an interactive **REPL** - "Read, Evaluate, Print, Loop"
    - shift-enter for multi-line code
    - up arrow to repeat last typed line
- 3. JavaScript Review & Demo
  - `'use strict';` - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode
  - declaring variables with `var`, `let`, and `const`
  - operators
  - data types:
    - `Boolean`, `Number`, `String`, `Null`, `Undefined`, `Symbol` (new for ES6) and `BigInt` (really new)
    - and `Object`
    - Reference: 
      - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures
      - https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects
  - Functions are also Objects and thus “first class” values, and can be both passed to functions and returned from them
  - `console.log()`
  - Standard built-in objects - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects
    - `Date`
    - `Math`
    - `Array`
  - Functions
    - writing functions
    - calling functions
    - Some DOM Elements (DOM = Document Object Model)
      - https://en.wikipedia.org/wiki/Document_Object_Model
      - https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model
    - Add &lt;button>, &lt;input>, and &lt;p>
    - Manipulating the properties of DOM elements:
      - `document.querySelector()`
      - `document.querySelectorAll()`
    - Events:
      - DOM elements have to load before we can manipulate their properties
      - event handlers - the `onclick` attribute
      - `element.addEventListener()`
- 4. JavaScript Debugger:
  - setting breakpoints
  - inspecting variable values 
  - viewing the call stack
  - "View Page Source" v. the Debugger's "Inspect Elements" view
- 5. Demo:
  - Add a "last name" input so that we can greet the person using both their first and last name
  - *Declaratively* (using CSS) make the button 50 pixels tall by 100 pixels wide
  - *Imperatively* (using JavaScript) give the paragraph a red text color, and a yellow background color

<hr>

<a id="js-review-video-links" />

## X. Videos of JS & DOM Review demo

We aren't always going to have video links, but here they are in case we run out of time today:

<!---
- [Week 1A - JavaScript and DOM review - 1 (20:36)](https://video.rit.edu/Watch/f8H5Akr4) - the lecture begins at 8:50, the demo begins at 13:30 
- [Week 1A - JavaScript and DOM review - 2 (29:51)](https://video.rit.edu/Watch/Dr8n4XNz)
--->
- [JSReview-1: Using the console (06:18)](https://video.rit.edu/Watch/js-review-1-using-the-console)
- [JSReview-2: Variables and scope (16:12)](https://video.rit.edu/Watch/js-review-2-variables-and-scope)
- [JSReview-3: Working with DOM & Creating Greeter App (12:19)](https://video.rit.edu/Watch/js-review-3-working-with-dom-A)
- [JSReview-4: Working with DOM & Refactoring Greeter App (13:26)](https://video.rit.edu/Watch/js-review-4-working-with-dom-B)

<hr>

## XI. Today's Activities

1) Review sections I. - VII. above that discuss this course
  
2) Grab the starter code in section VIII.

3) Section IX. - we will begin to work through the first part of this demo by reviewing what is covered in the 1st and 2nd videos linked above

4) Next time we will finish up the above demo, and you will have a HW assignment that builds on this material


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
|   :-\  |  [**IGME-330 Schedule**](../schedule.md) | [**week-01B-notes.md**](week-01B-notes.md)
