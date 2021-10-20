# Week 10 - Intro To Canvas

Welcome to day 2! We have quite a bit to cover today. If we don't get to cover everything during the class time, you are expected to get this material by watching the video links at the bottom of this page.

## I. Overview
Canvas is a 2D bitmap drawing API that allows the developer to write code that draws shapes and images into a browser window without the need for a plug-in like Flash or Java. 

## II. Required Reading & Assignments
* "Hello Canvas" HW -> [HW-hello-canvas.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-hello-canvas.md)
* Study Guide-1 -> [HW-SG-1.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-SG-1.md)
* Fix The Code-1 (we'll do this in class) -> [HW-fix-the-code-1.md](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-fix-the-code-1.md)

## III. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial

### III-A. The canvas specification
*When in doubt, read the spec!*
- https://www.w3.org/TR/2dcontext/
- https://html.spec.whatwg.org/multipage/canvas.html#2dcontext

## IV. Presentations
- [Intro-to-Canvas.pdf](https://github.com/tonethar/IGME-330-Master/blob/master/presentations/Intro-to-Canvas.pdf)

## V. Demo & HW
- [Intro to the Canvas 2D Drawing API (includes "screen saver" HW)](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-1.md)

## VI. Videos of lecture & demos

We aren't always going to have video links, but here they are:

- [Canvas Intro-1 (11:40)](https://video.rit.edu/Watch/w7CXx43H):
  - Intro to Canvas2D API
  - Obtaining a drawing *context* with `canvas.getContext("2d")`
  - Canvas2D *convenience method*: `ctx.fillRect()`
  - Canvas2D property: `ctx.fillStyle`
- [Canvas Intro-2 (13:24)](https://video.rit.edu/Watch/Bs62Kqo5):
  - Fill and stroke rectangles, lines & circles
  - Canvas2D methods for describing a path :`ctx.beginPath()`, `ctx.closePath()`, `ctx.rect()`, `ctx.moveTo()`, `ctx.lineTo()` & `ctx.arc()`
  - Canvas2D methods for rendering a path: `ctx.fill()` & `ctx.stroke()`
  - Canvas2D state properties: `ctx.strokeStyle` & `ctx.lineWidth`
- [Canvas Intro-3 (10:27)](https://video.rit.edu/Watch/j3P6BkYe):
  - HW Starter code - begin building "ScreenSaver App" (*The 80's are calling and want their flying toasters back!*)
  - utilize helper functions and calling `getRandomColor()` and `getRandomInt()` from the console
  - write a helper function: `drawRandomRect()`
  - animation: `update()` function & `window.requestAnimationFrame()`
- [Canvas Intro-4 (15:07)](https://video.rit.edu/Watch/d9ZMi3o7):
  - keep working on "ScreenSaver App" 
  - Canvas2D *drawing state stack* methods: `ctx.save()` & `ctx.restore()`
  - more helper functions: `drawRandomCircle()`, `drawRandomLine()` & `cls()`
  - Canvas2D *convenience method*: `ctx.clearRect()`
  - `window.setTimeout()`
- [Canvas Intro-5 (08:44)](https://video.rit.edu/Watch/Ri9y7H3L):
  - finish "ScreenSaver App" 
  - Canvas2D property: `ctx.globalAlpha`
  - Demo: ES6 arrow function
  - Demo: ES6 template string

<hr><hr>


| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-09B-notes.md**](week-09B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-10B-notes.md**](week-10B-notes.md) 
