---
title: JSON and HTML
outputs: ['Reveal']
reveal_hugo.theme: 'moon'
reveal_hugo.highlight_theme: 'solarized-light'
hidden: true
---
///////////////////////////////// JSON Data Scraping / HTML  ////////////////////////////////
/*

  So far we've had tons of practice obtaining JSON data using XMLHTTPRequests or Fetch API, and applying the data we receieved to real life scenarios,
  
  Such as when we found all of the subdivisions under a specific number of lots in the last section, or determined which street was safest according to crime data.
  
  We're going to continue putting JSON to use for real life scenarios, however now we want to start displaying the data we obtain and calculate in a more practical way.
  
  Up until this point we've only printed our results and calculations to the console
  
  Now we're going to begin inserting the data we retrieve and work with into HTML to get a better visual representation of the data,
  
  and to display the data in a way that is useful and provides information to us or someone else.
  
  When you take raw data in the form that we've been working with, for example the large set of data containing crime reports, 
  
  and present it in a way that provides insight or context regarding the data, you transform the data into information. 
  
  This is a basic principle of statistics. In short, data and information are different. 
  
  Data can simply be defined as "facts or figures from which conclusions can be drawn", 
  
  while information is  defined defined as data that has been classified/organized/recorded/interpreted in a manner such that meaning of the data emerges.
  
  This is essentially what we are achieving by presenting the data we work with visually using HTML to present a clear meaning of the data.
  
  First we'll cover a simple example inserting JSON data we retrieved from an outside source into our HTML:
  
  Lets create an HTML element for our data to be contained within. If you go to the HTML tab, you'll see an H1 holding the text ' New Residential Buildings in 2019'
  
  followed by an empty h2 with the class "blank". We want to store the number of new residential buildings built in Baton Rouge in 2019 in this h2.
  
  First we'll declare a variable, fillInTheBlank, to store the h2 element so that we can update its contents with the JSON data in the function of our fetch
  
  Next we'll have to actually obtain the number of new buildings, which we can achieve by creating a new fetch to the JSON data provided by Open Data BR:
  */

  let fillInTheBlank = document.querySelector(".blank");
  // visit the json data provided by open data BR and interpret the data being provided
  // each JSON object is a new building. Each building contains information regarding the date their permits were issued to build, and the number of permits required to build it.
  fetch("https://data.brla.gov/resource/rd5e-2zhz.json")
    // parsing the promise output into JSON
    .then(res => res.json()) 
    .then((output) => {
      // the variable newBuildings is going to store the total number of residential buildings built in 2019
      let newBuildings = 0;
      for(let i = 0; i<output.length; i++){
        // for each object in the JSON data, if the first 4 characters of the date value match 2019, the counter increases because it was/will be built in 2019
        if(output[i].issueddate.substring(0,4) == "2019")
          newBuildings++;
      }
    // after the loop finishes iterating through the data, we update the content of the h2 element to be the total number of new buildings in 2019
    //  this value will update and be shown on the rendered web page in the result pane
    fillInTheBlank.innerHTML = newBuildings + " new buildings";
  })

// Now that we've seen how to insert JSON data into HTML, we can do more complex things:

// If you were to show someone the json data representing the residential buildings per year (https://data.brla.gov/resource/rd5e-2zhz.json) without any context whatsoever,
// not even saying "hey this is data about residential buildings", just showing them the JSON data and nothing else, they'd probably be completely lost, right?
// However, if you organized the data in a way that allows them to understand the data and what it means and represents, they would be easily informed just by looking at your organization of the data.
// We'll practice the method of turning data into information by populating a table with the JSON data to provide information about the number of new residential buildings in Baton Rouge per year, from 2014 to 2019.

// First lets remove the h2 we worked with earlier and update the title (in the h1) to be "New Residential Buildings in Baton Rouge 2014 - 2019"
let title = document.querySelector("h1");
title.innerHTML = " 🏘 New Residential Buildings in Baton Rouge 2014 - 2019";
// now we'll remove the h2 from the page 
fillInTheBlank.style.display = "none";

