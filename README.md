# D3-Inclass-Activity
In this activity, you are going to create a line-chart using D3 

**Step 1**: CLone the repository and open a python server.\
**Step 2**: Open linechart.html and uncomment the "Loading d3 js library" (uncomment the version4). \
**Step 3**: Link the line.js with the html by creating `<script type="text/javascript" src="line.js"></script>` tag before the </body> tag (under the comment linking to the line.js file)

**Step 4**: Open the data.csv file and take a look at it.\
**Step 5**: Open the line.js file 

**Step 6**: Now we are going to load the data:
           `d3.csv("data.csv".get(function(error, data){console.log(data)};`              
           This is going to get the data and simply write it in the console. Hence go to your browser, and inspect the console. You will see that an array of 50 objects is there. If you see this in your console, your data has loaded!
           
**Step7**: However, in the console of your browser, you will notice that the date and price are both in **" "** and that is not the format that we want our data to be in. Hence we need to parse the data according to how we want it. 
To learn about data parsing visit: http://learnjsdata.com/time.html 
**To parse our data to the format we want, we are going to define a variable called parseData before the step where we loaded our data.**\

`var parseDate = d3.timeParse("%m/%d/%Y");`   *[Because our data has / in them we are using /. If our data was like 02-02-2009, we would    parse it as (%m-%d-%Y)]*

**Step8**: Now we are going to go back to the loading data step that will come after the var parseDate step. **Now remove the console.log(data) part as that was only to check if our data has loaded or not.**

**Step9**: **Now we will call a function that will return our parsedData and the price as a Number instead of a string for each row of your data. We will use:

`d3.csv("data.csv")` \
  `.row(function(d){return{date:parseDate(d.date),price:Number(d.price)};})`\
 `.get(function(error, data){`
 
 **Your entire code of creating the line chart will go here inside this function that gets the data you loaded and also gives error if there is something wrong with the csv file**
 
 `});` 
 
 ### Inside the get function:
 
**Step10**: In order to have the proper scales for your linechart, you need to know the max and min of your data. This is easy manually when your data is small, but with large data, this is cumbersome and can be done instead using d3.


**Step11**
**Step12*
**Step13**
**Step14**
**Step15**


