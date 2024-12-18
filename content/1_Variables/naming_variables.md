---
title: Naming Variables
weight: 2
---
[original slides](../old_presentation1_2)

<p data-height="600" data-theme-id="33744" data-slug-hash="a097ac9fdd7336bdde595ff8100a1476" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="1.2 Naming Variables" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/a097ac9fdd7336bdde595ff8100a1476/">1.2 Naming Variables</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation1_2)

## Naming Variables 
    
* Remember that we declare a new variable by typing the let keyword and then assigning a name to the variable. 
* A variable's name is also known as an identifier.
* In JavaScript, variables must be identified with a unique identifier. 
```
let blank;
```

* The identifier of the variable in the above example is "blank". 

* There are a few rules in regards to assigning variables' identifiers (in other words, rules for naming variables in JavaScript). 

---

### Rules for Naming Variables 

#### Rule 1
* Names must begin with a letter, an underscore, or a dollar sign $ (best coding practice starts names with a lowercase letter). 
* The letter of the first word in an identifier should always be lowercase, and the first word of any proceeding words should be uppercase. In other words, use camelcase!

---

#### Rule 2
* Names are case sensitive.
* If you declare a variable with the identifier myVariable, it cannot be accessed by saying myvariable or myVARIABLE

#### Rule 3 
* Reserved words cannot be used as names. 
* There are a few words used in JS that perform specific actions, such as the let keyword that tells the computer we are declaring a new variable
* Reserved words include JavaScript keywords, and all of the words included here: http:www.javascripter.net/faq/reserved.htm
---

The following are examples of acceptable identifiers(aka names):

```
let monthlyRent = 600;
let carNote$ = 300;
let home_address = "789 Super Fun Ln.";
let businessAddress2 = "326 City Rd.";
let lunchTotal$ = 11.49;
```

You probably noticed that the examples above are assigned to different types of data, as some store numbers while others store text. 
      
Next, we are going to discuss the different data types a variable can store.

---

## Exercise 1.2

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="wBwgdzB" data-pen-title="Exercise 1.2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/wBwgdzB">
  Exercise 1.2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
