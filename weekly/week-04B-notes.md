# Week 4B - More Web Components

## I. Lecture/Demo Notes
- [HW - Web Components-2 - more lifecycle methods](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-wc-2.md)

<hr>

## II. Breakout Group Activity

<hr>

## III. What else do we need to know about components?
- *How do we pass arrays or object values to a component, can we do that in an attribute?*
  - not really, because HTML attribute values are always strings
  - the solution is to create a JS *property* in the constructor of the component - ex. `this.items=[]` - and then set that value from the "outside" by using JS rather than HTML attributes
-*Imagine that we have a progress bar component, and that we want to have it call *outside* code that we have running in our main application - how do we do it?*

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-04A-notes.md**](week-04A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | :-/
