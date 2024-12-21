---
title: Array Methods
weight: 6
---

[original slides](../old_presentation3_6)

<p data-height="600" data-theme-id="33744" data-slug-hash="377859247834a2a3f0bb93b699568cb9" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="3.5 Array Methods" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/377859247834a2a3f0bb93b699568cb9/">3.5 Array Methods</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


[slides](../presentation3_6)

### 3.6 Array Methods

3.6 Array Methods

#### 1. to String : Arrays also have a .toString() method, and just like we can create arrays from a string, we can create a string from an array. The string contains the elements of the array separated by commas

syntax: .toString()

examples:

```js
let colors = ["Red", "Orange", "Yellow", "Green", "Blue", "Indigo", "Violet"];
console.log("The colors that makeup the rainbow are " + colors.toString());
```

Console view: 

<img src="../../media/3_6_1.png" alt="Image description" width="600">

#### 2. Join : Similar to the toString() method, the join method creates a string from an array, but allows us to specify a different separator than the comma:

syntax: .join()

examples:

```js
colors = ["Red", "Orange", "Yellow", "Green", "Blue", "Indigo", "Violet"];
console.log("The colors that makeup the rainbow are " + colors.join(" and "));
```

Console view: 

<img src="../../media/3_6_2.png" alt="Image description" width="600">

#### 3. push : push is a method that allows us to 'push' a new element into an array. The element is added at the last index.

syntax: .push()

examples:

```js
colors = ["Red", "Orange", "Yellow", "Green", "Blue", "Indigo", "Violet"];
colors.push("White");
colors.push("Black");
console.log(
  "New colors were added to the list : " + colors[7] + " and " + colors[8]
);
```

Console view: 

<img src="../../media/3_6_3.png" alt="Image description" width="600">

#### 4. shift : shift is a method that allows us to remove the first element of an array. The element is completely removed from the array, not just accessed. This means that the rest of the elements shift up one position/index. The element is returned to us and is no longer in the array.

syntax: .shift()

examples:

```js
colors = ["Red", "Orange", "Yellow", "Green", "Blue", "Indigo", "Violet"];
console.log("The first color in the list is : " + colors.shift());
console.log(
  "We removed Red from the list, so now the colors are " + colors.toString()
);
```
Console view: 

<img src="../../media/3_6_4.png" alt="Image description" width="600">

#### 5. unshift : unshift is a method that inserts a new element at the beginning of an array, and increases the rest of the elements' indexes by 1

syntax: .unshift()

examples:

```js
colors = ["Orange", "Yellow", "Green", "Blue", "Indigo", "Violet"];
console.log("I'm adding Red to the front of the array ");
colors.unshift("Red");
console.log("Now the colors are back to normal : " + colors.toString());
```
Console view: 

<img src="../../media/3_6_5.png" alt="Image description" width="6 00">

#### 6. sort : sort is a method that sorts the elements of an array alphabetically

syntax: .sort()

examples:

```js
let letters = ["P", "M", "E", "T", "N", "X", "J", "I"];
console.log("Letters unsorted: " + letters.toString());
console.log("Letters sorted: " + letters.sort().toString());
```
Console view: 

<img src="../../media/3_6_6.png" alt="Image description" width="400">

#### 7. reverse : reverse is a method that reverses the order of the elements within an array

syntax: .reverse()

examples:

```js
let order = ["First", "Second", "Third", "Fourth", "Fifth"];
console.log("Original order: " + order.toString());
console.log("Reversed order: " + order.reverse().toString());
```
Console view: 

<img src="../../media/3_6_7.png" alt="Image description" width="400">

### Exercise 3.6

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="VYZPrpv" data-pen-title="Exercise 3.6" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/VYZPrpv">
  Exercise 3.6</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>