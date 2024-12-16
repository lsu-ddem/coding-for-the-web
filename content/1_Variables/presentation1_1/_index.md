---
title: Javascript intro
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
weight: 2
separator: "---"
---

# JavaScript 

* The first concept in JavaScript we will visit is variables
we will look at their use as well as there syntax

* Syntax - simply means the rules or guidelines for doing something in a language, in our case a programming language.

* Note to all students: make sure that you read, and take notes.
--- 

# Declaring variables 

* Variables are the used in programming the same way they are used in math: as storage containers for some kind of data. 
* Creating and storing a variable is called "declaring" a variable.
* To declare a new variable, you need at least 2 things.

1. the JavaScript keyword `var`, `let`, or `const` 
which specifies that you are assigning a new variable
2. a name for the variable (called an identifier) 
that adheres to naming rules discussed in the next segment

---

# Variables 

* The reason a variable needs at least 2 components is because 
variables can be created without being assigned to a value yet.
* Whenever we declare variables without assigning them to a value, their value is automatically "undefined." For example:

```
let myVariable;
let weeklyIncome; 
```
* if we tried to print the value of either of these two variables, we would see "undefined"

--- 

# Assigning Variables

* If we know the value we want to set a variable to when we are creating it, we can simply declare a new variable and set it equal to this value
(this is called "assigning" the variable to a value), like this: 

```
let year = 2018;
let placeHolder = "This is an example of a variable.";
```
--- 

* If we had declared a variable without assigning its value (an undefined variable), and now we know what we would like to set the variable equal to,
we can simply call the variable name and set it equal to that value, like so:

```
myVariable = "random words!";
weeklyIncome = 700;
```

* We do not need to use the "var" keyword again because we have already declared that myVariable and weeklyIncome 

* To check that these variables now store the new values, we can print them to the console, or write them to the webpage. 
  
--- 

# The Console

* The `console` is used in programming for troubleshooting, finding bugs, keeping code organized, and ensuring accuracy.
* To view the console on codepen, simply click the console button in the bottom left corner

--- 

# Accessing the Console in your Browser

* If you are not on codepen's website, you can view the console by right clicking the webpage and clicking 'inspect' or 'inspect element' and selecting the console tab:

*  Google Chrome: right click webpage, select 'inspect element', click on 'console' tab

* Mozilla Firefox: right click webpage, select 'inspect element', click on 'console' tab

* Safari: right click webpage, select 'inspect element', click on 'console' tab
---

# Console.log

* To print something to the console, we place it in the quotation marks of the console print statement:
```
console.log("Hello, Patrick");
```
* After the line above is read by the computer, "Hello, Patrick" will be printed to the console.

* We can print our variables to check that they print the new values we assigned them:

```
console.log(myVariable);
console.log(weeklyIncome);
```

---

# Writing to the Webpage

* Later on in the course, we’ll learn how to visually create a webpage using HTML and CSS (Which we’ve already seen in the instagram project!). But for now, we can use the document.write() method to display text on the webpage. 

```
document.write(weeklyIncome)
document.write(myVariable)
```
--- 

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="jENyBdP" data-pen-title="1.1 Examples" data-preview="true" data-editable="true" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/jENyBdP">
  1.1 Examples</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---

# Reassign Variables 

* We can reassign the value of a variable as many times as we would like:

```
myVariable = "this is assigned to a new value";
myVariable = "now it's assigned to an even newer value";
```

*  We can even assign the value of a variable to that of another variable like so:

```
weeklyIncome = myVariable;
```

* If we print weeklyIncome to the console, we would see "now it's assigned to an even newer value"

---

# The Let keyword

* The latest version of JS has replaced the `var` keyword with `let`, so the declaration of variables will from here on use `let` instead of `var`,

* It is important to note that these keywords are interchangeable, because many of the older examples that you find online utilize `var`
---

# Coding style

* Before we continue, it is important to pay attention to your coding style.
* Your coding style is the way you format and structure the code you write.
* It is imperative that you pay attention to the structure and organization of your code in the beginning of your practice with programming, so that you become accustomed to writing clean code
* Clean code is important because it makes it easier to read your code, not only for you but for others viewing your code(teacher) or working on your code after you(group work)
* Clean code also allows us to troubleshoot more easily because we can pinpoint problem areas. This is harder to do with unorganized or 'spaghetti' code
---

# Good Conventions to Follow

1. Use "camelCase" for naming variables(covered more in depth in the next section). camelCase is the practice of keeping the first word lowercase, and having the rest of the words begin with an uppercase letter,
        
Example: camelCase, javaScript, myThirdExample
      
2. Put spaces before and after operators (+, -, *, /, %, etc) and put a space after commas. This helps with readability.
    
Example: 
```
let priceOfGoods = 200 + (5 - 27) / 30; 
``` 
3. When you are indenting, use 4 spaces for each indention, aka tab.
    
There are conventions and syntax rules we will cover later on that are specific to different topics in JavaScript, which will be covered in later segments.

---

# Exercise 1.1

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="gbYgWOy" data-pen-title="Exercise 1.1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/gbYgWOy">
  Exercise 1.1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

