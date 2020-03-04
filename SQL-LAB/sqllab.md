## SQL LAB 

**[W3schools SQL](https://www.w3schools.com/sql/default.asp)**<br>  
**TASK**:  
Practice writing SQL statements on the Northwind database. <br> 

**SETUP**:  
● In pgAdmin, create a database called northwind.  
● Open up a SQL window. Copy-paste and run this file...  
https://raw.githubusercontent.com/pthom/northwind_psql/master/northwind.sql  

**DETAILS**:  
Write SQL queries to do the following tasks. Record these queries in a text document so you
can repeat them in class. <br>   
[**NOTES**](https://www.postgresqltutorial.com/postgresql-select/)

## 1. Select all the records from the "Customers" table.   

```pgsql
SELECT *
from customers;
```

## 2. Get distinct countries from the Customers table.

# TODO ** need to figure out how to concatinate this**
```pgsql
Select *FROM customers 
Where country ='Germany;

Select *FROM customers 
Where country ='Canada';
```

## 3. Get all the records from the table Customers where the Customer's ID starts with "BL".  

```pgsql
Select * FROM customers 
Where customer_id LIKE 'BL%';
```
## 4. Get the first 100 records of the orders table.

```pgsql
Select * FROM orders LIMIT 100;
```
## 5. Get all customers that live in the postal codes 1010, 3012, 12209, and 05023.  

```pgsql
Select * FROM customers 
WHERE 
postal_code='1010' 
OR
postal_code='3012'
OR
postal_code='12209'
OR
postal_code='05023';
```

## 6. Get all orders where the ShipRegion is not equal to NULL.    

**need to find out what is different, both work**

```pgsql
SELECT *
FROM orders
WHERE orders.ship_region IS NOT null;

Select * FROM orders
Where ship_region IS NOT null;
```

## 7. Get all customers ordered by the country, then by the city.  

**why can't this be done for the zip codes**

```pgsql
Select * FROM customers
ORDER BY country,city;
```

## 8. Add a new customer to the customers table. You can use whatever values  

[create a user](https://chartio.com/docs/data-sources/faqs/create-a-user-with-pgadmin/)

```pgsql
insert into public.customers (customer_id, company_name,contact_name,contact_title) values ('GCAHB','vaneerden','Ramona Saintandre','Helpdesk')
```
## 9. Update all ShipRegion to the value 'EuroZone' in the Orders table, where the ShipCountry is equal to France.  

```pgsql
UPDATE orders SET ship_region='EuroZone' 
WHERE ship_country='France';
```
## 10. Delete all orders from `order_details` that have a quantity of 1 

```pgsql
DELETE  FROM order_details 
WHERE quanity=1;
```
## 11. Calculate the average, max, and min of the quantity at the `order details` table.

```pgsql
SELECT order_id, AVG(quantity)FROM order_details GROUP BY order_id;
SELECT order_id, MAX(quantity)FROM order_details GROUP BY order_id;
SELECT order_id, MIN(quantity)FROM order_details GROUP BY order_id;
```
## 12. Calculate the average, max, and min of the quantity at the `order details` table,grouped by the orderid.  

**NOTE** Watch th spaces in SQL
```pgsql
SELECT AVG(quanity) FROM order_details GROUP BY order_id;
SELECT MAX(quanity) FROM order_details GROUP BY order_id; 
SELECT MIN(quanity) FROM order_details GROUP BY order_id;
```
## 13. Find the CustomerID that placed order 10290 (orders table)

  ```pgsql
SELECT contact_name, customers.customer_id 
FROM customers JOIN orders 
ON customers.customer_id= orders.customer_id 
WHERE orders.order_id='10290'
```
## BONUS:

## 14. Do an inner join, left join, right join on orders and customers tables.

[SQL INNER JOIN Keyword](https://www.w3schools.com/sql/sql_join_inner.asp)
[SQL LEFT JOIN Keyword](https://www.w3schools.com/sql/sql_join_left.asp)
[SQL RIGHT JOIN Keyword](https://www.w3schools.com/sql/sql_join_right.asp)

```pgsql
SELECT * FROM orders INNER JOIN customers ON customer_id = customers.customer_id;
SELECT * FROM orders LEFT JOIN customers ON customer_id = customers.customer_id;
SELECT * FROM orders RIGHT JOIN  customers ON customer_id = customers.customer_id;```

## 15. Get first names of all employees who report to no one.

[SQL NULL Functions](https://www.w3schools.com/sql/sql_isnull.asp)
[SQL NULL Values](https://www.w3schools.com/sql/sql_null_values.asp)
```pgsql
SELECT first_name FROM employees WHERE reports_to IS NULL;
```
## 16. Get first names of all employees who report to Andrew.

**Need to double check this**

```pgsql
SELECT first_name FROM employees 
WHERE  reports_to=2;
```
```pgsql
SELECT first_name FROM employees
WHERE first_name='Andrew'; (2)
SELECT first_name FROM employees 
WHERE reportsto ='2';
```