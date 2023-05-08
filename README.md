Download Link: https://assignmentchef.com/product/solved-sdev-homework3-sql
<br>






5/5 - (1 vote)

<ol>

 <li>Start a postgresql instance and run the script northwind.sql.</li>

 <li>Once the data is loaded, write the queries to answer the questions below.</li>

 <li>Turn in a file with the QUERY and the RESULT for each question. We have included an example .txt file with a format for your submission; feel free to use this or your own version, but remember to include both query and result!</li>

</ol>

<p class="alignleft h5">Step 1: Initializing your database

<button class="btn btn-primary btn-sm alignbtn" type="button" data-toggle="collapse" data-target="#multiCollapseExample2" aria-expanded="false" aria-controls="multiCollapseExample2">Expand</button>

<ol>

 <li>Start your postgres instance<pre class="command-line" data-user="csci3308" data-host="csci3308-VirtualBox"><code class="language-bash">sudo -u postgres psql</code></pre></li>

 <li>Run the northwind.sql script to import data<pre class="command-line" data-prompt="postgres=#"><code class="language-bash">i &lt;path_to_northwind.sql&gt;;</code></pre>For eg:<pre class="command-line" data-prompt="postgres=#"><code class="language-bash">i Downloads/northwind.sql;</code></pre></li>

</ol>

<p class="alignleft h5">Part 2: Create and Execute queries (100 points)

<button class="btn btn-primary btn-sm alignbtn" type="button" data-toggle="collapse" data-target="#multiCollapseExample3" aria-expanded="false" aria-controls="multiCollapseExample3">Expand</button>

You must create and execute queries against the northwinds database to fulfill the requirements of this assignments. For each question, you must submit your query AND the result of the query. Each question has an associated number of rows that you should expect in resulting query.

