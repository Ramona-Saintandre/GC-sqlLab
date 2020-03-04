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

`SELECT *
from customers;`

## 2. Get distinct countries from the Customers table.

# TODO ** need to figure out how to concatinate this**

`Select *FROM customers 
Where country ='Germany;`
 
`Select *FROM customers 
Where country ='Canada';`

## 3. Get all the records from the table Customers where the Customer's ID starts with "BL".  

`Select * FROM customers 
Where customer_id LIKE 'BL%';`

## 4. Get the first 100 records of the orders table.  

`Select * FROM orders LIMIT 100;`

## 5. Get all customers that live in the postal codes 1010, 3012, 12209, and 05023.  

`Select * FROM customers 
WHERE 
postal_code='1010' 
OR
postal_code='3012'
OR
postal_code='12209'
OR
postal_code='05023';`


## 6. Get all orders where the ShipRegion is not equal to NULL.    

**need to find out what is different, both work**
`SELECT *
FROM orders
WHERE orders.ship_region IS NOT null;`

`Select * FROM orders
Where ship_region IS NOT null;` 

## 7. Get all customers ordered by the country, then by the city.  

**why can't this be done for the zip codes**

`Select * FROM customers
ORDER BY country,city;`


## 8. Add a new customer to the customers table. You can use whatever values  

[create a user](https://chartio.com/docs/data-sources/faqs/create-a-user-with-pgadmin/)

`insert into public.customers (customer_id, company_name,contact_name,contact_title) values ('GCAHB','vaneerden','Ramona Saintandre','Helpdesk')`


## 9. Update all ShipRegion to the value 'EuroZone' in the Orders table, where the ShipCountry is equal to France.  



## 10. Delete all orders from `order_details` that have a quantity of 1 




## 11. Calculate the average, max, and min of the quantity at the `order details` table.




## 12. Calculate the average, max, and min of the quantity at the `order details` table,grouped by the orderid.  




## 13. Find the CustomerID that placed order 10290 (orders table)

  


## BONUS:

## 14. Do an inner join, left join, right join on orders and customers tables.


## 15. Get first names of all employees who report to no one.


## 16. Get first names of all employees who report to Andrew.