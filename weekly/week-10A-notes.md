# Week 10 - Intro To Canvas

## I. Overview
- Canvas is a 2D bitmap drawing API that allows the developer to write code that draws shapes and images into a browser window without the need for a plug-in like Flash or Java. 
- [Intro-to-Canvas.pdf](https://github.com/tonethar/IGME-330-Master/blob/master/presentations/Intro-to-Canvas.pdf)

<hr>

## II. Canvas Concepts - Shape Viewer

- [HW - Shape Viewer](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-shape-viewer-2211.md)

<hr>

## III. Reference
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API
- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial

### III-A. The canvas specification
*When in doubt, read the spec!*
- https://www.w3.org/TR/2dcontext/
- https://html.spec.whatwg.org/multipage/canvas.html#2dcontext

<hr>

## IV. HW & Videos
- [Canvas 2D Essential Skills #1 - Intro to the Drawing Context](https://github.com/tonethar/IGME-330-Master/blob/master/notes/1-canvas-intro-to-drawing-context.md):
  - Concepts:
    - What is canvas?
    - Alternative drawing APIs
    - Obtaining a *drawing context*
  - Docs:
    - https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API
    - https://en.wikipedia.org/wiki/Canvas_element
    - **Get a *drawing context***
      - [`canvas.getContext("2d")`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/getContext)
    - **Canvas *convenience* methods**:
      - [`ctx.fillRect()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/fillRect)
      - [`ctx.strokeRect()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/strokeRect)
    - **Canvas *drawing state* properties**:
      - [`ctx.fillStyle`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/fillStyle)
      - [`ctx.strokeStyle`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/strokeStyle)
      - [`ctx.lineWidth`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/lineWidth)
- [Canvas 2D Essential Skills #2 - Paths & Lines & Arcs](https://github.com/tonethar/IGME-330-Master/blob/master/notes/2-canvas-paths-lines-arcs.md):
  - **Path methods:**
    - [`ctx.beginPath()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/beginPath)
    - [`ctx.closePath()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/closePath)
    - [`ctx.rect()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/rect)
    - [`ctx.fill()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/fill)
    - [`ctx.stroke()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/stroke)
  - **Line methods:**
    - [`ctx.moveTo()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/moveTo)
    - [`ctx.lineTo()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/lineTo)
  - **Arc methods:**
    - [`ctx.arc()`](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/arc)
- [Canvas 2D Essential Skills #3 - Begin making a screensaver](https://github.com/tonethar/IGME-330-Master/blob/master/notes/3-begin-making-screensaver.md)
- [Canvas 2D Essential Skills #4 - Adding Controls](https://github.com/tonethar/IGME-330-Master/blob/master/notes/4-adding-controls.md)
- [Canvas 2D Essential Skills #5 - Write some code!](https://github.com/tonethar/IGME-330-Master/blob/master/notes/5-write-some-code.md)

<hr><hr>


| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-09B-notes.md**](week-09B-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | :-/
