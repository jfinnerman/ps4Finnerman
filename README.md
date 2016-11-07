# ps4Finnerman
## Problem Set 4 

1. Create three tables: Customers, Orders, and OrderItems.

2. Why do we need an OrderItems table?
  We need an OrderItems table in order to link the products table with the orders table and organize the items that wered ordered by customers.
3. Create linked tables in MS Access.

4. Create forms to enter customer data.

5. Create a form with a subform to enter orders and order item.

6. Use forms created in 4 and 5 to insert Customers and Orders.  Add customers that have not made any orders. Make the number of entries relatively small.  Why?  
 


7. Use SQL DML to INSERT records into Customers and Orders (and OrderItems). 

  INSERT INTO `unemath_Finnerman`.`Customers` (`customer_id`, `first_name`, `last_name`, `email`, `phone_number`, `zip_id`, `address`) VALUES ('910360420', 'Reginald', 'Sparks', 'regisparks@gmail.com', '6038675309', '04005', '235 Sepulveda Dr');
   INSERT INTO `unemath_Finnerman`.`Customers` (`customer_id`, `first_name`, `last_name`, `email`, `phone_number`, `zip_id`, `address`) VALUES ('69779684', 'Juan', 'Cote', 'juanjose97@aol.com', '8884588768', '04106', '123 Jose Dr');
   
8. Find all customer orders.

9. Select all customers that orders a certain product (This will depend on what data you entered into the table).  Find all customers that ordered product 3452.  

10. List 5 questions that you can answer from this data.
