---
title: Math Methods
weight: 8
---

[original slides](../old_presentation3_8)

<p data-height="600" data-theme-id="33744" data-slug-hash="3152fff055f35dc243b7ab612dfa03ec" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="3.7 Math Methods" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/3152fff055f35dc243b7ab612dfa03ec/">3.8 Math Methods</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation3_8)

### Math Methods

The JavaScript Math object has a lot of useful methods that are worth mentioning.

To use the Math methods, we don't have to construct a new Math object.

All we do is include the Math object name, and then invoke the method, such as:

```js
let roundUp = Math.round(9.8); //here we invoked the round method. This would round 9.8 to 10.
```

There are a few constants loaded into the JS Math object's properties.

These include: 

1. PI : Math.PI

2. Euler's constant : Math.E

3. Natural log base 10: Math.LN10

More : https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math

The Math object also has many methods, but we will only cover the ones you will likely use most

If you'd like to see a full list of the Math object's methods, go to https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math

#### 1. Exponents:

Syntax: Math.pow(x,y) where x is the base and y is the exponent

Examples:

```js
let value = Math.pow(5, 2); 
let newValue = Math.pow(value, 2);
```
Q : What would value and newValue be equal to?

#### 2. Random:

Syntax: Math.random()

When Math.random() is used without any arguments, it returns a random floating point value between 0 and 1:

Examples:
```js
console.log("Here is a random number " + Math.random()); // A random number between 0 and 1 would be printed in the console. 
```
However, we can specify the values we want the random number to be within range of using the next method:

#### 3. Floor:

Syntax: Math.floor()

Math.floor() is used to return the largest whole number that is less than or equal to a specified value. We use this method to get a random whole number within a specific range of numbers, such as 1-10:

Examples:

For Jesse
I have always had an issue with this way of making a range for random numbers, because if you want a number start at 5 and go to 10, you would have to multiply by 5 and then add 5 instead of multiplying by 10 and adding 6... so it only really works if you're going between 1 and something, so I just feel like the way we explain it is a bit misleading. Obviously the best way to do it is with a function, but I'm wondering if we don't include the Math.floor((Math.random() * maxRangeValue) + minRangeValue)

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="qEWRVMO" data-pen-title="3.8 Example " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/qEWRVMO">
  3.8 Example </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 4. Round:
Syntax: Math.round(x) rounds the value x to the nearest whole number
Examples:
```js
let roundMeUp = Math.round(5.7); 
let roundMeDown = Math.round(7.3);
```
Q : What would the values of roundMeUp and roundMeDown be? 

#### 5. Exponential Function:
Syntax: Math.exp(x) raises E to the x power
Examples:
```js
let raised = Math.exp(5); // the value of this will be 148.4131591025766
```
#### 6. Absolute Value:
Syntax: Math.abs(x) returns the absolute value of the variable or value in parenthesis
Examples:

```js
let positive = Math.abs(-10);
let negative = -20;
let absoluteVal = Math.abs(negative / 2);
```
Q : What would the value of absoluteVal be? 

#### 7. Square Root:
Syntax: Math.sqrt(x) returns the square root of the value or variable in parenthesis
Examples:

```js
let sqrt = Math.sqrt(25);
sqrt = Math.pow(sqrt, 2);
```
Q : What would the value of sqrt be? 

#### 8. Trigonometric Functions:
Syntax:
Sin : Math.sin(x)
Tan : Math.tan(x)
Cos : Math.cos(x)

Arcsin : Math.asin(x)
Arctan : Math.atan(x)
Arccos : Math.acos(x)

Though there are a number of methods for the Math object that we didn't cover, you likely won't need to use them as a beginner programmer. Still, you can read about them here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math
and:
https://www.w3schools.com/js/js_math.asp

### Exercise 3.8

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="pvzRdxQ" data-pen-title="Exercise 3.8" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/pvzRdxQ">
  Exercise 3.8</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
