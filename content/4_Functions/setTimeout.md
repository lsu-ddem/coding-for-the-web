---
title: setTimeout and setInterval
weight: 5
---

[original slides](../old_presentation4_5)

<p data-height="600" data-theme-id="33744" data-slug-hash="e63001f5784c5ecb48e1f04d6e5a8fc0" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="4.5 setTimeout and setInterval" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/dymGZXz/e63001f5784c5ecb48e1f04d6e5a8fc0">4.5 setTimeout and setInterval</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation4_5)

### setTimout and setInterval 

setTimeout and setInterval allow us to schedule events. 

#### setTimeout

The setTimeout method is a built-in function that allows you to execute a function after a certain amount of time has passed. 

First, let's write a function. This function will create an alert that prints out "5 seconds have passed." We will then write a setTimeout to run the function after 5 seconds. 

```js
function timedAlert() {
  alert("Five seconds have passed.");
}
setTimeout(timedAlert, 5000);
```

We previously learned that functions need to be invoked in some way, for example user invoked or event invoked. With the setTimeout method, we use setTimeout to invoke our function at a certain time. 

The syntax is setTimeout(functionName, milliseconds). So if we want to specify that our function should be invoked after five seconds, we would use 5000, as in the example above. 

Whenever the page is reloaded, the alert should pop up after 5 seconds.  

Let's create a second example. First, we will create a random number using our Math.floor(Math.random()) combination. Next, the function winningNumber() prints that number to the webpage, with the text " is the winning number". Finally, the function is invoked by the setTimeout method, 2 seconds after the page has loaded. 

```js
let rand = Math.floor(Math.random() * 10) + 1;

function winningNumber() {
  document.write(rand + " is the winning number!");
}

setTimeout(winningNumber, 2000);
```

Examples in codepen: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="GgKrLgO" data-pen-title="4.5 Example " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/GgKrLgO">
  4.5 Example </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### setInterval

If we wanted a function to execute over and over again, we could use the setInterval method. The syntax for that method is similar:

setInterval(functionName, milliseconds) In this case, the milliseconds are the interval between each invocation of the function. 

The next example function will create a new date object, then print it as a string in an alert. 

The set interval method will run the function every 6 seconds, so the date will update with every new alert. 
The function will continue to run every six seconds until the end of time (or until the page is closed!)

```js
function dateAlert() {
  let date = new Date();
  alert(date.toString());
}
setInterval(dateAlert, 6000);
```

Another example: 

```html
<div> changing color text </div>
<button onclick="killAlert()"> This Button will Kill the Alert </button>
```

```js
function changeTextColor() {
  let myDiv = document.querySelector("div");
  if (myDiv.style.color == "black") {
    myDiv.style.color = "pink";
  } else {
    myDiv.style.color = "black";
  }
}

setInterval(changeTextColor, 500);
```

In this example, the div from the HTML code is stored in a variable, using document.querySelector (which we will learn in the next section!). Then, an if statement checks whether the CSS color is equal to black. If it is, it changes the color to pink. If not, it changes it back to black. 

The setInterval invocation means that the color will change every half a second.

Examples in codepen: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="bNbgJEx" data-pen-title="4.5 Example_1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/bNbgJEx">
  4.5 Example_1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Clearing setTimeout and setInterval

setTimeout and setInterval can be cleared using clearTimeout and clearInterval. 

In order to use these methods in JavaScript, the original method has to be stored in a variable. 

This function will print out "Hello again" to the console every 4 seconds. The setInterval to invoke it will be stored in a variable

```js
function greeting() {
  console.log("Hello again");
}

let myGreeting = setInterval(greeting, 4000);

//Now that the setInterval is stored in a variable, clearInterval can be used to stop it, like this:

clearInterval(myGreeting);
```

Of course, it may not be that useful to immediately clear a setInterval immediately after creating it. A more useful way of using the clearInterval method would be to apply it to a button, so that a setInterval will run until a button is pressed. 

Codepen Example: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="MYgJRjN" data-pen-title="4.5 Example_2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/MYgJRjN">
  4.5 Example_2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Exercise 4.5

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="pvzRBNm" data-pen-title="Exercise 4.5" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/pvzRBNm">
  Exercise 4.5</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>