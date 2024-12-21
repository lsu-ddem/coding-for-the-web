---
title: Number Methods
weight: 5
---

[original slides](../old_presentation3_5)

<p data-height="600" data-theme-id="33744" data-slug-hash="9e712d38fdce87429b1536064a5f8422" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="3.4 Number Methods" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/9e712d38fdce87429b1536064a5f8422/">3.4 Number Methods</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation3_5)

### Number methods 

#### 1. to String : this method converts a numeric value to a string

syntax: .toString()

examples:

```js
let randomNumber = 3124325454352;
console.log(randomNumber);
console.log(randomNumber.toString());
console.log((21414 + 234234).toString());
```
Console view: 

<img src="../../media/3_5_1.png" alt="Image description" width="300">

In the console image, you'll see that before we converted it to a string, randomNumber was printed as a numeric value, without quotation marks.


Remember that when numbers are concatenated to strings, they become strings themselves. So, there is no reason to use the .toString method during string to number concatenation.


This method comes in handy when using functions or methods that require a string parameter and thus the number needs to be converted to a string.

#### 2. to Exponential : this method converts a numeric value to a string that contains the exponential notation of the value

syntax: .toExponential(n)

examples:

```js
 let x = 3.2526;
 console.log(x);
 console.log(x.toExponential(2));
 console.log(x.toExponential(4));
```

Console view: 

<img src="../../media/3_5_2.png" alt="Image description" width="300">

#### 3. to Fixed : this method converts a numeric value to the same numeric value with the specified number of decimal places included. This is useful when dealing with values such as money or scores.

syntax: .toFixed(n)

examples:

```js
 let payCheck = 3000;
 let groceries = 240.247;
 let utilityBill = 139.26;
 let cellPhone = 45.206;
 let savings = 1000;
 let spendingMoney = payCheck - groceries - utilityBill - cellPhone - savings;
 console.log("This is how much money I have left: $" + spendingMoney);
 console.log("But it makes more sense to round money to two decimal places, like this : $" + spendingMoney.toFixed(2));
```
Console view:

<img src="../../media/3_5_3.png" alt="Image description" width="200">

## 4. to Precision : this method converts a numeric value to a string with a specified length. It is essentially the same as the .toFixed() method, but the return type is a string. And instead of specifying the number of decimal places, we are specifying the number of characters in total, or the length of the string:
      syntax: .toPrecision(n)
      examples:
```js
let grade = 87.2267;
console.log("My grade is " + grade.toPrecision(4));
console.log("My grade is " + grade.toPrecision(3));
console.log("My grade is " + grade.toPrecision(2));
```
Console view: 

<img src="../../media/3_5_4.png" alt="Image description" width="200">


### Exercise 3.5

 <p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="bNbgYER" data-pen-title="Exercise 3.5" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/bNbgYER">
  Exercise 3.5</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

