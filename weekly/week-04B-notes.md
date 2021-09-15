# Week 4B - More Web Components

## I. Lecture/Demo Notes
- [HW - Web Components-2 - more lifecycle methods](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-2.md)

<hr>

## II. What else do we need to know about web components?
- *How do we pass arrays or object values to a component, can we do that in an attribute?*
  - not really, because HTML attribute values are always strings
    - (But actually, you hypothetically *could* pass in a stringified JSON object as an attribute value, and then have the component `JSON.parse()` it - but don't do that!)
  - the solution is to create a JS *property* in the constructor of the component - ex. `this.items=[]` - and then set that value from the "outside" by using JS rather than HTML attributes
- *How else can we pass values to components?*
  - Answer: *Slots* - https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_templates_and_slots
- *Imagine that we have a progress bar component, and that when it hit 100% we want to have it call "up" to code that we have running in our main application - how do we do it?*
  - Custom events are the cleanest way to do it
  - See `element.dispatchEvent()` and `CustomEvent` - https://developer.mozilla.org/en-US/docs/Web/Events/Creating_and_triggering_events

<hr>

## III. Breakout Group Activity
- See myCourses

<hr>

## IV. Homework
- **HW - Web Components-2** above - this should take you less than 5 minutes
- The **Breakout Group Activity** above - hopefully that is near completion - you may continue to work on it solo, or with your group member(s)
- [HW - Web Service App with Components](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-web-service-app-with-components.md) - due start of our next class meeting

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-04A-notes.md**](week-04A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | :-/
