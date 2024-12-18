---
title: Assignment Operators
weight: 2
---
[original slides](../old_presentation2_2)

<p data-height="600" data-theme-id="33744" data-slug-hash="6d7aaa42a1365e32d6a3e3dde7c4ad24" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="2.2 Assignment Operators" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/6d7aaa42a1365e32d6a3e3dde7c4ad24/">2.2 Assignment Operators</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation2_2)

# Assignment Operators 

* JavaScript's assignment operators are used to assign variables to different values. Assignment operators each have a symbol known as the operator that is used to perform the operation.

## 1. Equals : used to assign a variable to a value
* Operator: =

* Examples:
```
let example = 5;
let name = "Alex";
name = example;
```
* Q : What is the value of the variable named "name"?
---
## 2. Plus-Equals : assigning a variable to its original value plus some specified value
* Operator: += 
* Examples:
```
x = 5;
y = 30;
x += 10;
x += y;
y += x;
```
* Q : What is the value of variable y?
---
## 3. Minus-Equals : assigning a variable to its original value minus some specified value
* Operator: -= 
* Examples:
```
x = 50;
y = 23;
x -= 12;
x -= y;
y -= x;
```
* Q : What is the value of variable y?
---
## 4. Times-Equals : assigning a variable to its original value times some specified value
* Operator: *= 
* Examples:
```
x = 13;
y = 9;
x *= 3;
x *= y;
y *= x;
```
* Q : What is the value of variable y?
---
## 5. Divide-Equals : assigning a variable to its original value divided by some specified value
* Operator: /= 
* Examples:
```
x = 348;
y = 24;
x /= 58;
y /= x;
```
* Q : What is the value of variable y?
---
## 6. Modulus-Equals : assigning a variable to its original value modulus some specified value
* Operator: %= 
* Examples:
```
x = 49;
y = 17;
x %= 12;
y %= x;
```
* Q : What is the value of variable y?
---
# Exercise 2.2

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="ZYzLJyG" data-pen-title="Untitled" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/ZYzLJyG">
  Untitled</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>