---
title: Flex Box
weight: 6
---

[slides](../presentation5_6)


<p data-height="600" data-theme-id="33744" data-slug-hash="9f014a39f945e70cc4065a829c767e81" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="5.6 Flex Box" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/GRQbWNw/9f014a39f945e70cc4065a829c767e81">5.6 Flex Box</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


### Flexbox

* Positioning items in CSS can be one of the most challenging aspects of web design, due to many different screen sizes and alignments. Flexbox is an efficient way of managing webpage layout and aligning elements. 

* The main idea is to give the outside container the ability to alter the width/height of its elements in order to best fill the available space (this can allow webpages to work well on different devices and screen sizes!)

#### Terminology:

* Before we get started, its important to understand a few key terms that will be used to describe these processes.

* parent and child - you may have already heard these terms. A child is any element that belongs to another element, which would be its parent element, for example the div with the id "mySubDiv1" is a child of its parent div, "myDiv". 

* When using flexbox, there is a parent element, called the flex container, and child elements, called the flex items. 

* Properties for the parent (flex container):

* Our parent and child elements for our flexbox layout can first be created in HTML, like this:

```html
<div class="flex-container">
  <div class="flex-items" id="number1" >1</div>
  <div class ="flex-items">2</div>
  <div class ="flex-items">3</div> 
  <div class ="flex-items">4</div> 
  <div class ="flex-items">5</div> 
</div>
```

* By adding the property display, with the value flex, in CSS, various flex properties can be used, like so:

```css
.flex-container {
  display: flex;
}
```

* We will go through these properties, showing codepen examples for each one. 

* For each example, we will use a styling for the flex items and the flex container that make it easy to see what is happening. 

#### flex-direction 

* This  defines in which direction the container wants to stack the flex items. (e.g vertial or horizontal) Common ways to set it are column or row. Row is the default, we can set it to column like this:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="XJrRPpw" data-pen-title="5.6 Example " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/XJrRPpw">
  5.6 Example </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

* comment out the line of code that sets flex-direction: column to see the default row view. 

#### flex-wrap

* This property specifies whether the flex items should wrap or not. This controlls whether they will "wrap" onto multiple lines, or be forced onto one line. Some values would be : wrap and nowrap. nowrap is the default! If you don't specify, then your flex items will stay on the same line!

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="ByBROWm" data-pen-title="5.6 Example " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/ByBROWm">
  5.6 Example </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

#### flex-flow

* flex-flow is a shorthand for both wrap and direction, so both could be specified, like so:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="azoWaWo" data-pen-title="5.6 Example_1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/azoWaWo">
  5.6 Example_1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

* notice that while this looks the same as the previous example, the numbers are in a different order becuase they are in columns, not rows

#### justify-content

* The justify-content property is used to align the flex items along the "main axis" (in a row layout, this is the x axis, in a column layout, its the y axis!) It will move all of the flex items to the the center, or to the left, or make space between them etc. 

- The center value aligns the flex items at the center of the container.
- The flex-start value aligns the flex items at the beginning of the container (this is default).
- The flex-end value aligns the flex items at the end of the container.
- The space-around value displays the flex items with space before, between, and after the lines.
- The space-between value displays the flex items with space between the lines.

* For the justify content example, we are making our parent div take up the whole page, so you can clearly see the difference. Try out each different value and see what happens. 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="mybmGmW" data-pen-title="5.6 Example_2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/mybmGmW">
  5.6 Example_2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

#### align-content

* The align-content property is used to align the flex items along the cross axis. (the other axis that isn't the main axis!)

- The space-between value displays the flex lines with equal space between them.
- The space-around value displays the flex lines with space before, between, and after them.
- The stretch value stretches the flex lines to take up the remaining space (this is default).
- The center value displays display the flex lines in the middle of the container.
- The flex-start value displays the flex lines at the start of the container.
- The flex-end value displays the flex lines at the end of the container. 

* Example: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="ZYzKMKP" data-pen-title="5.6 Example_3" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/ZYzKMKP">
  5.6 Example_3</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

* Note: this property will only be useful when you have multiple rows wrapping onto different lines 

#### align-items

* The align-items property is used to align the flex items with themselves. This will only make a difference if some of the flex items are different sizes.

- The center value aligns the flex items in the middle of the container.
- The flex-start value aligns the flex items at the top of the container.
- The flex-end value aligns the flex items at the bottom of the container.
- The stretch value stretches the flex items to fill the container (this is default).

* In this example, the height of the first item will be reduced to show the different possibilities of align items. 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="xbKdaLb" data-pen-title="5.6 Example_4" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/xbKdaLb">
  5.6 Example_4</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

* Again, try out the different options to see what happens!

#### Flex Items:

* As well as flex container properties, there are a number of flex item properties that can be used to control the layout of the flex items. 

* For these examples, we will use a different layout. The styling for the outside container will be the same for each one. 

#### order

* The order property specifies the order of the flex items. The default is 0, so if no order property is specified, each will have an order of 0. If the first div is given an order of 1 it will be last, unless anything has an order greater than 1. 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="jENmvwv" data-pen-title="5.6 Example_6" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/jENmvwv">
  5.6 Example_6</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

#### flex-grow:

* The flex-grow property specifies how much a flex item will grow relative to the rest of the flex items.

* The value must be a number, the default value is 0.

* If we give the third item a flex-grow value of 1, it will be larger than the other two items. 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="KwPmxvG" data-pen-title="5.6 Example_6" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/KwPmxvG">
  5.6 Example_6</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

Read about more properties here: https://www.w3schools.com/css/css3_flexbox_items.asp

### Exercise 5.6

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="MYgmqvL" data-pen-title="Exercise 5.6" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/MYgmqvL">
  Exercise 5.6</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>


















