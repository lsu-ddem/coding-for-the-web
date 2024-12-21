---
title: String Operators
weight: 3
---
[original slides](../old_presentation2_3)

<p data-height="600" data-theme-id="33744" data-slug-hash="d28fddfedf3b86c3d25e93af1f7ae649" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="2.3 String Operators" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/d28fddfedf3b86c3d25e93af1f7ae649/">2.3 String Operators</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation2_3)

### String Operators 

* JavaScript's string operators are used to attach strings to one another, or to attach variables to strings.
* String operators each have a symbol known as the operator that is used to perform the operation

#### 1. Concatenation : concatenate is another word for add. Concatenating two strings simply means adding or attaching them to one another.
* Operator: + 
* Examples:
```
x = "My name is ";
y = "Hulk Hogan, ";
z = "Brothur";
var sentence = x + y + z;
```
* Q : What is the value of the variable sentence?
---
* Note that this operator (+) is also used for numerical addition. 
* You may ask how you are supposed to specify that you are adding strings instead of numbers, and the answer is that you do not have to. 
* If any value you are adding is a string, the compiler automatically uses the + operator to concatenate values to the string, even if they are numbers. The result is a string. For example:
```
var cents = 93;
var sentenceWithNumbers = "I have " + 16 + " dollars and " + cents + " cents.";
console.log(sentenceWithNumbers);
```
* The result of this code in the console would be:

<img src="../../media/2_3_concat.png" alt="Image description" width="400">

* Note that between each value or variable added, another addition sign needs to be used to concatenate the entire string. 
---
* It is good practice to pay attention to where spaces should be inserted so that the sentence's formatting is not confusing and bunched together when the string is printed out.
* Typically if you are printing a string and then a new variable or string, you want to make sure there is a space included at the end of the first string, or the beginning of the second.  
* If a numeric value is printed before another or before a string, you can concatenate a single space before the next number, or include a space in the beginning of the next string
---
#### 2. Concatenate-Equals : assigning a variable to its original value plus some specified value concatenated to it
* Operator: += 
* Examples:
```
x = "My name is ";
y = "Hulk Hogan,";
z = "Brothur";
var sentence = x + y + z;
x += y + z;
```
* Q : What is the value of variable x? Is this equal to the value of sentence?

#### Exercise 2.3

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="LEPxjQz" data-pen-title="Exercise 2.3" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/LEPxjQz">
  Exercise 2.3</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

