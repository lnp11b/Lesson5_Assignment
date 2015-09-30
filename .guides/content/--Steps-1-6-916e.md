<h1>Step 1 - Create the 'seminole.js' file:</h1>
Create a new file in the <b>'Lesson5_Exercise'</b> folder.
<ol>
<li>Right Click on the FOLDER <b>'Lesson5_Assignment_F15'</b>.  Make sure you are not selecting the Project!!</li>
<li>Select <b>'New File'</b></li>
<li>Name the new file:  <b><mark>seminole.js</mark></b></li>
<li>Remove <b>ALL</b> of the content that was generated in this new file.  <b>NOTE:</b>  Codio add this content by default to get you started.  We do NOT need these statements!!!</li>
</ol>
<h1>Step 2 - Add Comments</h1>

<b>REMINDER:  Clear all content from the new file!!!</b>  Now, enter your name and today's date where indicated below:<br>
<pre>
//    Program Name:  Seminole Trojans <br>
//    Program topics:  Variables, Functions, Arrays, Loops<br>
//    Author: <br>
//    Date:   <br>
//    Filename: seminole.js<br>
</pre>
<b>REMINDER:  Do not copy and paste the statements into your .js file.  If you do, you may have to replace ALL <b>" "</b> in the file.  Codio will not always copy double quotes correctly and MAY keep you from successfully rendering the page!!!</b> <br>
<p>
<h1>Step 3 - Declare the array literal - <code>daysOfWeek</code></h1>
Below the comment section, enter the following code to declare the <code>daysOfWeek</code> variable and set its value using an array literal:<br>

<pre>// global variables
var daysOfWeek = ["Sunday", "Monday", "Tuesday", "Wednesday", 
                  "Thursday","Friday", "Saturday"];</pre>
This code uses an array literal to declare a variable named <code>daysOfWeek</code> whose value is an array that contains the name of each day of the week.
</p>

<p>
<h1>Step 4 - Declare the array literal - <code>opponents</code></h1>
Below the <code>daysOfWeek</code> variable declaration, enter the following code to declare the <code>opponents</code> variable and set its value:<br>

<pre>// global variables
var opponents = ["Lightning", "Combines", "Combines", 
    "Combines", "Lightning", "Lightning", "Lightning", 
    "Lightning", "Barn Raisers", "Barn Raisers", 
    "Barn Raisers", "Sodbusters", "Sodbusters", "Sodbusters",
    "Sodbusters", "(off)", "River Riders", "River Riders", 
    "River Riders", "Big Dippers", "Big Dippers", 
    "Big Dippers", "(off)", "Sodbusters", "Sodbusters",
    "Sodbusters", "Combines", "Combines", "Combines", 
    "(off)", "(off)"];</pre>


<b><h1>NOTE:</h1></b>  Be sure to start the list of values with an opening bracket ( <code>[</code>) and end it with a closing bracket ( <code>]</code>).  Also make sure the entire statement ends with a semicolon (<code>;</code>).
This array lists, in order, the Seminole Trojans' opponents for each of the 31 days in August 2016.  

For instance, the first day of the month, August 1, the team is playing the Lightning, on the second day they're playing the Combines, on the last day, August 31, no game is scheduled.

</p>

<h1>Step 5 - Declare the array literal - <code>gameLocation</code></h1>
Below the <code>opponents</code> variable declaration, enter the following code to declare the <code>gameLocation</code> variable and set its value:<br>

<pre>// global variables
var gameLocation = 
   ["away", "away", "away", "away", "home", "home", "home",
    "home", "home", "home", "home", "away", "away", "away",
    "away", "", "away", "away", "away", "away", "away",
    "away", "", "home", "home", "home", "home", "home",
    "home", "", ""];</pre>
    
This array lists whether the team is playing away or at home for each of the 31 days in August 2016.  Note that this combines the strings "away" and "home" with empty values, indicated by "", which denotes days when no game is scheduled.  

For instance, the first four days of the month, August 1-4, the games are away, on the next 7 days, August 5-11, the games are at home, and on the last day, August 31, no game is scheduled.
</p>


<h1>Step 6 - </h1>
Return to <b>calender.htm</b> file and add the following code at the bottom of the document, just above the <b>closing</b> <code>body</code> tag:
<pre>&lt;script src="seminole.js">&lt;/script></pre>

Refresh or reload the <b>calendar.htm</b> file and preview the web page.  

<p>

<b><h1>NOTE:</h1></b>   Although you've declared three array variables, <b>you have not yet referenced their values in any JavaScript code, so the web page still contains an empty table.</b>  You will create functions to insert the array values in the table in a later step!

<center><b>BE PATIENT!!!</b></center>
</p>


