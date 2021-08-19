# IGME-330 - Spring 2021: Topics & Outcomes

## I. Basic JavaScript & Browser DOM
This material is review you need to do on your own - most of this is now taught in IGME-230
- See these [IGME-230 Web App tutorials](https://github.com/tonethar/IGME-230-Master/blob/master/notes/web-apps-0.md#section4)

## II. More JavaScript
- Object-Oriented JavaScript: Object literals, Function constructors, `Object.create()`, ES6 class constructors
- Modular JavaScript: ES6 Modules
- Transpiling between ES5 & ES6 using Node.js & Webpack

## III. Canvas Drawing API
- **Getting a reference to 2D context** - `canvasElement.getContext("2d")`
- **Canvas drawing state attributes** - `strokeStyle`, `fillStyle`, `lineWidth`, `lineCap`, `lineJoin`, `miterLimit`, `shadowOffsetX`, `shadowOffsetY`, `shadowBlur`, `shadowColor`, `font`, `textAlign`,`textBaseline`, `globalAlpha`, `globalCompositeOperation`
- **Drawing state stack management** - `save()`, `restore()`
- **Transformation methods** - `scale()`, `rotate()`, `translate()`, `transform()`, `setTransform()`
- **Transformation concepts** - matrix, identity
- **Rectangles** - `clearRect()`, `strokeRect()`, `fillRect()` in conjunction with applicable state attributes
- **Text** - `fillText()`, `strokeText()`, `measureText()` in conjunction with applicable state attributes
- **Image drawing** - `drawImage()`, `createPattern()`
- **Compositing modes** - set with `globalCompositeOperation`, possible values include: `source-over`, `source-in`, `source-out` and others
- **Gradients** - `createRadialGradient()`, `createLinearGradient()`
- **Pixel Manipulation** - `createImageData()`, `getImageData()`, `putImageData()`, `canvas.toDataURL()`

## IV. WebAudio API
- analyzer nodes: frequency and time domain
- audio effect nodes & convolutions

## V. Text
- working with both unstructured and structured text
- Node.js, Hieroku, Twitter Bot HW

## VI. MVVM (Model View View-Model) Frameworks
- Vue.js framework (similar to React and Angular, but easier to get started with)

## VII. Storing Data in the cloud
- Firebase
