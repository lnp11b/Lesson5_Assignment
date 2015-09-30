<h1>Step 8 - Add the days of the month to the calendar using a <b>do/while</b> loop</h1>

<ol>
<li>Return to the <b>seminole.js</b> file.</li>

<li>BELOW the <code>addColumnsHeaders()</code> function and ABOVE the <code>window.addEventListener</code>code> statement, enter the following code to add a comment and create the structure of a new function named <code>addCalendarDates()</code>:
<pre>// function to place day of month value in first p element 
// within each table data cell that has an id 
function addCalendarDates() {

<br /><br />


}//end of addCalendarDates function</pre>
</li>

<li>Within the <code>addCalendarDates()</code> function, enter the following statements:
<pre>
var i = 1;
var paragraphs = "";
</pre>
This statement creates a counter variable called <code>i</code> and sets its value to 1.  The second statement creates a variable named <code>paragraphs</code> and sets its value to an empty string.
</li>

<li>
Below the variable declarations, enter the following code:

<pre>
do {

}//end of do/while loop</pre> 
This code starts a do/while statement with the <code>do</code> keyword.

</li>

<li>
Within the code block for the <code>do</code> statement, enter the following statement:
<pre>var tableCell = document.getElementById("08-" + i);</pre>

This statement creates a variable called <code>tableCell</code> and uses the <code>getElementById()</code> method to set its value to the element with an <code>id</code> value that starts with 08- followed by the value of <code>i</code>.  This means that in the first iteration of the loop, the table cell variable references the element with the <code>id</code> of <code>08-1</code>, which is the second <code>td</code> element in the second row of the table.
</li>

<li>
Below the statement you created in the previous step, enter the following statement:
<pre>paragraphs = tableCell.getElementsByTagName("p");</pre>
This statement uses the <code>getElementByTagName("p")</code> method to look up all <code>p</code> elements within the current cell (designated by the <code>tableCell</code> variable), and stores the values as an array in the <code>paragraphs</code> variable.
</li>

<li>
Below the statement you created in the previous step, enter the following statement:
<pre>paragraphs[0].innerHTML = i;</pre>
This statement assigns the value of the counter variable, <code>i</code>, as a content of the first paragraph (numbered 0) in the current cell.  The first time through the loop, this places the value 1 in the cell for the first day of the month.
</li>

<li>
Below the statement you created in the previous step, enter the following statement:
<pre>i++;</pre>
This statement increments the counter variable.
</li>
<li>
<b>After</b> AND on the <b>same line</b> of the closing <code>}//end of do/while loop</code> for the <code>do</code> command block, and before the closing <code>}</code> for the function, add the following statement:
<pre>while (i < 32); </pre>
This conditional statement determines whether the <code>do</code> command block is repeated for another iteration.  Because the month of August has 31 days, the block should be executed 31 times.  After the 31st time, the counter variable will be 32, which is not less than or equal to 31, so the <code>do/while</code> statement will end without iterating again.  The following shows the <b>completed code</b> for the <code>addCalendarDates()</code> function.
<pre>
// function to place day of month value in first p element 
// within each table data cell that has an id 
function addCalendarDates() {
   var i = 1;
   var paragraphs = "";
   do {
      var tableCell = document.getElementById("08-" + i);
      paragraphs = tableCell.getElementsByTagName("p");
      paragraphs[0].innerHTML = i;
      i++;      
   } while (i < 32);
}//end of addCalendarDates function </pre>
Because you now have multiple functions to run when the page loads, you will create a master function called, <code>setUpPage()</code>to call when the page loads.  This function will in turn call each of the functions that need to run when the page loads in the browswer.  We will create this function in the next!!  

<li>At the bottom of the 'seminole.js' file, enter the following code to add a comment and create the structure of the new function named <code>setUpPage()</code>:
<pre>// function to load the calendar content in the calendar when the page loads
function setUpPage()  {
<br /><br />
}//end of setUpPage function</pre>

Within the <code>setUpPage()</code> function, before the closing <code>}//end of setUpPage function</code>, add the function call statements <b>addColumnHeaders();</b>  AND <b>addCalendarDates();</b> so your <code>setUpPage()</code> function matches the following:
<pre>// function to load the calendar content in the calendar when the page loads
function setUpPage() {
   addColumnHeaders();
   addCalendarDates();
}//end of setUpPage function</pre>
Calling the <code>addColumnHeaders();</code> AND the <code>addCalendarDates();</code> functions ensures that the calendar is populated with the column headers and the calendar date information when the page is loaded!</li>
<li>
<b>MODIFY</b> the <code>window.addEventListener("load", addColumnHeaders(), false)</code> statement, which should be the last statement in the "seminole.js" file.  

Instead of it saying the following:  <code>window.addEventListener("load", addColumnHeaders, false);</code>

<b>REPLACE</b> the above statement with the following: <code> window.addEventListener("load", <b>setUpPage()</b>, false); </code>.  This will call the <code>setUpPage()</code> function each time the html page loads, which will then call all of the methods in this function.  

</li>
<li>
Reload/refresh the <b>calendar.htm</b> file and view the web page ("Preview static").  The table header rows are now populated with the days of the week in the same order you entered them in the <code>daysOfWeek</code> array.
</li>

<center><b>CONGRATULATIONS!!  YOU NOW HAVE COLUMN HEADERS AND THE DAYS OF THE DAYS OF THE WEEK!!</b></center>

</ol>
