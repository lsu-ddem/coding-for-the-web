---
title: Arithmetic Operators
weight: 1
---
[original slides](../old_presentation2_1)

<p data-height="600" data-theme-id="33744" data-slug-hash="179fa139121785c06929d1bc67e7766c" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="2.1 Arithmetic Operators" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/179fa139121785c06929d1bc67e7766c/">2.1 Arithmetic Operators</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation2_1)

# Javascript Operators

* Operators are used in programming to assign new values, compare values, test values, update values, perform arithmetic on values, etc.
* In short, operators are used to manipulate variables in a number of ways. 
* So far, we've only really dealt with the default assignment operator, =, like when we say:

```
var usingAssignmentOperator = “the equals sign is the assignment operator” 

```
* In total, there are seven categories of operators in JavaScript. 
* These include operators for arithmetic operations, assignments, string operations, comparisons, logical operations, conditional operations, and other types of operators that are worth mentioning.
---
## Arithmetic Operators
* JavaScript's arithmetic operators are used to perform arithmetic in your code. 
Arithmetic operators each have a symbol known as the operator that is used to perform the operation.

### 1. Addition : adding two values or variables together
 * Operator: + 
 * Examples:
```
 let sum = 5 + 7000;
 let x, y;
 x = 20;
 y = 30;
 let z = x + y + 400; 
```
 * Q : What is the value of variable z?
---
### 2. Subtraction : subtracting one value or variable from another
 * Operator: - 
 * Examples:
```
 let minus = 300 - 87;
 let a, b;
 a = 83;
 b = 65;
 let c =  a - b; 
```
 * Q : What is the value of variable c?
---
### 3. Multiplication : mutliplying multiple values or variables together
 * Operator: *
 * Examples:
```
 let product = 75 * 39;
 let j, k;
 j = 14;
 k = 92;
 let l = j * k * .5; 
```
 * Q : What is the value of variable l?
---
### 4. Division : dividing one or more values or variables by another
* Operator: /
* Examples:
```
 let quotient = 5016 / 6;
 let q, w;
 q = 46;
 w = 138;
 let p = (w / q) / 3; When there are multiple operations on a single line, the answer is calculated in the order of PEMDAS 
```
 * Q : What is the value of variable p?
---
### 5. Modulus : retrieving the remainder of one or more values or variables being divided by another
* Operator: %
*  Examples:
```
 let modulus = 33%15; the value of modulus would be 3, because 32 goes into 15 twice, with 3 left over.
 let h = 46;
 let i = 13;
 let g = h % i;  
```
* Q : What is the value of variable g?
---
### 6. Increment : increasing the value of a variable by 1 (adding 1)
* Operator: ++
* Examples:
```
 let someValue = 10;
 someValue++;
 let newValue = someValue++;
```
* Q : What is the value of the variable named newValue?
---
### 7. Decrement : decreasing the value of a variable by 1 (subtracting 1)
* Operator: --
* Examples:
```
 let someOtherValue = 90;
 someOtherValue--;
 let anotherNewValue = someOtherValue--;
```
* Q : What is the value of the variable named anotherNewValue?
---
* The operators can be used on fixed values: 
```
  let adding = 5 + 5;
  let subtracting = 10 - 5;
  let dividing = 40 / 5;
  let multiplying = 80 * 3;
  let modulos = 20 % 8;
 ```
* On variables: 
```
  Arithmetic operators can also be used on variables:
  let number = 50;
  let newAdding =  adding + number;
  let newSubtracting = subtracting - number;
  let newDividing = number / dividing;
  let newMultiplying = multiplying * number;
  let newModulos = number % modulos;
```
* Or on a mix of both fixed values and variables: 
```
  newAdding =  adding + 30;
  newSubtracting = subtracting - 23;
  newDividing = 5 / dividing;
  newMultiplying = multiplying * 7;
  newModulos = 24 % modulos;
```
--- 
### Note about the increment and decrement operators:
* Increment and decrement can either go before or after the variable name, for example:
```
myVar = 3;
myVar++ 
or
++myVar 
```
* When the increment operator happens after the variable, its the post-increment operator. If its before the variable, it's the pre-increment operator. 
---
Here’s the different:

```
let myVar = 2
document.write(myVar++)
document.write(myVar++)
document.write(myVar++)
console.log(myVar)

let myVar1 = 2
document.write(++myVar)
document.write(++myVar)
document.write(++myVar)
console.log(myVar1)
```

* The output of the first example is 234, because the document.write is executed before the value is updated. The variable is equal to 5 after the other operations. 

* The output of the second example is 345, because the document.write is executed after the value is updated. The variable is equal to 5 after the other operations. 
---
# Exercise 2.1

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="jENywyz" data-pen-title="Untitled" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/jENywyz">
  Untitled</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---