<table>

 <tbody>

  <tr>

   <th>Serial No</th>

   <th>Query</th>

   <th>Number of rows returned</th>

   <th>points</th>

  </tr>

  <tr>

   <td>1</td>

   <td>Create an alphabetical listing (last name, first name) of all employees not living the in the UK who have been employed by Northwinds for at least 5 years as of the due date of this assignment (2019-04-14).</td>

   <td>5 rows</td>

   <td>4</td>

  </tr>

  <tr>

   <td>2</td>

   <td>Prepare a reorder list for products that currently have at least one unit in stock but are (strictly) below their reorder level. Display the product ID, name, quantity in stock, and unit price for each matching product.</td>

   <td>17 rows</td>

   <td>4</td>

  </tr>

  <tr>

   <td>3</td>

   <td>What is the name and unit price of the least expensive product sold by Northwinds? Use a subquery.</td>

   <td>1 row</td>

   <td>4</td>

  </tr>

  <tr>

   <td>4</td>

   <td>Create a list of the products in stock which have an inventory value (number of units in stock * unit price) under $200. Display the product ID, product name, and “total inventory value” in ascending total inventory value order (lowest to highest).</td>

   <td>15 rows</td>

   <td>4</td>

  </tr>

  <tr>

   <td>5</td>

   <td>List the country and a count of orders for all orders that shipped from that country for all countries other than the USA during August 1996.</td>

   <td>10 rows</td>

   <td>6</td>

  </tr>

  <tr>

   <td>6</td>

   <td>List the customer ID of the customers who have less than 4 orders in descending alphabetical order (Z-A).</td>

   <td>10 rows</td>

   <td>4</td>

  </tr>

  <tr>

   <td>7</td>

   <td>Create a supplier inventory report that shows the total value of each suppliers inventory in stock (total value = sum over all units of (units in stock * unit price)). List only those suppliers who supply more than 3 different items.</td>

   <td>4 rows</td>

   <td>4</td>

  </tr>

  <tr>

   <td>8</td>

   <td>Create a supplier price list showing the supplier company name, product name, and unit price for all products from suppliers located in France. Sort the list on unit price in descending order (highest to lowest).<i>hint: must use both the products table and the suppliers table</i></td>

   <td>5 rows</td>

   <td>6</td>

  </tr>

  <tr>

   <td>9</td>

   <td>Create an employee order list showing the last name, first name, title, extension, and number of orders for each employee who has less than 75 orders.<i>Hint: must use both the employees table and the orders table</i></td>

   <td>4 rows</td>

   <td>6</td>

  </tr>

  <tr>

   <td>10</td>

   <td>Create a NEW table named top_items with the following items: item_id (integer), item_code (integer), item_name (varchar(40)), inventory_date (DATE), supplier_id (integer), item_quantity (integer), and item_price (decimal (9,2)). None of these columns can be null. Include a PRIMARY KEY constraint on item_id.</td>

   <td>No answer set needed, just the create table command</td>

   <td>6</td>

  </tr>

  <tr>

   <td>11</td>

   <td>Populate the new table top_items with items from products for those products whose inventory value is greater than $2500. The corresponding columns are the following:a. product_id -&gt; item_idb. category_id -&gt; item_codec. product_name -&gt; item_named. &lt;today’s date=””&gt;-&gt; inventory_datee. units_in_stock -&gt; item_quantityf. unit_price -&gt; item_priceg. supplier_id -&gt; supplier_id<i>Hint: this entails an INSERT with a SELECT query as the insert value.</i>(No answer set needed, just the populate command)&lt;/today’s&gt;</td>

   <td>9 rows inserted</td>

   <td>6</td>

  </tr>

  <tr>

   <td>12</td>

   <td>Delete the rows in top_items for items with item_quantity less than 50.(No answer set deleted, just the delete command)</td>

   <td>4 rows deleted</td>

   <td>4</td>

  </tr>

  <tr>

   <td>13</td>

   <td>Add a new column to the top_items table called inventory_value (decimal (9,2)), with a default value of 0.</td>

   <td>No answer set needed, just the column add command</td>

   <td>4</td>

  </tr>

  <tr>

   <td>14</td>

   <td>Update the top_items table, setting the inventory_value column equal to item_price * item_quantity.</td>

   <td>No answer set needed, just the update command</td>

   <td>4</td>

  </tr>

  <tr>

   <td>15</td>

   <td>Drop the top_items table.</td>

   <td>No answer set table, just the drop command</td>

   <td>4</td>

  </tr>

  <tr>

   <td>16</td>

   <td>Create a list of employees’ first and last names as well as the number of unique customers they have sold to called “clients”. Only include employees who have sold to at least 50 unique clients. Display results in descending order by number of clients.</td>

   <td>5 rows</td>

   <td>6</td>

  </tr>

  <tr>

   <td>17</td>

   <td>Find all products that are cost less than the average unit price</td>

   <td>52 rows</td>

   <td>4</td>

  </tr>

  <tr>

   <td>18</td>

   <td>You’re Jeff Bezos and your employees have access to free Prime subscription. You’ve heard rumors that your employees are letting their neighbors and relatives use Prime. Find count of all employees that’ve ordered products to a different address (not their home address) in their city.</td>

   <td>1 row</td>

   <td>6</td>

  </tr>

  <tr>

   <td>19</td>

   <td>Create a list of employees and the number of orders they have completed and the number of unique clients sold to during the calendar year of 1998. Your table should display each employee’s first and last name, the number of unique clients, and the number of orders as order_count.</td>

   <td>9 rows</td>

   <td>6</td>

  </tr>

  <tr>

   <td>20</td>

   <td>‘Janet Leverling’ wants to know the count of all the orders which were getting shipped from ‘Sweden’ and took less than a week time to ship.</td>

   <td>1 row</td>

   <td>4</td>

  </tr>

  <tr>

   <td>21</td>

   <td>The company ‘Leka Trading’ was blacklisted by the regulators. List out all the product which were being supplied from this supplier.</td>

   <td>3 rows</td>

   <td>4</td>

  </tr>

 </tbody>

</table>

<p class="alignleft h5">Bonus Question (10 points)

<button class="btn btn-primary btn-sm alignbtn" type="button" data-toggle="collapse" data-target="#multiCollapseExample5" aria-expanded="false" aria-controls="multiCollapseExample5">Expand</button>

<table>

 <tbody>

  <tr>

   <th>Serial No</th>

   <th>Query</th>

   <th>Number of rows returned</th>

   <th>points</th>

  </tr>

  <tr>

   <td>1</td>

   <td>Create a list of employee names, the number of orders they have completed, and the number of customers they have sold to called “clients”. Only include employees that have either (a) more than 50 clients or (b) more than 70 orders. Your table should display each employee’s first and last name, the number of unique clients, and the number of orders as order_count.</td>

   <td>6 rows</td>

   <td>6</td>

  </tr>

  <tr>

   <td>2</td>

   <td>Find the average price of products that are supplied by companies that are based in the United States. Specify the name of company alongside the average price.</td>

   <td>4 rows</td>

   <td>4</td>

  </tr>

 </tbody>

</table>