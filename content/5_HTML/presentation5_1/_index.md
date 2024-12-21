---
title: Accessing HTML in CSS
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

### HTML, CSS, and Javascript

As we have progressed through this course, we have already learned some of the basics of HTML and CSS. In this chapter, we will look at integrating HTML, CSS, and Javascript in more detail.

We will begin by looking at CSS syntax, since we haven't covered it as much as Javascript and HTML. 

--- 

#### Accessing HTML in CSS

CSS stands for Cascading Style Sheets. CSS is used to style HTML elements, and generally to make your websites look amazing! 

Similarly to accessing HTML in Javascript, we can access HTML in CSS using elements types, classes, and ids (and in some other ways, but this is enough for now!)

---

Consider the following element: 

```html
<p id=para1 class="paraClass"> My Paragraph </p>
```

To access it by its element type in CSS, we would use the following syntax:

---

```css 
p {
    font-size: 30px;
}
```

We simply type out the element type, followed by curly brackets, in which we put all the styling that we want. The styling that we apply to it (in this case, changing the font size), will apply to every element of that type. 

---

CSS properties are in property and value pairs, with a colon inbetween, and a semi-colon between each pair. Properties are pre-defined, and the format of values changes depending on the type of property. 

To access our element by its class, we would use the following syntax:
```css
.paraClass {
    color: blue;
    background-color: green;
}
```

We use a period to access classes. Again, this CSS will style any element in the paraClass class. 

--- 

To access this element by its id, we would use the following syntax: 

```css 
#para1 {
  color: red;
  font-size: 10vh
}
```
We use a hash symbol to access the id. This will style only the specific element that has this id. An id styling will always take precedence over a class or element. This is useful, becuase you can use a class to style the basic properties of elements that you want to look the same, and id to make more specific stylings. 

---

The codepen example shows a few different elements with ids and classes to illustrate the specificity of different stylings. 

Codepen Example:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="zxONQpR" data-pen-title="5.1 Example " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/zxONQpR">
  5.1 Example </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

--- 

##### Accessing the Body of the Webpage

We can apply stylings to the whole webpage by accessing the body element in CSS. Because there is only one body of the webpage, we access the body just with the word "body", we don't need to use classes or ids: 

```css
body {
    background-color: pink;
    font-family: Arial;
}
```
This will change the background color and font of the whole document. 

---

#### Exercise 5.1

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="qEWRGYJ" data-pen-title="Exercise 5.1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/qEWRGYJ">
  Exercise 5.1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>