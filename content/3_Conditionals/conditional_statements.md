---
title: Conditional Statements
weight: 1
---

[original slides](../old_presentation3_1)

<p data-height="600" data-theme-id="33744" data-slug-hash="13781480ff73bc907eaa31ab76c06ddc" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="3.1 Conditional Statements" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/13781480ff73bc907eaa31ab76c06ddc/">3.1 Conditional Statements</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation3_1)

### Conditional Statements 

* Conditional Statements use operators to test different expressions, and execute code according to the outcome of the expressions.
* There are four types of conditional statements in JavaScript: If statements, Else statements, Else if statements, and switch statements.
* Conditional statements can be nested within each other, so that another expression can be tested after one has been proven true or false, to determine the next course of action for the program.

#### 1. If statements 

* If statements are pretty self explanatory. The statement tests "if" a condition within the parentheses is true. If the condition is true, the code is executed. Like so:
```
if (5 < 6) {
  document.write("Our first if statement!");
}
```
* The expression within the parenthesis is the condition being tested. Since the expression is true, the code executes. 

* All of the conventions for using conditional and logical operators remain true when we use them in if statements.
* Examples:

```
let name = "Bob";
if (name === "Bob") {
  console.log("Hi Bob!");
}

x = 20;
y = 30;
if (x > 10 && y < 50) {
  console.log("True!");
}
```
* Q : Will these if statements execute or not? 


#### 2. Else statements 

* Else statements follow if statements and/or else-if statements(covered next).
* Else statements are literally saying "if that condition was not true, execute this code"
* Example:
```
let secondName = "Todd";
if (secondName === "John") {
  console.log("Hello, John!");
} else {
  console.log("Hi, " + secondName);
}
```
* Running this code will print "Hii, Todd" to the console because the else statement was executed since the variable 'name' was not equal to "John".
* More examples:
<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="LEPxzVr" data-pen-title="3.1 Examples " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/LEPxzVr">
  3.1 Examples </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
---

#### 3. Else-if statements 

* Else-if statements are used in between if statements and else statements to test for an extra condition before running the "else code".
* In other words, if the if statement proves false, the next expression evaluated will be the else if, which will test for a new condition.
* If the else if is also false, the next else if expression is evaluated, or the else code is executed.
* We can have multiple else if statements before the final else statement
---
* Example:
```
let name1 = "Todd";
let name2 = "Katy";
let name3 = "Max";
if (name1 == "Katy") {
  console.log("Hi, Katy!");
} else if (name1 == "Max") {
  console.log("Hi, Max!");
} else {
  console.log("Hi, " + name1);
}
```
* "Hi, Todd" is printed to the console because the first if statement and else if statement proved false, so the else statement was executed.
--- 
* Further Examples: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="wBwgrzB" data-pen-title="3.1 Examples_1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/wBwgrzB">
  3.1 Examples_1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


* As mentioned, conditional statements can be nested within each other. For example:

```
let color = "purple";
if (color == "red") {
  console.log(color);
} else if (color == "purple") {
  if (5 > 6) {
    console.log("First nested if-statement was true");
  } else {
    console.log("First nested if-statement was false");
  }
}

```
* Q : What will be printed to the console when this code runs?

### Exercise 3.1

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="qEWRPRy" data-pen-title="Exercise 3.1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/qEWRPRy">
  Exercise 3.1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
