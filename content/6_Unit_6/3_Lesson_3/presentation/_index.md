---
title: READING JSON WITH XMLHTTPREQUEST
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---
///////////////////////////////// Reading JSON with XMLHTTPRequests  ////////////////////////////////
/*
* 
  The JSON code we've practiced thus var has been very simple. JSON is capable of holding much more data than we've been storing in our JSON objects.
  
  In fact, depending on the data, JSON files can end up holding hundreds of objects
   
  From this point on, the JSON data we will use will be contained within a JSON file rather than hard coding the JSON objects into our JavaScript code.
  
  JSON data within a JSON file may at first look different than the JSON code we've seen here, but don't get confused
  
  .json files wrap the entirety of the JSON content within a pair of curly brackets { } as you will see
  
  .json files also almost always contain multiple objects, but the syntax for this is something we've already seen, so don't get intimidated.
  
  You may be curious as to why we would want to store all of these objects in the same JSON file
  
  This is because JSON is extremely useful for presenting data in an organized, clean format that is easy for both humans and machines to read
  
  Say, for example, we were creating a JSON file that stored all of the books in our own personal library. 
  
  Instead of having 30 or so individual variables storing the data, we can organize the data in a JSON file by placing them within an array
  
  Each element of the array is a JSON object itself, and the elements are separated by commas, just like a JavaScript array
  
  Remember that in JSON, the elements of arrays are contained within a pair of square brackets [ ] and objects are placed within curly brackets { }

  Here is an example of using JSON to bookkeep a personal library: https://api.myjson.com/bins/12j3gg?pretty=1
  
  You can see the data organized in an easily readable format, representing our library of 3 books
  
  Now what we can do with the JSON file representing our library is read it and store the data in our JavaScript code, and later display it using HTML
  
  There are multiple ways to access and read a JSON data file hosted online, and use the data in JavaScript
  
  The method we will first cover is reading JSON files using XMLHTTPRequest:
  
  */

/*************************************  XMLHTTPRequest

  XMLHTTPRequest ( XHR for short ) is an API in the form of an object.
  
  XHR objects are used to communicate back and forth with servers. 
  
  XML(which is a language) is in the name, but XMLHTTPRequests can be used with any language, which is why we can use them when working with JSON files
  
  XMLHTTPRequests is one of the more complicated methods of communicating with a server that we will look at, but the process is still relatively simple.
  
  
  
  The syntax for constructing a new XMLHTTPRequest object is simply declaring a vew variable and setting it equal to XMLHTTPRequest() 
  
  The first step in reading JSON data using the XMLHTTPRequest method is to declare a JavaScript constant variable storing the URL of our JSON data 
  
  Remember that in JavaScript, a constant, declared with the keyword 'const' cannot be redeclared or reassigned
  
  Here we declare the constant 'url' and store the URL of the JSON data representing our library from earlier
  
  */

    const url = "https://api.myjson.com/bins/12j3gg?pretty=1";
// Realistically, to be more efficient, the url can be passed directly as a parameter of the .open method instead of storing the url to a variable, which we will see later on

// Next we declare another constant named 'request' which creates a new XMLHttpRequest object

    const request = new XMLHttpRequest();

/*
    The line above, the declaration of the request constant, created a new XMLHttpRequest object.
    
    The XMLHttpRequest object allows us to easily request data from a server
    
    Next we'll specify the response type of our request by using the responseType method, of which the default response type is text:
  
   */

    request.responseType = 'json';
    // Now our response type is set to JSON.

