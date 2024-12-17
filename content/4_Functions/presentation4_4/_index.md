---
title: Event Invoked Functions
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---
### Event Invoked Functions 

In order to program event invoked functions, we need to refresh and extend our knowledge of HTML. 

#### HTML Refresher

HTML stands for Hyper Text Markup Language 

HTML allows us to create our own websites by writing code in a way that can be read by a browser and translated into the images and designs you see on web pages. 

All text, images, etc. present on a website are there because they were coded into the website's HTML. 

Good websites make use of at least 3 languages: HTML for structure, CSS for design, and JavaScript for interactability/making web pages dynamic. 

HTML is responsible for laying out the structure of the site. 

An actual HTML file contains the following lines of code that you won't see present in HTML code on codepen, and that is because codepen allows us to begin at the body tag of the HTML: 

```html
      <!DOCTYPE html>
      <html>
        <head>
          <title>Page Title</title>
        </head>
        <body>
          <h1>My First Heading</h1>
          <p>My first paragraph.</p>
        </body>
      </html>
```
If you were to copy this code, open up a txt file on your computer, paste the code into the text file and save the file as "index.html", you would be able to double click the file and open it in a web browser, where you will see the two sentences "My First Heading" and "My first paragraph."

Codepen makes this task easier by rendering our HTML in the white space below. 

This codepen white space is the equivalent to the part of the website that we can see. 

You don't need to concern yourself with memorizing the HTML document setup. We don't need to use it in codepen, and when you need to use it outside of codepen, you can look it up. 

Content is placed onto a web page by placing elements within the page's HTML. 

There are a variety of elements with different uses, such as headings, paragraphs, sections, images, videos, tables, etc. all with their own unique start and end tags. 

All HTML elements begin with a start tag and most end with an end tag.

Any text that we want displayed within the element goes between the tags. 

A start tag consists of the element's tagname, wrapped in carats <___> , while an end tag has a foreward slash before the tagname </___>, as you can see on the body element: <body> </body> . 

It is important to always remember to include a closing/end tag for an element at the correct position (if the element needs an end tag). 

HTML elements can be nested within each other, so misplacing or forgetting an ending tag can cause errors in the format and appearance of your website, with elements accidentally being placed inside of one another or ending up in the wrong place entirely.

#### The Body Element 

The body element contains all of the content that is visible on the web page. 

All of the content containing paragraphs, text, images, etc. are placed within elements that are all nested within the start and end body tag. 

Anything placed outside of the body element will not be visibly rendered on the page, so it is important to make sure all of your content is within the body tags. All other elements are nested inside the body tag. 

Example: 

```html
<body>
  <div id="textArea"> 
    <p class = "field1">This paragraph is in the first div and has the class "field1".</p>
    <p class = "field2">This paragraph is in the first div and has the class "field2".</p>
  </div>
  
  <div id="blankArea"> 
    <p class = "field1">This paragraph is in the second div and has the class "field1"</p>
    <p class = "field2">This paragraph is in the second div and has the class "field2"</p>
  </div>
```

To keep our code organized and so that the nesting is easy to see, we will indent each element's starting tag within the body element. 

If an element within the body also has nested elements, these elements will have two indentions 

#### Divs and Paragraphs 

In our example, we have two div elements, with two paragraph elements nested inside them. The div element is a fundamental block-level HTML element used for grouping and structuring content on a webpage. It is short for "division" and serves as a generic container to organize other HTML elements.

Both div elements have an id attribute in their opening tag. Ids are used to access specific elements. An id can't be used for more than one element. The paragraph elements have classes. Classes can be used to access groups of elements, so that can be styled or can behave in the same way. 

#### querySelector("")
  
To store and manipulate a HTML element in Javascript, we can use the document.querySelector(") method (we will learn a couple of other ways later on).

We can use querySelector to access the first element of a specific type (for the following examples, assume that we are on the same webpage as the HTML example above!). We place the type of element in quotes. 
```js
let firstDiv = document.querySelector("div");
```

we can use it to access ids. For ids, we have to use a hash symbol # before our id name. 
```js
let secondDiv = document.querySelector("#blankArea")
```
and we can use it to access the first element of a class (a different method can be used to access all elements of a class, but we will learn that later on). For classes, we have to use a period . before our class name. 

```js
let firstPara = document.querySelector(".field1")
```
#### Events

Consider an event to be any action, property, or change that can be tested for, such as when something on a web page is clicked or hovered over. Events work the same way logically that they do in real life. Say, for example, if you were to insert your house key into your front door. On the event that you turn your key to unlock it, your door will become unlocked. If we were to replicate this event through programming, we would run a function that would probably be called unlockDoor() on the event that a key is inserted and turned.

There are numerous different types of events that can happen to an HTML element that triggers the invocation of a JavaScript function, such as:
* onclick : when a user clicks an element
* onload : when the webpage finishes loading
* onmouseover : when a user hovers over an element
and many more: https://www.w3schools.com/js/js_events.asp , https://www.w3schools.com/jsref/dom_obj_event.asp

onclick is the main event we will focus on.

#### The Onclick Attribute 

The onclick attribute allows us to add a "click" event to an element. Once an element is clickable, we can use Javascript to execute a function when the element is clicked. The "click" is the event part of event invoked functions, though there are other types of events. 

We can make an element clickable in HTML or Javascript, but for now we will look at adding an onclick in HTML. The following example uses a button element, commonly used for click events. 

```html
<button onclick="myFunction()">Click the Button!</button>
```
When the button is clicked, it will run the funciton myFunction(), which means that there must be a function with that name in javascript, for example:

```js
function myFunction() {
    confirm("This function is invoked by a click event!");
}
```
The confirm will appear every time the button is clicked. 

Example in codepen: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="yyBgwxQ" data-pen-title="Untitled" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/yyBgwxQ">
  Untitled</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

In our second example, we will make use of document.querySelector() to create a function that manipulates the content of our webpage. We will create this function using the following steps

1. Create a paragraph in HTML, give it an id, and give it the text "Button has not been clicked yet" 
2. Create a button in HTML, give it an onclick with the function "changeText()". Put some text in the button. 
3. In Javascript, create a variable called "num", and set it equal to one. This variable will update our text every time our function runs. 
4. Create the changeText() function. Inside the function, store the paragraph element in a variable using querySelector(). 
5. Use your paragraph variable to change the text using the .innerHTML property. Set it equal to "Button has been clicked " + num++ + " times". 

Example in codepen: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="gbYgEyG" data-pen-title="4.4 Example_1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/gbYgEyG">
  4.4 Example_1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Exercise 4.4

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="LEPxawZ" data-pen-title="Untitled" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/LEPxawZ">
  Untitled</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>