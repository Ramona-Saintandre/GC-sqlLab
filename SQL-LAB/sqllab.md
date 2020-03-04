SQL LAB
TASK:
Practice writing SQL statements on the Northwind database.
SETUP:
● In pgAdmin, create a database called northwind.
● Open up a SQL window. Copy-paste and run this file...
https://raw.githubusercontent.com/pthom/northwind_psql/master/northwind.sql
DETAILS:
Write SQL queries to do the following tasks. Record these queries in a text document so you
can repeat them in class.
[**NOTES**](https://www.postgresqltutorial.com/postgresql-select/)

1. Select all the records from the "Customers" table.   

SELECT *
from customers;

2. Get distinct countries from the Customers table.

SELECT country 
From customers;


3. Get all the records from the table Customers where the Customer's ID starts with "BL".


4. Get the first 100 records of the orders table.


5. Get all customers that live in the postal codes 1010, 3012, 12209, and 05023.


6. Get all orders where the ShipRegion is not equal to NULL.


7. Get all customers ordered by the country, then by the city.


8. Add a new customer to the customers table. You can use whatever values/

insert into public.customers (customer_id, company_name,contact_name,contact_title) values ('GCAHB','vaneerden','Ramona Saintandre','Helpdesk')

9. Update all ShipRegion to the value 'EuroZone' in the Orders table, where the ShipCountry is equal to France.  


10. Delete all orders from `order_details` that have a quantity of 1  


11. Calculate the average, max, and min of the quantity at the `order details` table.


12. Calculate the average, max, and min of the quantity at the `order details` table,grouped by the orderid.  


13. Find the CustomerID that placed order 10290 (orders table)


## BONUS:
14. Do an inner join, left join, right join on orders and customers tables.


15. Get first names of all employees who report to no one.


16. Get first names of all employees who report to Andrew.