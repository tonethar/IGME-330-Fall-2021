
# Week 13B - More JavaScript

## I. Project 3
- [Project 3 - *Interactive Sandbox of Awesomeness* - Overview & Tips](../projects/p3-overview-and-tips.md)
- Project 3 checkpoint is due in myCourses dropbox next Tuesday night

<hr>

## II. JavaScript Prototype Chain

- [JavaScript Objects & the JavaScript Prototype Chain](https://github.com/tonethar/IGME-330-Master/blob/master/notes/js-prototype-chain.md)

<hr>

## III. JavaScript Getters and Setters

- What you do here is to create a "public property" that is actually going to call a setter method (where you could do data validation)
- You also need to create a "backing property", the convention is that it is the same name as the property but begins with an underscore
- You have probably seen this technique before in your C# classes
- BTW - this also works on object literals, not just classes

**setter-getter-tester.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<title>Setter Getter Tester</title>
</head>
<body>


<script>
	"use strict";
	class Monster{
	  constructor(species,hitpoints){
	    this._species = species;
	    this._hitpoints = hitpoints;
	  }
		
	  // read-only
	  get species(){
	    return this._species;
          }
		
	  get hitpoints(){
	    return this._hitpoints;
	  }
		
	  set hitpoints(value){
	    value = parseInt(value); 
	    if(value >= 0) this._hitpoints = value;
	  }
	
	}
	
	const m1 = new Monster("Orc",10);
	
	console.log(m1.species);   // calls getter without parentheses
	console.log(m1.hitpoints); // calls getter without parentheses
	m1.hitpoints = 100;        // calls setter and passes in 100 for a `value`
	console.log(m1.hitpoints); 		
	m1.hitpoints = 2.6;        // calls setter and passes in 2.6 for a `value`, which is truncated to `2`
	console.log(m1.hitpoints); 
	m1.hitpoints = -300;       // calls setter and passes in -300 for a `value`, which is ignored
	console.log(m1.hitpoints);  
//	m1.species = "Goblin"; // ERROR!
//	m1._species = "Kobold"; // allowed! :-|
//      console.log(m1.species); 
</script>
</body>
</html>
```


## IV. Other Stuff

- Next week's class (11/22/21 & 11/23/21) are *optional* work days
  - the Prof will be online in Zoom, but won't be taking attendance

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-13A-notes.md**](week-13A-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-14A-notes.md**](week-14A-notes.md)  
  
