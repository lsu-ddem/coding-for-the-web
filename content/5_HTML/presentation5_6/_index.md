---
title: Flex Box
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

### Flexbox

There are different ways to position elements on a page! Flexbox is an efficient way of managing webpage layout and aligning elements. 

The main idea is to give the outside container the ability to alter the width/height of its elements in order to best fill the available space (this can allow webpages to work well on different devices and screen sizes!)

Terminology:

Before we get started, its important to understand a few key terms that will be used to describe these processes.

* parent and child - you may have already heard these terms. A child is any element that belongs to another element, which would be its parent element, for example the div with the id "mySubDiv1" is a child of its parent div, "myDiv". 

* When using flexbox, there is a parent element, called the flex container, and child elements, called the flex items. 

Properties for the parent (flex container):

In HTML, we can set up the elements for the flex-container. We will use a div as our flex container, and  set the class to flex-container. Then, some child divs inside will be added, which for this example have the text 1, 2, and 3 in them. 

By adding the property display, with the value flex, in CSS, various flex properties can be used, like so:
*/

.flex-container {
  display: flex;
  width: 500px;
  height:500px;
  background-color: blue
}

/*

I am also going to make my flex container a specific width, height, and background color, so we can differentiate the container from the items!

Now, we can use a number of different properties to control the layout of the elements. Some flex properties an also be used on single elements with no children. 

* flex-direction 

This  defines in which direction the container wants to stack the flex items. (e.g vertial or horizontal) Common ways to set it are column or row. Row is the default, we can set it to column like this:

*/

/* .flex-container {
  flex-direction: column;
} */

/*

flex-wrap

This property specifies whether the flex items should wrap or not. This controlls whether they will "wrap" onto multiple lines, or be forced onto one line. Some values would be : wrap and nowrap. nowrap is the default! If you don't specify, then your flex items will stay on the same line!

First, we should make our text much bigger, and give them a background color, we will be able to observe this property better. 

*/

.flex-items {
  font-size: 50px;
  background-color: lightblue;
  width: 150px;
  margin: 5px;
  height: 40%
}

.flex-container {
  flex-wrap: wrap;
}


/*

flex-flow

flex-low is a shorthand for both wrap and direction, so both could be specified, like so:

.flex-container {
  flex-flow: row wrap
}

justify-content

The justify-content property is used to align the flex items along the "main axis" (in a row layout, this is the x axis, in a column layout, its the y axis!) It will move all of the flex items to the the center, or to the left, or make space between them etc. 

* The center value aligns the flex items at the center of the container.
* The flex-start value aligns the flex items at the beginning of the container (this is default).
* The flex-end value aligns the flex items at the end of the container.
* The space-around value displays the flex items with space before, between, and after the lines.
* The space-between value displays the flex items with space between the lines.
*/
.flex-container {
  justify-content: center;
}
/*

align-content

The align-content property is used to align the flex items along the cross axis. (the other axis that isn't the main axis!)

* The space-between value displays the flex lines with equal space between them.
* The space-around value displays the flex lines with space before, between, and after them.
* The stretch value stretches the flex lines to take up the remaining space (this is default).
* The center value displays display the flex lines in the middle of the container.
* The flex-start value displays the flex lines at the start of the container.
* The flex-end value displays the flex lines at the end of the container. 

Example
*/

/* .flex-container {
  align-content: center;
} */

/* 

If you want something in the center of the page, set both justify-content and align-content to center!

align-items

The align-items property is used to align the flex items with themselves. This will only make a difference if some of the flex items are different sizes.

* The center value aligns the flex items in the middle of the container.
* The flex-start value aligns the flex items at the top of the container.
* The flex-end value aligns the flex items at the bottom of the container.
* The stretch value stretches the flex items to fill the container (this is default).

Example: 
In this example, the height of the first item will be reduced to show the different possibilities of align items. 
*/

/* #number1 {
  height: 20%;
}

.flex-container {
  align-items: center; 
} */ 

/*


Flex Items:

For these examples, we will use a second flex-box example: 

*/

.flex-container1 {
  display: flex;
  height: 500px;
  width: 500px;
  background-color: gray;
  flex-flow: column wrap;
  justify-content: center;
  align-content: center;
}

.flex-items1 {
  font-size: 30px;
  background-color: peachpuff;
  width: 150px;
  height: 20%;
  margin: 5px;
}




/*

As well as flex container properties, there are a number of flex item properties that can be used to control the layout of the flex items. The properties discussed will be: 

order
flex-grow

order:

The order property specifies the order of the flex items. The default is 0, so if no order property is specified, each will have an order of 0. If the first div is given an order of 1 it will be last, unless anything has an order greater than 1. 

*/

/* #firstItem {
  order: 1
}
 */
/*


flex-grow:

The flex-grow property specifies how much a flex item will grow relative to the rest of the flex items.

The value must be a number, the default value is 0.

If we give the third item a flex-grow value of 1, it will be larger than the other two items. 

*/

/* #thirdItem {
  flex-grow: 1
} */

/*

More properties can be read about here: https://www.w3schools.com/css/css3_flexbox_items.asp

////////////Exercises:

// 1. Make a flex layout in HTML. You'll need to make an outside div with a class, and then make six inside divs, with a new class (but the same for all three) and a unique id each. In each div, put the name of a book/show/movie in a header, and add a paragraph in which you provide a brief description about each one. 

// 2. Change the background font-family and font-size of the inside divs using their shared class. Give the divs the property margin, and set it to at least 5px. This will create some space around each div. 

// 3. Using their unique id, give them all a different backgdound color. 

// 4. Set the properties of the class for the outside div. Make sure you set the display to flex. Next, use at least 3 of the flex properties we have covered to arrange your flex items in a way that you like. 


/////////////Extra Exercises:
1. Make a flexbox layout in HTML with five items. In each of the flex items, load an image using an image tag!
//In CSS, style your flexbox using various properties to make your images look nice!


















