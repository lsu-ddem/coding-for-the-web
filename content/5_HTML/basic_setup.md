---
title: Basic HTML Document Setup
weight: 2
---

[slides](../presentation5_2)

<p data-height="600" data-theme-id="33744" data-slug-hash="ZErxpKx/34e1bf7dbf71afebc6bde522c1ced954" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="5.2 Basic HTML Document Setup" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/ZErxpKx/34e1bf7dbf71afebc6bde522c1ced954?editors=1111">1.2 Naming Variables</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>


### Basic HTML Document Setup 

As we know, when working outside of codepen, we set up our HTML document like this: 

<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

</body>
</html>

The first tag specifies that the document is a HTML document. Then we need the html tag, which is closed at the botton. 

Within that, we have the head tag, which includes the title tag. The title that we put in the title tag is not included on the web page, but is the title of the web page. When we have a tab open, we see the title of the webpage. 

Below the head tag, we have the body tag. Everything that we want to actually appear on our webpage goes inside the body tag. 

#### Loading Javascript and CSS into HTML 

When creating a website, we tend to create a folder that its different pages will be stored in. We usually create a homepage for the website called index.html. This will be the default landing page for our website. We can make other html pages (for example bio.html, resume.html, etc) and link them in some way. 

There are two ways to include CSS and JavaScript in our HTML pages. One is to add them as tags in our HTML document(s), and the other is to link them as seperate pages in our folder. 

#### Adding CSS and Javascript with Tags

For this approach, we write our css and javascript in relevant css and javascript tags in our html. For css, we would use the <style> </style> tag. 

The following example shows that the regular CSS syntax can be used with the style tag. 
```html
<h1 id="firstHeader" onclick="changeColor()"> This Demonstrates the Style Tag </h1>

<style>
  
  #firstHeader {
    color: red;
  }

</style>
```

The javascript for the webpage can be similarly placed into the <script> </script> tag. The following function is written inside the script tag. 

```html
<script>
  
  function changeColor() {
    let myHeader = document.getElementById("firstHeader");
    if (firstHeader.style.color == "red") {
      firstHeader.style.color = "blue";
    } else {
      firstHeader.style.color = "red";
    }
  }
  
</script>
```

Q : What will the function do? 

Example in Codepen:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="raBjbgW" data-pen-title="5.1 Example " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/raBjbgW">
  5.2 Example </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Linking CSS and Javascript pages

The second way to add CSS and JavaScript to HTML is to load in seperate CSS and Javascript pages. This is similar to how we have different windows for CSS and JavaScript in Codepen. These ones are automatically connected to the HTML in codepen. 

Seperate CSS and JavaScript pages are usually called styles.css and scripts.js. They are loaded into the HTML using the same technique used for adding a link to HTML. The link to the css code goes within the head tag, wheras the js link goes in the body tag. 

```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
 <link rel="stylesheet" href="styles.css">
</head>
<body>

<script src="scripts.js"></script>
</body>
</html>
```
#### Images and Hyperlinks

In the very beginning of the class, we learned how to add an image to HTML. We will do a brief refresher on that, and then learn how to link to another page, element, and external website.

To add an image to our webpage, we use the ```<img>``` tag. This tag does not need a closing tag. Inside the tag, we will use the attribute src (which is short for source, and is basically the link to the image!). We will then 
add our link in quotes. We can either set the size of our image in CSS, or we can actually set it in the HTML tag, like in the example below. 

Remember to check that images you are using are not Copyrighted! The image below is from this website: https://unsplash.com/

```html
<img src="https://images.unsplash.com/photo-1587620962725-abab7fe55159?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2831&q=80" height="200">
```

In order to add a hyperlink to our HTML, we use the <a> tag. Inside that tag, we use the href attribute (similar to the src attribute! This time, href means the hypertext reference, again, basically the link itself), then we put our destination link, in quotes, for example:

```html
<h2>
<a href="https://www.w3schools.com/html/html_links.asp"> If you click this, it will take you to the page for HTML links and hyperlinks on w2schools! We can not open this page *in* codepen, but if we select open in a new tab, it will work. </a> 
</h2>
```

Example in Codepen: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="MYgJdYj" data-pen-title="5.1 Example_1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/MYgJdYj">
  5.2 Example_1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Linking to an element on the same page

The following example in codepen shows how we can use a tags to link to other elements on the same page. The example contains an unordered list (with bulletpoints instead of numbers!) Each list item (```<li>```) contains an <a> element with a href which refers to the id of another element. In this case, three different poem titles. When each item is clicked, the page will jump to the element with the corresponding id. 

Notice the use of ```<br>``` for line breaks, and ```<b> </b>``` for bold! (```<br>``` does not need a closing tag!)

Example in Codepen:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="bNbgyEb" data-pen-title="5.1 Example_2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/bNbgyEb">
  5.2 Example_2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

### Exercise 5.2

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="MYgJdeb" data-pen-title="Exercise 5.2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/MYgJdeb">
  Exercise 5.2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
