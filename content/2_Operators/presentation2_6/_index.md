---
title: Other Operators
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Other Types of Operators 

* JavaScript has a few additional operators that can be convinient, and are worth mentioning. You likely would not use these as frequently as the other operators already discussed.

## 1. Type Of : The type of operator returns the data type of a specified variable, object, function, etc.

* Operator: typeof
* Examples:
```
let car = "Honda";
typeof car; //this line returns "string" because the value of car is a string
let x, y;
let equation = x + 5 / (6 * y) + 17;
typeof equation; //this line returns "number" because the value returned from evaluating the equation is a number
```
---
## 2. Delete : The delete operator deletes a property from an object
* Operator: delete
* Examples:
```
let pet = {name:"Macy", species:"Dog", age:5, attribute:"fluffy"};
delete pet.age;   // removes the age property from the pet object
```
---
## 3. In : The in operator checks to see if a specified property is in a specified object(objects are covered in the next lesson). If the object does contain the property, the operation returns true. Otherwise, it returns false.
* Operator: in
* Examples:
```
pet = {name:"Macy", species:"Dog", age:5, attribute:"fluffy"};
"name" in pet;   // returns true because the pet object has a property called "name"
```
---
# Exercise 2.6

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="GgKrvVz" data-pen-title="Exercise 2.6" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/GgKrvVz">
  Exercise 2.6</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>