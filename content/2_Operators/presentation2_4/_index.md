---
title: Comparison Operators
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---
# Comparison Operators 

* JavaScript's comparison operators are used in logical/conditional statements to determine if variables are equal to, less than, greater than, etc. another value or variable.
* Comparison operators each have a symbol known as the operator that is used to perform the operation.

## 1. Equal To : used to test whether a variable's value is equal to another variable's value or a fixed value
* Operator: ==
* Examples:
```
let example = 5;
let val = 6;
example == 10 //(false) This line translates to "is the value of example equal to 10?"
example == 5 //(true)
example == val //(false)
val = 5;
example == val 
```
* Q : What is the result of the comparison on the last line (true or false)?
---
# 2. Equal Value and Type : used to test whether a variable's data type and assigned value are equal to another variable or fixed value's assigned value and data type(it checks BOTH, if one is not the same, it is overall not equal)
* Operator: ===
* Examples:
```
example = 5;
val = "5";
example === val; //false; This line translates to "is the value of example equal to 10 the value of val, AND are the data types the same?"
example += val;
example === val;
```
* Q : What is the result of the comparison on the last line (true or false)?
---
# 3. Not Equal : used to test whether a variable's value is NOT equal to another variable's value or a fixed value. If it is not equal, it returns true. If the values are equal, it returns false.
* Operator: !=
* Examples:
```
example = 29;
val = 28;
example != val; //true; This line translates to "is the value of example not equal to the value of val? 
example != val++;
example-- != val;
```
* Q : What is the result of the comparison on the last line (true or false)?
---
# 4. Not Equal value or not equal type : used to test whether a variable's value OR data type is NOT equal to another variable's value and data type or a fixed value's value and data type. If either the values or types are not equal, it returns true. If the values are equal, it returns false.
* Operator: !==
* Examples:
```
example = 10;
val = "10";
example !== val; //true; This line translates to "is the value of example not equal to the value of val, and is the data type of example also not the same as the data type of val? 
val = 11;
val--;
example !== val;
```
* Q : What is the result of the comparison on the last line (true or false)?
---
# 5. Greater Than : used to test whether a value or variable is greater than another value or variable
* Operator: >
* Examples:
```
example = 300;
val = 295;
example > val; //true; This line translates to "is the value of example greater than the value of val?"
val * 5;
example > val; //false
example = 300 * 3 % val;
```
* Q : What is the result of the comparison on the last line (true or false)?
---
# 6. Less Than : used to test whether a value or variable is less than another value or variable
* Operator: <
* Examples:
```
example = 46;
val = 13;
example < val; //false; This line translates to "is the value of example less than the value of val?"
(example % val) < val; //true
(val % example) < example; 
```
* Q :  What is the result of the comparison on the last line (true or false)?
---
# 7. Greater Than or Equal To : used to test whether a value or variable is greater than or equal to another value or variable
* Operator: >=
* Examples:
```
example = 50;
val = example;
example++ >= val;//true; This line translates to "is the value of example+1 greater than or equal to the value of val?"
example-- >= val++; 
```
* Q :  What is the result of the comparison on the last line (true or false)?
---
# 8. Less Than or Equal To : used to test whether a value or variable is less than or equal to another value or variable
* Operator: <=
* Examples:
```
example = 20;
val = example*example;
example <= val;//true; This line translates to "is the value of example less than or equal to the value of val?"
example += val/2;
val <= example;
```
* Q :  What is the result of the comparison on the last line (true or false)?
---

# Exercise 2.4

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="mybRMGG" data-pen-title="Exercise 2.4" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/mybRMGG">
  Exercise 2.4</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>