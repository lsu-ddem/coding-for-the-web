---
title: JSON Syntax
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---
///////////////////////////////// JSON Syntax ////////////////////////////////

/* In this section we're going to cover common JSON syntax 

  We know that JSON is commonly used to communicate between web browsers and servers, 
 
  either sending or requesting and receiving data.
  
  JSON data is always sent and recieved in text format, AKA as a string.
  
  So, the JavaScript method JSON.parse() exists to parse the data from strings into JavaScript, 
  
  making the translation from JSON text to useable JavaScript data easier for us
  

/*************************************** Parse Method


  The JSON.parse() method can be used on any JSON data you want to convert to JS, whether it was recieved from a server, or it was stored in the JS code.
  
  First lets look at converting a JSON object to a JavaScript object using the JSON.parse() method

  The first requirement of the parse method is that the JSON data must be wrapped in a string by placing single quotes around the entirety of the data
  
  For example, say we declare a new JSON object on the next line like so:
  */  
      let studentJSON = { "firstName" : "Millie", "lastName" : "Brown", "grade" : 10 };

  /* The JSON object called studentJSON is a perfectly fine JSON object.
  
  We can modify it, print it, print specific attributes, etc. 
  
  However, say we now want to convert studentJSON to a JS object. 
  
  If we tried to use the parse method on studentJSON as it is, and then print the last name attribute, nothing will be printed to the console :
  */ 

      //let studentJS = JSON.parse(studentJSON);    ** Note that this line and the one below are commented out because they cause an error in the program

      //console.log(studentJS.lastName);

 // This is because the JSON object studentJSON is not wrapped in quotes, so it isn't being read as a string.

 // The parameter of the JSON.parse() method must be a string 

 // In order to use the parse method on the JSON object, the JSON data needs to be wrapped in single quotes to make it a string:

   studentJSON = '{ "firstName" : "Millie", "lastName" : "Brown", "grade" : 10 }';

 // Reassigning the value of studentJSON to the string of JSON data now allows us to successfully implement the parse method:

   let student = JSON.parse(studentJSON);
   console.log(student.firstName);

 /* If you check the console you can see that we have successfully parsed the string of JSON data into a JavaScript object.

    Now we will look at how we can complete the opposite task: converting a JavaScript object to JSON

    Remember that JSON is useful for exchanging data from AND to a web server.

    In the event that we want to convert JS data and SEND JSON data to a web server, we essentially perform the opposite action of the JSON.parse method

    Fortunately, there is also a method that makes this task easy for us, called Stringify.
*/


/************************************** Stringify Method

    The Stringify method is used to convert JavaScript objects to a string, the opposite action of the parse method, which converts strings of JSON data to a JavaScript object

    The syntax for the Stringify method is as follows:

      1. Declare a new variable to store the string returned by the Stringify method:
          let newString;
      2. Set the new variable equal to the Stringify method with the JavaScript object passed in as a parameter:
          newString = JSON.stringify(student);
        (of course, steps 1 and 2 should be combined for efficiency, but they're separated here for your understanding)

    The Stringify method takes the JavaScript object passed in as a parameter, and converts it to a long string containing all of the key:value pairs

    Let's convert the student object back to a string: 

*/
      let studentString = JSON.stringify(student);
      console.log(studentString);

  /* Checking the console, you'll see that the entire object is converted and the string is printed
   
     The string is now ready to be sent to a server, which will read the JSON text

     There are a few exceptions to pay attention to when using the stringify method to convert a JS object to a string:

     Remember that JSON does not support functions, dates, or undefined values. 

     This means that if you try to use the stringify method on a JS object that has a date, function, or undefined value, JSON will alter the object according to the unsupported data type.

     Dates are simply converted to a string. Let's look at an example:
     */
        let obj = { name: "John", today: new Date(), city : "New York" };
        let myJSON = JSON.stringify(obj);
        console.log(myJSON);

    // Looking at the console you'll see that the date object was converted to a string representation containing the value "2019-01-31T17:55:11.928Z" or whatever the current time/date is when you print it 
    
    // Functions are removed from the object entirely unless the return value of a function is converted to a string before the stringify method is implemented

   

/******************************************** Looping:

  An important functionality of JSON is looping
  
  Looping is extremely useful when working with larger JSON data sets; for example when populating a table of the JSON data instead of having to manually enter each cell
  
  Looping through JSON data is something that will look familiar, as it just uses a simple for-in loop
  
  Remember that for-in loops are used to loop through the properties of an object; in this case, we're looping through the properties of a JSON object
  
  For JSON data, we can loop through and print each key like so:
  
  */
      television = { "brand":"Samsung", "model":"QF Series", "make":"QN82Q6FNAFXZA", "price":2999};
      for (key in television) {
        console.log(key);
      }

// Looking at the console, you'll see that each of the keys from the object were printed.

// Note that the iterator, key, can be named anything. It could be i, x, etc. The name is irrelevant, the variable however is used to iterate through each key in the object

// To loop through the JSON data and retrieve the values of the key:value pairs, we use bracket notation like so:

    for (key in television) {
        console.log(television[key]);
      }

// Looking at the console, you'll see that each of the values from the object were printed.


/***************************************  Nesting

  The last syntax we'll look at before working with external JSON files is Nesting
  
  Sometimes you want to store a JSON object within a JSON object.
  
  For example, if we're making a list of our friends and their respective attributes, such as hair color, eye color, age, name, etc. all of these keys typically require one value
  
  Unless, of course, your friend has more than one hair color or two different colored eyes.
  
  In these scenarios, or if we wanted to include another key that would typically have more than one input, such as pets, we simply store a json object with the multiple values within a parent object, like so:
    
*/
      friend = {
        "name":"Kate",
        "age":21,
        "hairColor":"Blonde",
        "eyeColor":"Brown",
        "pets": {
          "bird":"Mack",
          "iguana":"Beemer",
          "cat":"Ozzy",
          "hamster":"Retsuko"
        }
       }


    // Notice that the JSON object friend nests another object, pets, inside of it

    // Nested JSON data is simply accessed using dot or bracket notation like so:

       console.log(friend.pets.hamster);

    // or:

      let pet2 = friend.pets["iguana"];
      console.log(pet2);
  
///////////////////////// Exercises /////////////////////////

//1: Declare a new JSON object named favoriteShow and assign at least 5 key:value pairs that describe your favorite show, such as the Title, main actor, genre, director or network, etc.
  // Implement the appropriate method to store the JSON object to a variable named showData

//2: Using dot notation, print the values of each of the attributes of showData in sentence format to form a short paragraph, 
    // such as "My favorite show is __(title)__. __(title)__, starring __(main actor/actress) is directed by __(director)__ and airs on __(network/platform)__. It has aired on __(network/platform)__ for __(# of seasons)__ as a successful __(genre)__ franchise.""
  // Declare a new variabled named newJSON and implement the appropriate method to convert showData back into JSON. Print the string to the console.

//3: Declare a JSON object named 'family', in which each of your family members will be their own JSON object with at least 3 attributes






