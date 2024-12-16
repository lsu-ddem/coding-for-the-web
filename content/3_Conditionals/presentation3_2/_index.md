---
title: Switch Statements
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

# Switch statements 

* The final type of conditional statement is the switch statement. 
* Switch statements are used to "switch" among a number of conditions called cases, instead of including tons of else if statements. 
* The cases compare the value of the tested variable/value to the value attributed to the case.
* Once the correct value is found, the code in that case is executed.
* If no cases match the tested value, the switch statement executes the "default case" 
---

* Our first switch statement will test different conditions to see what day of the week it is today.
* The switch statement will do this by utilizing a JavaScript date object, which will be covered in a later segment.
* The variables 'today' and 'day' get the current date from the JavaScript Date object. Objects are covered in a later segment. The value of the day is returned to us in a numeric format, with 0 representing Sunday, 1 representing Monday, and so on.
* We use a switch statement instead of seven  if, else if, else statements to determine what day it is.
* The variable day is compared to the values of each case. When the value is matched, the day is printed. 
* We always include a default statement in switch statements in case of an error on our part, or in case none of the cases evaluate as true. 
* The default case also helps with troubleshooting instead of not having any output when something goes wrong.

---

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="LEPxzLg" data-pen-title="3.2 Example " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/LEPxzLg">
  3.2 Example </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

* Make sure to add a break statement before testing a new case!             
---
* We can also program switch statements that check more complex conditions
* To do so, we set the variable the switch statement is checking to "true". 
* Now, we can set the conditions for the cases to more complex conditions, such as the cases below: 
* This switch example determines the letter grade of a test score out of 100
```
let testScore = 73;
// Note that we use 'true' in place of the tested variable, and incorporate the testScore variable in the case conditions
switch(true){
    case testScore >= 90:
        console.log(testScore +" / 100 : A");
        break;
    case testScore >= 80:
        console.log(testScore +" / 100 : B");
        break;
    case testScore >= 70:
        console.log(testScore +" / 100 : C");
        break;
    case testScore >= 60:
        console.log(testScore +" / 100 : D");
        break;
    case testScore >= 50:
        console.log(testScore +" / 100 : F");
        break;
    default:
        console.log("Score is too low to even have a grade");
    }
```
---
# Exercise 3.2

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="MYgJEEo" data-pen-title="Exercise 3.2" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/MYgJEEo">
  Exercise 3.2</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>