// Now that the title is updated and we've removed the h2, we're ready to get started with our table!
// First we'll create the empty table in our HTML
   
    // If you look in the HTML pane, you will see that we created a table with the class "container", and established the 4 table headers that indicate what the columns of the table represent
    // As you can see, the table contains 4 columns. One for the Year, Number of new buildings that year, total number of permits obtained that year, and the average number of permits per building.
    // Each row we insert into the table from our JS code will represent a year from the dataset, from 2014 to 2019
    // We created the table body, but the rest of the creation of the table will be handled in our JavaScript code rather than our HMTL.

// The function handling the JSON data and inserting it into our HTML is longer than functions we've placed within our fetch before, 
// so in this case, we've passed the function called 'calculate' into our second .then() method,
// which passes the output of the promise from the fetch request that was parsed into JSON into the calculate function
  
  fetch("https://data.brla.gov/resource/rd5e-2zhz.json")
    // parsing the promise output into JSON:
    .then(res => res.json()) 
    // passing the parsed JSON data into the calculate function:
    .then(calculate) 
     
 // the calculate function:
    // based on the table headers we've already established, we know we need to extract or calculate data for the following:
    // year, number of buildings per year, and number of permits per year
    // the average number of permits per building can be calculated using the two values we extract from the JSON data
  function calculate(output){
      // first we'll assign the HTML table body element to a variable so that we can insert rows into it later on
      let table = document.querySelector("tbody");
      // remember that we update the content of an HTML element using .innerHTML, so the variable 'rows' will store the HTML elements and data we create, so that we can later insert all of them into the table body
      let rows = "";
      // the following variables are declared to serve as counters for the number of new buildings per year
      let new2019 = 0;
      let new2018 = 0;
      let new2017 = 0;
      let new2016 = 0;
      let new2015 = 0;
      let new2014 = 0;
      // the following variables are declared to serve as counters for the number of permits obtained per year 
      let permits19 = 0;
      let permits18 = 0;
      let permits17 = 0;
      let permits16 = 0;
      let permits15 = 0;
      let permits14 = 0;
      // now that we have these counter variables declared, we can loop through the entire JSON data set and update our counter variables accordingly:
      for(let i = 0; i<output.length; i++){
        // for each object in the JSON data, we cut the first 4 characters from the issueddate value using the substring(x,y) method so that we can check the year the building is associated with
        // if the first 4 characters of the date value match the specified year, the counter for that year increases by 1 building
        if(output[i].issueddate.substring(0,4) == "2019"){
          new2019++;
          // if the object matched the date, then we know we can associate the number of permits awarded to that building with the total number of permits for that year
          // so, we update the permit counter for the year to equal itself(!!) PLUS permit count from the new object
          permits19 += parseInt(output[i].count_permit_number);
        }
        // the next 5 if statements follow the same logic, updating the appropriate variables accordingly
        if(output[i].issueddate.substring(0,4) == "2018"){
          new2018++;
          permits18 = permits18 + parseInt(output[i].count_permit_number);
        }
        if(output[i].issueddate.substring(0,4) == "2017"){
          new2017++;
          permits17 = permits17 + parseInt(output[i].count_permit_number);
        }
        if(output[i].issueddate.substring(0,4) == "2016"){
          new2016++;
          permits16 = permits16 + parseInt(output[i].count_permit_number);
        }
        if(output[i].issueddate.substring(0,4) == "2015"){
          new2015++;
          permits15= permits15 + parseInt(output[i].count_permit_number);
        }
        if(output[i].issueddate.substring(0,4) == "2014"){
          new2014++;
          permits14 = permits14 + parseInt(output[i].count_permit_number);
      }}
    // after the for loop is done iterating through the data set, our counter variables will all be up to date.
    // we can check this by printing the values to the console after the for loop is closed, which you can do now if you'd like to make sure the values are correct
    // now that we have the data needed to populate our table, we can begin doing just that
    
    // to populate our table, as mentioned earlier, we will append the "rows" variable to the tbody by using the innerHTML method on the variable storing the table body.
    // therefore we need to place the HTML code to create the rows of data within this variable:
    // we create a new row using the tags for an HTML table
    // remember that we create new rows using the table row element <tr> </tr>
    // and we include a table data element within each for for as many columns as the table contains
    // therefore, since we have 4 columns, each table row element should have 4 table data <td> </td> elements within it
    // so that it is easier to view and understand, each row is spread across 4 lines, as you can see below:
    rows = "<tr>" + "<td>" + "2019" + "</td>"
         // the row above creates a new table row which will represent the year 2019; the first data we assign to a table data element is the year this row represents. Note that this syntax will achieve the same result: "<tr> <td> 2019 </td>" since we are typing the year instead of getting it from a variable.
         // the next line creates another table data cell within the same row, which contains the total number of buildings built in 2019, which we obtain by simply referencing the variable we explicitly stored that value to
         + "<td>" + new2019 + "</td>" 
         // next we create the data cell in the same row for 2019 to display the total number of permits obtained for residential buildings in 2019
         + "<td>" + permits19 + "</td>" 
         // finally we calculate the average number of permits per building for 2019 by dividing the total number of permits by the total number of new residential buildings. 
         // Note that we close the table row on this line, and create a new table row for 2018 on the next line. The rest of the rows are poplated in the same manner:
         + "<td>" + permits19 / new2019 + "</td>" + "</tr>" +
           "<tr>" + "<td>" + "2018" + "</td>"
         + "<td>" + new2018 + "</td>" 
         + "<td>" + permits18 + "</td>" 
         + "<td>" + permits18 / new2018 + "</td>" + "</tr>"+
           "<tr>" + "<td>" + "2017" + "</td>"
         + "<td>" + new2017 + "</td>" 
         + "<td>" + permits17 + "</td>" 
         + "<td>" + permits17 / new2017 + "</td>" + "</tr>"+
           "<tr>" + "<td>" + "2016" + "</td>"
         + "<td>" + new2016 + "</td>" 
         + "<td>" + permits16 + "</td>" 
         + "<td>" + permits16 / new2016 + "</td>" + "</tr>"+
           "<tr>" + "<td>" + "2015" + "</td>"
         + "<td>" + new2015 + "</td>" 
         + "<td>" + permits15 + "</td>" 
         + "<td>" + permits15 / new2015 + "</td>" + "</tr>"+
           "<tr>" + "<td>" + "2014" + "</td>"
         + "<td>" + new2014 + "</td>" 
         + "<td>" + permits14 + "</td>" 
         + "<td>" + permits14 / new2014 + "</td>" + "</tr>";
   // Because there were only 6 rows, we manually created the rows and inserted the data were appropriate
   // If our data set was much larger, however, it would be very tedious to create the rows manually this way
   // In that scenario, it would be beneficial to write another function that takes the data you're going to insert into the data cells as parameters, and construct these rows automatically for you
   // The last step is to update the table body by populating it with the rows of data we created
      // we do this by using the .innerHTML method on the variable storing the table body and setting it equal to rows, the variable in which we stored the new table rows and data
  table.innerHTML = rows;
  }
     
