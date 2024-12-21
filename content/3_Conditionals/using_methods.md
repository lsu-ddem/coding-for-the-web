---
title: Using Methods
weight: 3
---

<p data-height="600" data-theme-id="33744" data-slug-hash="f4ab3783e7bdb874c9d0b1de1f45849a" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="3.2 Using JS Objects and Methods" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/f4ab3783e7bdb874c9d0b1de1f45849a/">3.2 Using JS Objects and Methods</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

[slides](../presentation3_3)


### Using JS Objects and Methods 

* In lesson 1.3 discussing data types, we learned how to create objects in JavaScript.
* Remember that objects store multiple values within one variable, and their values are attributed to their "properties"
* We can obtain the value of an object's property by typing the objectName.objectProperty
* There is a difference between typical variables and objects that we have not yet discussed, and that is the difference between primitive values and reference values.
* Primitive values are simply values stored to variables without creating new objects.
* For all of the types of variables we have created so far, there was a way for us to declare those variables as objects. 
* If we declare variables as objects, they would be of the reference type instead of primitive.
* For example, lets simply declare a new variable that stores a string of text:

```js
let primitiveWords = "Have a really great day, like maybe even the best day ever, because why not.";
```
* The variable 'primitiveWords' is a string primitive. 
* JavaScript identifies six data types as primitive: undefined, null, boolean, number, string, and symbol.
That means the following variables are also primitive types:

```js
let year = 2018;
let snowyOutside = false;
let randomVariable;
let placeHolder = null;
```

* Now lets create the reference type equivalent of the primitive variable 'words':

```js
let referenceWords = new String("Have a really great day, like maybe even the best day ever, because why not.");
```

* the variable referenceWords is a String Object.
* The purpose of learning about the difference between primitive and reference types is to understand the use of JavaScript methods.
* JavaScript methods exist for the different objects in the JavaScript library.
* An object's method is essentially a function that was programmed as a property of that object, and therefore we can invoke the function similarly to how we retrieve any property of an object: objectName.objectMethod()
* We have not yet covered functions, so we will not learn about writing object methods until the next section.
* Instead, this lesson focuses on using the object methods already built into the JavaScript library.
* Let's start with the String Object and its methods:
* As you saw, we can create a reference type variable that stores a string object.
* On this object, we can use the methods created for JavaScript String Objects, such as:

.length : returns the length of a string\

.indexOf("word") : returns the index of the first occurrence of the specified text within quotes

.slice(start, end) : splits a string into two strings, the new string containing the text within the start and end indexes 

* For example:

```js
let referenceWords = new String("Have a really great day, like maybe even the best day ever, because why not.");
console.log(referenceWords.length); // this prints 76 to the console
console.log(referenceWords.indexOf("great"));  // this prints 14 to the console
console.log(referenceWords.indexOf("why"));  // this prints 68 to the console
```

* However, if I try to use these methods with the primitiveWords variable....

```js
let primitiveWords = "Have a really great day, like maybe even the best day ever, because why not.";
console.log(primitiveWords.length);  // this prints 76 to the console
console.log(primitiveWords.indexOf("great"));  // this prints 14 to the console
console.log(primitiveWords.indexOf("why"));  // this prints 68 to the console
 ```

* The methods still work even though primitiveWords is a primitive type!!!
* This is because, whenever these methods are invoked, JavaScript treats primitive values as objects in order to use the many methods in the JS library.
* This means that we can apply the JavaScript methods for most objects to their primitive equivalent.
* The rest of this module will cover pre-existing methods that can be used on different types of objects. 

### Exercise 3.3

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="jENyGKB" data-pen-title="Exercise 3.3" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/jENyGKB">
  Exercise 3.3</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
