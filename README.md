Download Link: https://assignmentchef.com/product/solved-dsc-450-database-processing-for-large-scale-analytics-assignment-3
<br>
<strong>Also Chapter 15 functions INSTR(), SUBSTR(), REGEX()</strong>

<strong>Part 1</strong>

<strong> </strong><strong>Restaurant Address Cleanup (20 points)</strong>

Use the Restaurants.sql file from HW2, which creates three tables Restaurant, Reviewer, and Rating. In this problem, we are concerned with the Restaurant table, which has a single attribute ‘Address’ of type ‘varchar2(100)’. We would like address to be searchable.  So we would like to create another table Restaurant_Locations with the following attributes:

rID, name, street_address,  city, state, zipcode, cuisine

<ol>

 <li>Create Restaurant_Locations table. Use the source dataset to determine the data types (and sizes) to use for each of the attributes.</li>

 <li>Write a cursor (using SQL and PL/SQL) to process each row from the original Restaurant table, extracting information as necessary to populate the new Restaurant_Locations table. The original address field must be split up and parsed into the new street_address, city, state, and zipcode fields.</li>

</ol>

You will need the following Oracle PL/SQL functions: SUBSTR, INSTR, and REGEX.




<strong>Submit 1.sql file. </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>Part 2</strong>

<strong>PL/SQL Functions</strong> <strong>(25 points)</strong>

The restaurants in the database continue to be visited and reviewed. Information about new restaurant reviews is made available as:

(RestaurantName, UserName, Rating, RatingDate)

Restaurant names and user names are assumed to be unique.

<ol>

 <li>Write a PL/SQL stored procedure that accepts the above input string and inserts new restaurant rating information into the Rating table. If a new user appears, it inserts into the Reviewer table.</li>

 <li>Also, create a table ‘Top5Restaurants’ restaurants in the database. Top5Restaurants holds the rIDs and names of top 5 restaurants in Chicago. Write a table-level trigger on the Rating table that computes top 5 restaurants and populates the Top5Restaurants table. This trigger is fired every time a restaurant receives a new rating.</li>

 <li>Test your procedure and trigger in SQL Developer to insert the following four strings:</li>

</ol>

(‘Jade Court’,`Sarah M.’, 4, ‘08/17/2017’)

(‘Shanghai Terrace’,`Cameron J.’, 5, ‘08/17/2017’)

(‘Rangoli’,`Vivek T.’,3,`09/17/2017’)

(‘Shanghai Inn’,`Audrey M.’,2,`07/08/2017’);

(‘Cumin’,`Cameron J.’, 2, ‘09/17/2017’)




<strong>Submit your 2.sql file and screenshot of data in Top5Restaurant table after the last inserted string in (c). </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>Part 3</strong>

<strong> </strong>

<strong>Restaurant Python DBAPI (15 points)</strong>

<strong> </strong>

For this problem download the CHIzipcode.csv file provided on D2L.

<ol>

 <li>Create ZipCode table based on attributes in zipcode.csv file (zip, city, state, latitude, longitude, timezone, dst)</li>

 <li>Write a Python program (similar to the one showed in class to connect to your SQlite database using PythonDB API) to convert the zipcode.csv file into a series of SQL insert statements. Populate the table by executing the INSERT statements.</li>

</ol>

Note: Use Python readlines function to read lines from zipcode.csv.

<ol>

 <li>Write a query to join zipcodes table with restaurant_locations table. Send the query to the database and obtain latitude and longitude of all restaurants in the Restaurants table. Print out the name, zipcode, latitude, longitude using your program.</li>

</ol>

Output should look like this:

Shanghai Inn, 60625, “41.971614”,”-87.70256″

<strong> </strong>

<strong>Submit your zipcode.py files</strong>

<strong> </strong>

<strong> </strong>

<ul>

 <li></li>

</ul>


