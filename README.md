# SQL-Queries

**A few Solutions to business problems utilizing SQL **
Problem 1


**•	Return the customer IDs of customers who have spent at least $110 with the staff member who has an ID of 2.**


Solution
1.	SELECT customer_id , SUM(amount)

Selects the Customer id and Amount fields/columns from the payment table. Sum(amount) Aggregates the total payment made by each unique customer?customer_id .

2.	FROM payment

The table with the data we need to perform the query

3.	WHERE staff_id = 2

The where clause acts as a filter to limit the result of the query based on specific parameters i.e. Only return a result of staff member whose id number is 2.

4.	GROUP BY customer_id
Group  BY clause used to group the values in customer_id column of the payment table

5.	HAVING SUM(amount) > 110;
Returns values of the sum total payment that is greater than 110   









