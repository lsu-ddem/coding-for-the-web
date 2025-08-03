---
title: CSS Properties - Color, Font-family, Size Units and Position
weight: 5
---

[slides](../presentation5_5)

<p data-height="600" data-theme-id="33744" data-slug-hash="d7adeae9505e9adc18b83a7b44053da8" data-default-tab="js" data-user="lsuddem" data-embed-version="2" data-pen-title="5.5 CSS Properties - Color, Font-family, Size Units and Position" data-editable="true" class="codepen">See the Pen <a href="https://codepen.io/lsuddem/pen/vYdRQmr/d7adeae9505e9adc18b83a7b44053da8">5.5 CSS Properties - Color, Font-family, Size Units and Position</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

### CSS Properties 

* In this lesson, we will learn various CSS properties, in order to gain a basic understanding of how to style a webpage. 

* There are many very useful CSS properties, and we will not have time to look at all of them, but there are some great explanations available here: 
https://www.w3schools.com/cssref/

#### Color 

* We have learned that there are many colors that you can write out, for example blue, darkblue, magenta etc. 

* We can get any color we want by using Hex color codes. These are 6 digit codes that begin with a # sign. 

* Here is a link to a color picker, where you can choose any shade that you want:

https://htmlcolorcodes.com/

* At the top of the page, you will see HEX, RGB, and HSL. These are all methods that we can use to specify colors, but we will use hex codes. Once you pick a color that you like, you can simply copy the hex code at the top, and paste it into CSS, for example:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="LEPyroB" data-pen-title="5.5 Example" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/LEPyroB">
  5.5 Example</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

* Notice that like with color names, we do not put quotes around our hex code. 

* Practice

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="vEBmrwb" data-pen-title="5.5 Practice " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/vEBmrwb">
  5.5 Practice </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

#### Changing color in JavaScript with Hex Codes

* In JavaScript, you can change the color of something using hex color codes, using the document object. The pen below shows an example of this: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="yyBbEdg" data-pen-title="5.5 Example_1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/yyBbEdg">
  5.5 Example_1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

* Practice 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="qEWmKzK" data-pen-title="5.5 Practice_1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/qEWmKzK">
  5.5 Practice_1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

#### Font Family

* We will look at a couple of different ways to change the font of our text. 

* The font-family property is responsible for changing our text in CSS. 

* Some fonts are already programmed into CSS. Learn more here: https://www.w3schools.com/css/css_font.asp

* The basic types of fonts are: 

1. Serif: serif fonts have a small stroke at the edges of each letter. 
2. Sans-serif: sans serif fonts have clean lines (no small strokes attached). 
3. Monospace fonts - here all the letters have the same fixed width.
4. Cursive fonts: they imitate human handwriting.
5. Fantasy fonts: decorative/playful fonts.

* When we speficy a font using the font-family property, we should specify the name of the font, a backup font from the same family, and then the family itself. We do this because not all browsers display fonts the same way. By giving the font-family property options, it will ensure that the font is as close to what you want as possible. 

* Look at the w3schools link for some font names: https://www.w3schools.com/css/css_font.asp

* Example:

* The following code will change the font of our pargraph to a monospace font, Courier New. The backup font will be a very similar monospace font, Courier. Finally, the font family, monospace, will be added. 

```css
#para {
  font-family: "Courier New", Courier, monospace
}
```

* If the browser doesn't recognize the first font (the preferred one) it will default to the second, then third. 

* Example in Codepen: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="ByBRPBa" data-pen-title="5.5 Example_2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/ByBRPBa">
  5.5 Example_2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

* Practice

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="EaYmpYQ" data-pen-title="5.5 Practice_2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/EaYmpYQ">
  5.5 Practice_2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

#### Google Fonts

* Another way to specify font is to get a font from google fonts, and load it into the HTML of your webpage. 

* First, go to the google fonts website, to find a font that you like: https://fonts.google.com/

* Choose a font, and click on it. You will see a button on the example of the font that says "select this style". Click on that, and information about the font will appear in the right-hand panel. 

* In the panel, you will see a section that says "Use on the web." Here, you can choose either <link> or @import. Choose the @import option. 

* Select everything in the ```<style>``` tag, including the opening and closing tags, and copy it. Then, paste it into your HTML. 

* Now, you can use this google font for any of your HTML elements. Simply copy the CSS font-familly property provided by google fonts and apply it to the element(s) of your choice. You can load as many google fonts into your HTML as you want. 

* In the codepen example, a google font is loaded into HTML, and then specified in CSS. 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="QwLvBbE" data-pen-title="5.5 Example_2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/QwLvBbE">
  5.5 Example_2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

* Practice 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="gbYWjaY" data-pen-title="5.5 Practice_3" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/gbYWjaY">
  5.5 Practice_3</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

#### Sizing 

* Size units in CSS are either absolute or relative. 

* Absolute means that the units are fixed, and will prescribe a specific height/width to an element. This does not always work well over multiple platforms and screen sizes. 

* An example of an absolute size value is px (pixels), which we have already used. 

* Relative specifies a size relative to another size, for example relative to the parent element (if an element is inside another element, the outside element is the parent, and the inside one is the child) or relative to the size of the screen. 

* The relative units that we will learn include vw, vh, and rem. 

* vw and vh stand for viewport width and viewport height. The viewport is the browser window size. 

* vw and vh and equal to 1% of the width and height of the viewport respectively, so if you have a viewport that is 50cm wide, 1vw would be equal to 0.5cm. 

* height and width properties can be used to set the size of an element. 

* Example

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="MYgmBKo" data-pen-title="5.5 Example_4" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/MYgmBKo">
  5.5 Example_4</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

* If we pull the webpage around, the div will change size in relation to its parent (the webpage). 

* A commonly used size unit to resize text is rem. 

* rem is a relative size unit because it is based on the root element's font size (usually the <html> element) rather than a fixed size like pixels (px). For example, if the root font size is 16px, then 1rem equals 16px. This makes rem units scalable and more accessible, as users can adjust their browser's default font size, and the design will scale accordingly.

* The codepen example shows a four paragraphs that have different rem font sizes. 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="wBwdxGK" data-pen-title="5.5 Example_5" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/wBwdxGK">
  5.5 Example_5</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

#### Position:

* To move an element to a different position, the top, bottom, left, and right properties can be set using sizing units. In order to use these properties, the position property must be specified in CSS, which controls the behaviour of elements in relation to the viewport and/or one another

* position is a CSS property, which can be set to the following values:

1. static - this is the default, an element will be positioned in terms of the order of the HTML elements. 
2. relative - An element with position: relative; is positioned relative to its normal position.
Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.
3. fixed - An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element. A fixed element does not leave a gap in the page where it would normally have been located.
4. absolute - An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed). However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

* The following practice should help demonstrate how these values work: 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="qEWmyXL" data-pen-title="5.5 Practice_4" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/qEWmyXL">
  5.5 Practice_4</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>

### Exercise 5.5

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="raBmrGv" data-pen-title="Exercise 5.5" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/raBmrGv">
  Exercise 5.5</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>