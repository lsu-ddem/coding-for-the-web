---
title: Function Returns
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---

### Function Returns

As mentioned earlier, functions often end with a return statement

A return statement must begin with the keyword 'return'

Whatever follows the return keyword is what is literally "returned" to us as a result of running the function

We can place variables, equations, strings, concatenations, etc. as the return value for a function

Unlike other popular languages, JavaScript does not require us to specify the type of data that is being returned

I will provide a few examples of different types of functions and returns, so that you see the different possibilities for return statements, and gain greater understanding of functions:

1. Future Age Calculator

This function returns the age the user will be in the year provided by the user.
The function calculates the future age by subtracting the future year from the current year, and adding that value to the user's current age:

```js
let myAge = 20;
let futureYear = 2060;
console.log( "I'm " + myAge + " now, but in " + futureYear + " I'll be " + futureAge(myAge,futureYear));

myAge = 32;
futureYear = 2047;
document.write("I'm " + myAge + " now, but in " + futureYear + " I'll be " + futureAge(myAge,futureYear));

function futureAge(currentAge, futureYear) {
  let now = new Date();
  let thisYear = now.getFullYear();
  return currentAge + (futureYear - thisYear);
}
```

Returning this value instead of just adding console.log inside the function allows us to use the returned value in any way we want, which could be a console.log, a document.write like in our example, in another function, or in pretty much any other way!

2. Random Pet Generator
The next example looks at returning new objects or properties of new objects
This function randomly selects different elements from different arrays and assigns these values to the property of a new pet object
We return the randomly selected properties of the new pet object to the user.
The function's return statement prints the randomly selected properties of the object to the console in a specified format.

```js
console.log(petGenerator());

function petGenerator() {
  let petNames = [
    "Charlie",
    "Max",
    "Bella",
    "Fluffi",
    "Petunia",
    "Bloo",
    "Sushi"
  ];
  let animalTypes = [
    "bird",
    "cat",
    "dog",
    "horse",
    "tiger",
    "chinchilla",
    "bunny"
  ];
  let animalColors = [
    "tan",
    "black and white",
    "spotted",
    "striped",
    "red-orange",
    "rainbow",
    "brown"
  ];

  let randomNumber = Math.floor(Math.random() * 7);

  let newPet = {
    name: petNames[randomNumber],
    type: animalTypes[randomNumber],
    color: animalColors[randomNumber]
  };

  return (
    "Your new pet is a " +
    newPet.color +
    " " +
    newPet.type +
    " named " +
    newPet.name +
    "!"
  );
}
```
Examples in Codepen:

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="EaYZJWK" data-pen-title="4.6 " data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/EaYZJWK">
  4.6 </a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Exercise 4.6

<p class="codepen" data-height="300" data-default-tab="result" data-slug-hash="JoPEVOE" data-pen-title="Untitled" data-user="lsuddem" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/lsuddem/pen/JoPEVOE">
  Untitled</a> by LSU DDEM (<a href="https://codepen.io/lsuddem">@lsuddem</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

