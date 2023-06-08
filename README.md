# SQL-Queries

**A few Solutions to business problems utilizing SQL in a video rental store database**

# Problem 1


**Return the customer IDs of customers who have spent at least $110 with the staff member who has an ID of 2.**


Solution
1.	SELECT customer_id , SUM(amount)

<b> Selects the Customer id and Amount fields/columns from the payment table. Sum(amount) Aggregates the total payment made by each unique customer?customer_id .

2.	FROM payment

The table with the data we need to perform the query

3.	WHERE staff_id = 2

The where clause acts as a filter to limit the result of the query based on specific parameters i.e. Only return a result of staff member whose id number is 2.

4.	GROUP BY customer_id
Group  BY clause used to group the values in customer_id column of the payment table

5.	HAVING SUM(amount) > 110;
Returns values of the sum total payment that is greater than 110   




# Problem 2

**How many films begin with the letter J?**

Solution
1.	SELECT COUNT(*) FROM film

Counts all the values in the film table based on parameters. 
 
2.	WHERE title LIKE 'J%';

Returns all films that begin with the letter ‘J’

    So in essence, it returns the count of films that begin with the letter ‘J’. 
    
    
 # Problem 3
**What customer has the highest customer ID number whose name starts with an 'E' and has an address ID lower than 500?**

Solution
1.	SELECT first_name, last_name FROM customer

Retrieves the first_name and last_name columns 

2.	WHERE first_name LIKE 'E%'

Filters by the customer’s  first name  which begins with the letter ‘E’

3.	AND address_id <500

Adds a secondary filter by the customer’s address_id which is less than 500

4.	ORDER BY customer_id DESC

Sorts the customer’s id number 
 in descending order 

5.	LIMIT 1;

Returns only on row of  the final result 