// Looking at the rendered web page, it is safe to say that we have successfully transformed the raw data provided in the JSON file into information that can be easily and quickly understood by anyone looking at our table



//////////////////////////// Exercises /////////////////////////////

//1: Create a new fetch for the data located at https://data.ny.gov/api/views/w4pv-hbkt/rows.json?
  // This data set serves as a record for all of the vehicles, snowmobiles, trailers, and boats registered in the state of New York, whose registrations have not expired within the last two years
  // Each object is classified as a snowmobile, trailer, boat, or other type of vehicle using the following classifications respectively as the value of the record_type key: SNOW, TRL, BOAT, VEH
  // Using the response from the fetch, tally the total number of boats, snowmobiles, trailers, and vehicles
  // Finally, visualize this data by printing as many boat emojis(🚤), snowmobile emojis(🛷), trailer emojis(🏎), and car emojis(🚙) as there are of each type to the div with the ID "emojiHolder" to create a makeshift pictograph

//2: Create a new empty table in the HTML with columns for 'Age Range', 'Total # Females Employed', 'Average Female Hourly Rate', 'Total # Males Employed', 'Average Male Hourly Rate', 'Total # of Employed', 'Average Hourly Rate'
  // Populate the table using the data at https://data.seattle.gov/resource/24tp-6m99.json
  // This data represents Seattle's Gender Wage Comparison, including data for totals of males and females employed in specific age ranges, and the average hourly wage for each of these age ranges
  // Look back at the table example from this lesson if you need to
  // For each age range, insert a new row into the table you created in the HTML with cells for each of the columns using Javascript and JSON only (don't directly code the rows in HTML)
  // Populate the cells with the appropriate data from the JSON file