/*
    In the next few lines, we're going to be submitting an HttpRequest, which needs some explanation:
    
    The HttpRequest is literally a request to a server, in other words, its literally our browser asking another machine somewhere else in the world for something.
    
    Whether that something is getting data, sending data, etc. 
    
    There are 9 HTTP methods, but we're going to focus on the most important and common 4:
    
    (1) GET
        Requests using GET as the method should only retrieve data 
        (i.e. we use GET to GET data, to read data from the JSON file)
    
    (2) POST
        Requests using POST as the method are sending information to that location, either new or updated information
        The sending and reception of the information often causes a change in state on the server, like logging in
        
    (3) PUT
        Requests using PUT as the method are sending information to a location, but this information completely replaces what information was held prior
        In other words, PUT can be used to update information already being shared/stored, but it can also be used to store new information
    
    (4) DELETE
        Requests using DELETE as the method are deleting the specified resource
        
        The other 5 HTTP methods include HEAD, CONNECT, and TRACE, OPTIONS, and PATCH which you can read about here: 
        https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods
        
    Next, we need to open the XMLHTTPRequest object we created by using the .open() method, and specifying which HTTP Request method we want to use:
*/  

    request.open('GET', url, true);
  
  /*
  
   The .open() method initializes a new or existing request
   
   The method takes up to 5 parameters, and as little as 2 parameters.
   
   The 2 parameters required no matter what include the HTTP Request method type wrapped in quotation marks, and the url of the JSON data:
   
        XMLHttpRequest.open(method, url)
        
   The 3rd optional parameter is a boolean that defaults to true, which specifies whether or not to execute the operation asynchronously. 
   
       The async parameter defaults to true because sending the request asynchronously allows for our JavaScript code to continue working;

       Instead of having to wait for a response from the server, the JS code can continue to execute other scripts while waiting, and handle the response some time after the response is ready to be handled

       Setting this parameter to false would send the request synchronously, forcing us to wait for a response to gain back control and continue executing scripts or working

   The 4th and 5th optional parameters are for a user and password, which are used for authentification, but again are optional.
  
   As you can see on line 111, we initialized the request with the GET method, the url to our library data, and setting async to true.


/* Next we implement the onload method, which is called when an XMLHTTPRequest transaction is successfully completed
   
   The method is set equal to a function that will be executed when the request is completed successfully
  
   Within the function, we tell our code what to do with the data we get back from the request, which is stored in request.response
  */
  
   request.onload = function () {
    // first we want to check that the response to the request is ready for us to work with the data it returned
    // We do this by checking if the status of the request is equal to 200, which is the ready status, like so:
      if (request.status == 200){
        // if the response is ready for us to work with, the following code will execute:
         let jsonData = request.response; // this line stores the JSON data from the reponse to a local variable
         console.log(jsonData);
      }
     //close the if statement and the function curly brackets
    };
  // Finally, we send the request off by using the .send method() : 
  request.send();


// Now, looking at the console, you can see that we successfully programmed our first XMLHTTPRequest to access our library data and print it to the console!


// Lets practice accessing data with XMLHTTPRequests and doing more than simply printing the entirety of the data set to the console:

// In this example, we'll use a json file containing information about English Monarchs at https://api.myjson.com/bins/18jsro?pretty=1

// First we'll create a new XMLHTTPRequest to access the json file:
    const req = new XMLHttpRequest();
    // next we specify the response type of the request; we want the text to parsed into JSON
    req.responseType = 'json';
    // now we implement the .open method passing in the URL of the json data as the second parameter:
    req.open('GET', "https://api.myjson.com/bins/18jsro?pretty=1", true);
    // next we program the onload function to work with our data 
    req.onload = function () {
       // first check if the request is ready
      if (req.status == 200){
        // then store the response in a variable
        let monarchs = req.response; // this line stores the JSON data from the reponse to a local variable
        // now we can work with the JSON data in more detail!

        // If you looked at the JSON file, you probably took note that the JSON objects contain key:value pairs for their id(out of the entire data set), their name, the country, house, and years they ruled
        // Lets say we want to print information about ALL of the English Monarchs who have ever ruled over the House of Hanover
        // First, we'll scan through the JSON data and identify all of the Monarchs who ruled over the house of Hanover
        for(let i = 0; i<monarchs.length; i++){
          // the loop iterates through each object in the JSON file and checks if the value of the 'hse' key equals House of Hanover
          if(monarchs[i].hse == "House of Hanover"){
            // if we find a Monarch who ruled over the House of Hanover, we want to print some more facts about them
            // for every Monarch that meets the condition, we'll print their info in this format: Monarch __(name)__ ruled over the House of Hanover between the years ____(value of yrs key)__
            console.log(monarchs[i].nm + " ruled over the House of Hanover between the years " + monarchs[i].yrs );
          }
        }
      }
    };
  // Finally, we send the request off by using the .send method() : 
  req.send();

  // Looking at the console you can see that 6 monarchs ruled over the House of Hanover with their respective dates

  // In the next section we'll cover a method that most consider simpler than submitting XMLHTTPRequests, Fetch API




///////////////////////// Exercises /////////////////////////

//1 : Use an XMLHTTPRequest to access a json file containing information pertaining to the American Presidents : https://github.com/hitch17/sample-data/blob/master/presidents.json
    // Use loops to count the total number of Democratic presidents the United States has had, the total number of Republican presidents the United States has had, and the the total number of Other Party presidents the United States has had
    // Any object whose value for "party" that does not equal Democratic or Republican can be considered "Other Party"
    // Print the data to the console in this format: 
      // Total Democratic Presidents : X 
      // Total Republican Presidents : X 
      // Total Other Party Presidents : X 

//2 : Using the same data set from exercise 1, find all instances of a US president with the first name 'James'
      // Print the total number of US presidents with the first name James, and the date they took office

//3 : Use an XMLHTTPRequest to access a json file containing info pertaining to all of the makes of cars in the year 2010 : https://api.myjson.com/bins/xyaz0
   // Check if each object is considered a common brand/make, and if so, print the make to the console

//4 : Using the same data set from exercise 2, print all of the uncommon brands to the console next to their country of origin, like so: "Brand from Country"

