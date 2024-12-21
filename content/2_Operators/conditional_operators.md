---
title: Conditional and Logical Operators
weight: 5
---
[original slides](../old_presentation2_5)

<p data-height="600" data-theme-id="33744" data-slug-hash="834bee751e9122c4d293f963a3a36740" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="2.5 Conditional and Logical Operators" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/834bee751e9122c4d293f963a3a36740/">2.5 Conditional and Logical Operators</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation2_5)

### Conditional Operators 

* JavaScript's conditional operator can be used as a shorthand for conditional statements(these are covered in a later lesson). 
* The conditional operator assigns a value to a variable according to the result of a specified condition (a real world example: if the weather is cold outside, you choose to wear a coat. If it isn’t you don’t. Checking the weather is the condition). 
* The conditional operator has a specified syntax(way of writing/coding) instead of a single operator.
---
#### 1. Conditional : used to test the relationship between a variable's value and another variable's value, using the comparison operators
* Syntax: variablename = (condition) ? value1:value2
* Examples:
```
let time = 1800; //this is 6pm in military time
let currentSky = time >= 1650 ? "dark" : "light";
```
* The currentSky variable will evaluate to "dark" if the condition is true, or "light" if the condition is false. 
* Q : What is the result of the comparison (light or dark)?

* In this example: 
```
time = 700; //this is 7am military time
currentSky = time <= 1650 ? "light" : "dark";
```
* What is the result of the comparison (light or dark)?
---
#### Logical Operators 

* JavaScript's logical operators are used to determine whether an entire statement/condition is true or false depending on the operation and values involved.
* These can be used to assign boolean values to variables or to determine the next course of action in conditional statements.
* The logical operators have symbols known as the operators that are used to perform the operations
---
##### 1. And : if the values on both sides of the operand are true, then the operation returns true. If one is false, the operation returns false. If both are false, the operation returns false.
* Operator: &&
* Examples:
```
x = 20;
y = 30;
j = 19;
z = x > 10 && y < 50; //returns true
```
---
##### 2. Or : if one or more values are true, the entire statement returns true. Only if both sides of the operand are true does the entire statement return true
* Operator: ||
* Examples:
```
x = 20;
y = 30;
z = x > 10 || y < 15; //returns true because the left side is true, even though the right side is false
```
---
##### 3. Not : the not operator returns the opposite of the value it is operating on.
* Operator: !
* Examples:
```
x = false;
y = true;
z = !x; //returns true
z = !y; //returns false
```
---
#### Exercise 2.5

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="WbeREWN" data-pen-title="Exercise 2.5" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/WbeREWN">
  Exercise 2.5</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>