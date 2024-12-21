---
title: User Invoked Functions
weight: 3
---

[original slides](../old_presentation4_3)

<p data-height="600" data-theme-id="33744" data-slug-hash="03b0144de3b4e87bb7b7d61261a158c6" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="4.3 User Invoked Functions" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/03b0144de3b4e87bb7b7d61261a158c6/">4.3 User Invoked Functions</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation4_3)

### Invoking Functions  

The code inside of a function will not be executed until the function is told to do so.

When we tell a function to run, we are 'invoking' the function.

Functions can also be invoked by an event. When a specific event occurs, the function is ordered to execute. 

The event that invokes a function can be anything. Usually, you will see events such as button clicks triggering functions. For example, when a user fills out a form online and clicks the "submit" button, the function that sends the form's data is invoked and the data is sent to the correct location.

Functions can also be invoked by themselves, this is called self invocation.

We will visit each of these methods of invocation, beginning with user invocation:

To invoke a function we have written, or a function in the JavaScript library, we simply type the function's name, followed by a pair of parenthesis.

If the function requires parameters, we will provide the arguments for these parameters within the parenthesis after the function's name. Otherwise, we invoke functions without parameters by including the pair of empty parenthesis.

Examples:

1. A Simple Adding Function 

```js
    function adder(value1, value2, value3){
    return value1 + value2 + value3;
    }
```
 
the function, named adder, takes three parameters.

the function returns the sum of all three parameters.

the keyword "return" is the indicator of the last line of a function. If any code is placed beyond the return statement, the code will not be executed, as the function exits after executing its return statement. 

to invoke the function and retrieve the value it returns to us, we can either save the return value to a variable or print the value to the console, like so:

```js
function adder(value1, value2, value3) {
    return value1 + value2 + value3;
}

let sumOfNumbers = adder(45,67,23);
console.log(sumOfNumbers);

//  Or:

console.log(adder(45,67,23));
```
Both methods will achieve the same result, but you can see that the second option is more efficient

We can pass arguments directly into a function without having to store them as variables first. 

2. A Simple Current-Date Printing Function:
```js
function printDate() {
    let today = new Date();
    return today.getMonth() + " / " + today.getDate() + " / " + today.getFullYear();  
}
```
the function, named printDate, uses the JavaScript Date object methods getMonth(), getDate(), and getYear() to print the current date in this format: MM / DD / YYYY

to use the methods for the JavaScript Date object, we created a new variable named today and declared that it was a date object. You should remember objects from the lesson on data types. Objects can have methods that act like functions, which we will visit in a few lessons, so don't worry if you are confused about this function.

The purpose of this function(for us) is to see an example of a parameter-less function.

To invoke the printDate function, we simply save the return value to a variable or print the invocation to the console, like so:
```js
function printDate() {
    let today = new Date();
    return today.getMonth() + " / " + today.getDate() + " / " + today.getFullYear();  
}
let todaysDate = printDate();
console.log(todaysDate); 

or:

console.log(printDate()); 
```
Note that we did not pass in arguments in either method because the function does not have parameters.

Examples in Codepen:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="WbeRmej" data-pen-title="4.3 Example " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/WbeRmej">
  4.3 Example </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Exercise 4.3

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="pvzRYvp" data-pen-title="Exercise 4.3" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/pvzRYvp">
  Exercise 4.3</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>