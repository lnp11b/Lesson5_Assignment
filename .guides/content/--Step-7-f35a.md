<h1>Step 7 - Create a function which uses a <b><em>while</em></b> loop to place the days of the week in the table.</h1>

<ol>
<li>In the <b>seminole.js</b> file, below the array declarations, enter the following code to add a comment and create the structure of a function named <b>addColumnHeaders()</b>: 

<pre><b>// function to place daysOfWeek values in header row cells 
function addColumnHeaders() {
<br /><br />

}//end of addColumnHeaders function</b></pre>
</li>

<li><b>INSIDE</b> the body of the <b>addColumnHeaders()</b> function, enter the following variable declaration:
<pre><b>var i = 0;</b></pre>
This statement creates a counter variable called <code>i</code> and sets its value to <code>0</code>.
</li>

<li>
Below the variable declaration, enter the following code:
<pre><b>while (i < 7) {
<br /><br />

}//end of while loop </b></pre>
This code creates a <code>while</code> loop that sets the condition <code>i < 7</code>.  This means that everytime the loop restarts and the value of the counter variable is less than 7, the loop will go through another iteration.
</li>

<li>
Within the command block for the <code>while</code> loop, enter the following statement:
<pre>
<b>document.getElementsByTagName("th")[i].innerHTML = daysOfWeek[i];</b>
</pre>

Starting at the end, the second part of this statement, <code>daysOfWeek[i]</code>, fetches the value from the <code>daysOfWeek</code> array that has the index value equal to the counter variable, <code>i</code>.  The first part of the statement uses the <code>getElementByTagName()</code> method to identify the <code>th</code> element that has the index value equal to the counter variable, <code>i</code>, and sets the value of its <code>innerHTML</code> property to the corresponding value fetched from the <code>daysOfWeek</code> array.  

For instance, in the first interation of this loop, the value of <code>i</code> will be 0.  The <code>getElementByTagName()</code> method will identify the first <code>th</code> element, representing the column heading for the first column, and set its value to the first value of the <code>daysOfWeek</code> array, which is "Sunday".
</li>

<li>
Below the statement you created in the previous step, enter the following statement:
<pre><b>i++;</b></pre>

This statement increments the counter variable.  <br>

The following is the completed code for the <code>addColumnHeaders()</code> function.  <b>Verify that you have written the function correctly!!!</b>

<pre><b>
// function to place daysOfWeek values in header row cells 
function addColumnHeaders() {
   var i = 0;
   while (i < 7) {
      document.getElementsByTagName("th")[i].innerHTML = daysOfWeek[i];
      i++;
   }//end of while loop
}//end of addColumnHeaders function


</b></pre>

</li>

<li>
Below (outside of) the function you just created, enter the following comment and statement:
<pre><b>
//This statement will add the column headers to the page immediately when the page loads in the browser
window.addEventListener("load", addColumnHeaders, false);
</b></pre>

This statement calls the <code>addColumnHeaders()</code> function when the page finishes loading a browser.
</li>

<li>
Reload/refresh the <b>calendar.htm</b> file and view the web page ("Preview static").  The table header rows are now populated in the calendar.
</li>

<center><b>CONGRATULATIONS!!  YOU NOW HAVE COLUMN HEADERS!!</b></center>
<hr>

