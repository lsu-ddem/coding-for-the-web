---
title: Date Object and Methods
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

#### Date Object and Methods 

### Date Object 

A useful object in the JavaScript library is the Date object.

We now know the difference between primative and reference types, and we know that JavaScript treats primative types as objects(aka reference types) when using methods.

A date object, however, needs to be declared for us to work with dates.

We declare a date object by simply saying:

```js
let today = new Date();
```

Setting the variable equal to new Date(); constructs a new date object that the today variable is a reference to.

There may be an instance in which you wish to create a date object that does not represent the current time. 
To specify a date, we add the date we want within the parenthesis, in the order (Year, Month, Day, Hour, Minute, Seconds, and Milliseconds).
we do not have to provide all of these parameters, however.
For example, we can provide only the year, month, and day:

```js
let myBirthday = new Date(1997, 7, 29);
```

We can apply many useful methods to the date object. For most of these, our examples will be in codepen so that you can see the date in real time. 

### Date Methods 

See all the date methods here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date


#### 1. getFullYear : this method returns the year of the date object in a 4 digit format

syntax: .getFullYear()

examples:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="EaYZbvz" data-pen-title="3.7 Example" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/EaYZbvz">
  3.7 Example</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 2. getMonth : this method returns the month of the date object as a number. Months begin at 0, meaning January = 0 while December = 11

syntax: .getMonth()

examples:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="jENyaGx" data-pen-title="3.7 Example_1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/jENyaGx">
  3.7 Example_1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Because the month method gives us the month as a number starting at 0, we can easily create an array to convert our month into text. The following example demonstrates this approach. 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="EaYZbwB" data-pen-title="3.7 Example_2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/EaYZbwB">
  3.7 Example_2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

### 3. getDate : this method returns the day of the date object as a number from 1-31(out of the month)

syntax: .getDate()

examples:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="gbYgXXW" data-pen-title="3.7 Example_3" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/gbYgXXW">
  3.7 Example_3</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 4. getDay : this method returns the day of the date object as a number from 0-6 (as a weekday)

syntax: .getDay()

examples:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="yyBgPPR" data-pen-title="3.7 Example_4" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/yyBgPPR">
  3.7 Example_4</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 5. getHours : this method returns the hours of the date object as a number from 0-23

syntax: .getHours()

examples:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="qEWRVpE" data-pen-title="3.7 Example_5" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/qEWRVpE">
  3.7 Example_5</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 6. getMinutes : this method returns the minutes of the date object as a number from 0-59

syntax: .getMinutes()

examples:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="mybRqpR" data-pen-title="3.7 Example_6" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/mybRqpR">
  3.7 Example_6</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 7. getSeconds : this method returns the seconds of the date object as a number from 0-59

syntax: .getSeconds()

examples:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="KwPayZB" data-pen-title="3.7 Example_6" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/KwPayZB">
  3.7 Example_6</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Note: try reloading this pen, the seconds will be different!

#### 8. setDate() : this method sets the day of the date object as a number from 1-31. You can use this method to add or subtract days from any Date

syntax: .setDate()

examples:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="gbYgXvW" data-pen-title="3.7 Example_7" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/gbYgXvW">
  3.7 Example_7</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 9. setFullYear() : this method sets the year of the date object. You can use this method to add or subtract years from any Date

syntax: .setFullYear()

examples:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="EaYZbQq" data-pen-title="3.7 Example_7" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/EaYZbQq">
  3.7 Example_7</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 10. all of the Set Methods

setDate()  Set the day as a number (1-31)

setFullYear()	Set the year (optionally month and day)

setHours()	Set the hour (0-23)

setMilliseconds()	Set the milliseconds (0-999)

setMinutes()	Set the minutes (0-59)

setMonth()	Set the month (0-11)

setSeconds()	Set the seconds (0-59)

setTime()	Set the time (milliseconds since January 1, 1970)

### Exercise 3.7 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="NPKdwYY" data-pen-title="Exercise 3.7" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/NPKdwYY">
  Exercise 3.7</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>