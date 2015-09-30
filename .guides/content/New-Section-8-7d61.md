<h1>Step 8 - Add the days of the month to the calendar using a <b>do/while</b> loop</h1>

<ol>
<li>Return to the <b>seminole.js</b> file.</li>

<li>Below the <code>addColumnsHeaders()</code> function, enter the following code to add a comment and create the structure of a new function named <code>addCalendarDates()</code>:
<pre>// function to place day of month value in first p element 
// within each table data cell that has an id 
function addCalendarDates() {




}//end of function</pre>
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

}</pre> 
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
After the closing <code>}</code> for the <code>do</code> command block, but before the closing <code>}</code> for the function, add the following statement:
<pre>while (i <= 31);</pre>
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
   } while (i <= 31);
}//end of function</pre>
Because you now have multiple functions to run when the page loads, you will create a master function to call when the page loads.  This function will in turn call each of the functions that needs to run on page load.
</li>

<li>
Below the function you just created, enter the following comment and statement:
<pre>
// function to populate calendar 
function setUpPage() {
   addColumnHeaders();   
   addCalendarDates();
}//end of function
</pre>
This code creates a new function name <code>setUpPage()</code> that calls the addColumnHeaders() and <code>addCalendarDates()</code> functions.  You need to change the event listener call to this function when the page finishes loading.
</li>
<li>
In the the <b>seminole.js</b> file, replace the occurrences of <code>addColumnHeaders</code> with <b>setUpPage</b> so your code matches the following:
<pre>// runs setUpPage() function when page loads
window.addEventListener("load", setUpPage, false);
</pre>

</li>
<li>Reload the <b>calender.htm</b> and view the web page.  As you can see, the table cells should now contain the days of the month with consecutive numbers from 1-31.</li>


<center><img src=".guides/img/SeminoleTrojan_Days.png" alt="Seminole Trojans" /></center>