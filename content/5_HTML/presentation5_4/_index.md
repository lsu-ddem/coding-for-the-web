---
title: Event Invoked Functions 2
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

### Event Invoked Functions 2

* In our section on functions, we learned about event invoked functions: functions that are triggered to run by a certain event, for example the pressing of a button. 

* We learned that we can use onclick, which will trigger an action when an element is clicked. 

* In this chapter, we learn other useful events. 

---

#### onmouseover

* onmouseover invokes a function when a mouse hovers over an element. 

* onmouseover is similar to onclick in that we put it in the opening tag of our element, and give it a function name in quotes. 

---

* In the codepen example, text changes when hovered over. The onhover is in the HTML tag of the paragraph element, just like an onclick. 
<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="YPKNmqQ" data-pen-title="5.4 Example " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/YPKNmqQ">
  5.4 Example </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---

#### onmouseout

* onmouseout is kind of the reverse of onmouseover. It invokes a function when you move the mouse off an element. 

* In the codepen example, the text is given a border when the mouse moves off the paragraph element.  
<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="ByBpXzV" data-pen-title="5.4 Example_1" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/ByBpXzV">
  5.4 Example_1</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---

#### onmouseover and onmouseout together

* onmouseover and onmouseout can be used together to make elements continue to change as the mouse moves on and off them. 

* In the following codepen example, we will create onmouseout and onmouseover events that work together on a single element. 

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="bNbgXwx" data-pen-title="5.4 Example_2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/bNbgXwx">
  5.4 Example_2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---

#### onkeydown

* onkeydown triggers a function every time a key is pressed (any key on the keyboard).

* onkeydown works best with input elements (elements in which text can be input), or generally, elements that are "selectable" - they can be selected on the webpage. 

* In the following Codepen example, you will see an input element. There are different types of inputs, but the default is text. input elements do not need a closing tag. 

---

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="jENygVJ" data-pen-title="5.4 Example_3" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/jENygVJ">
  5.4 Example_3</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---

#### Exercise 5.4
<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="KwPaOaY" data-pen-title="Exercise 5.4" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/KwPaOaY">
  Exercise 5.4</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---