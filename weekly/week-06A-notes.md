# Week 6A - Working on Project 1

## I. Project
- Discuss [Project 1 - VanillaJS App of Awesomeness](../projects/project-1.md) topic submissions
  - Due Soon: a P1 working prototype - see dropbox for details
  - **IMPORTANT** - be sure that your web service works:
    -  in a browser window AND
    -  from `fetch()` or `XHR` JavaScript code
    -  test your web service - SOON - and stay after class today if you are having any issues connecting to it
    -  also, note the **CORS** folder of proxy-server demo code that's in myCourses - that might be a big help to some of you
- ES6 Module Pattern:
  - it is required in Project 1, and was covered in WC-3 - let's review that right now:
    - all the JS code in each JS file is now *private* to that file, and specific functions/classes/variables are only visible when they are exported via the `export` statement
    - note that we now only need ONE `<script>` tag in our HTML file (for the JavaScript code we write) and if one JS file needs a function that is declared in another JS file, it needs to explicitly `import` it
   - [ES6 Module Pattern](https://github.com/tonethar/IGME-330-Master/blob/master/notes/ES6-module-pattern-2211.md) - let's look at these notes

<hr>

## II. Review Web Components

- [WC-1 - Intro to Web Components](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-1.md):
  - we learned about Custom Elements, the Shadow DOM and HTML templates
  - we saw how to extend the `HTMLElement` class, what needs to go into the `contructor()` and the `connectedCallback` lifecycle method
- [WC-2 - more lifecycle methods](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-2.md):
  - we discussed the naming rules for custom element and custom attribute names, how to change custom element attribute values via JavaScript
  - we also implemented `static get observedAttributes()` & the `attributeChangedCallback()` and `disconnectedCallback()` lifecycle methods
  - we also saw how to add JavaScript to our components - in this case a "count" that increased every time the text was clicked 
- [WC-3 - Build a component driven web app](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-3.md):
  - in this exercise we converted a Star Wars Character app to use web components - here `<sw-header>`, `<sw-footer>` and `<sw-card>`
  - we were exposed to `??` - JavaScript's new *nullish coalescing operator*
  - we saw how ES6 JS modules work with the `import` and `export` statements
  - we also looked at a version of the SW App that had an `<sw-app>` component that contained the majority of the app logic, and also our 3 previous components. So yes, it's possible (and desirable) to have components nested inside of other components
- [WC-4 - Walk through a `<my-list>` web component](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-4.md):
  - we saw how to pass array and object data to a `<my-list>` web component (which is an issue because the values of HTML attributes must be strings). The trick is to NOT use an attribute, but instead declare a regular JS property on the component, and pass the array or object data in as a value of that property

**\*NEW\***

- [WC-5 - Dispatching Custom Events](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-5.md):
  - how do you pass information *out* of a web component and communicate with the rest of your program?
  - one answer: Custom Events implemented via the `CustomEvent` class and `EventTarget.dispatchEvent()`
  - we will give the `<my-list>` component from last time the ability to emit a "lengthchanged" event - this event will be broadcast by the component whenever the `.length` of the `items` array changes
  - there is a HW assignment for this, see myCourses dropbox
 - [HW - Web Components-6 - Building a "pubsub" object aka "Publish/Subscribe"](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-6.md):
   - Optional, look it over if you wish, no associated HW assignment


<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-05A-notes.md**](week-05A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | :-\

