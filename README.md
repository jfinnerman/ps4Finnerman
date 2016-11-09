# ps4Finnerman
## Problem Set 4 

1. Create three tables: Customers, Orders, and OrderItems.
 
 CREATE TABLE `Customers` (
  `customer_id` int(11) NOT NULL,
  `first_name` varchar(45) COLLATE utf8_unicode_ci NOT NULL,
  `last_name` varchar(45) COLLATE utf8_unicode_ci NOT NULL,
  `email` varchar(45) COLLATE utf8_unicode_ci DEFAULT NULL,
  `phone_number` varchar(45) CHARACTER SET utf8 DEFAULT NULL,
  `zip` char(5) CHARACTER SET utf8 DEFAULT NULL,
  `address` varchar(45) COLLATE utf8_unicode_ci DEFAULT NULL,
  PRIMARY KEY (`customer_id`)
  ) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;
  
   CREATE TABLE `Order Items` (
  `orderItems_id` int(11) NOT NULL,
  `quantity` int(11) NOT NULL DEFAULT '1',
  `order_id` int(11) DEFAULT NULL,
  `product_id` int(11) DEFAULT NULL,
  PRIMARY KEY (`orderItems_id`),
  KEY `order_id_idx` (`order_id`),
  KEY `product_id_idx` (`product_id`),
  CONSTRAINT `order_id` FOREIGN KEY (`order_id`) REFERENCES `Orders` (`order_id`) ON DELETE CASCADE ON UPDATE CASCADE,
  CONSTRAINT `product_id` FOREIGN KEY (`product_id`) REFERENCES `Products` (`product_id`) ON DELETE CASCADE ON UPDATE CASCADE
  ) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;
  
  CREATE TABLE `Orders` (
  `order_id` int(11) NOT NULL,
  `customer_id` int(11) DEFAULT NULL,
  `orderItem_id` int(11) DEFAULT NULL,
  `date` date DEFAULT NULL,
  `time` time DEFAULT NULL,
  PRIMARY KEY (`order_id`),
  KEY `customer_id_idx` (`customer_id`),
  CONSTRAINT `customer_id` FOREIGN KEY (`customer_id`) REFERENCES `Customers` (`customer_id`) ON DELETE CASCADE ON UPDATE CASCADE
  ) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;

2. Why do we need an OrderItems table?
  We need an OrderItems table in order to link the products table with the orders table and organize the items that wered ordered by customers.
3. Create linked tables in MS Access.

4. Create forms to enter customer data.

5. Create a form with a subform to enter orders and order item.

6. Use forms created in 4 and 5 to insert Customers and Orders.  Add customers that have not made any orders. Make the number of entries relatively small.  Why?  
 
  The number of entries should be relatively small because if there is a large number of entries then the data will be too big and it would be difficult to analyze everything in the data, especially smaller bits in the data. 

7. Use SQL DML to INSERT records into Customers and Orders (and OrderItems). 

  INSERT INTO `unemath_Finnerman`.`Customers` (`customer_id`, `first_name`, `last_name`, `email`, `phone_number`, `zip`, `address`) VALUES ('910360420', 'Reginald', 'Sparks', 'regisparks@gmail.com', '6038675309', '04005', '235 Sepulveda Dr');
  
  INSERT INTO `unemath_Finnerman`.`Customers` (`customer_id`, `first_name`, `last_name`, `email`, `phone_number`, `zip`, `address`) VALUES ('69779684', 'Juan', 'Cote', 'juanjose97@aol.com', '8884588768', '04106', '123 Jose Dr');
   
   INSERT INTO `unemath_Finnerman`.`Orders` (`Order_id`, `Customer_id`, `OrderItem_id`, `date`, `time`) VALUES ('0420', '69779684', '1217', '2016-07-11', '1200');
   
   INSERT INTO 'unemath_Finnerman`.`Orders` (`Order_id`, `Customer_id`, `OrderItem_id`, `date`, `time`) VALUES ('5555', '910360420', '1111', '2016-07-11', '1200');
   
8. Find all customer orders.

9. Select all customers that orders a certain product (This will depend on what data you entered into the table).  Find all customers that ordered product 3452.  

10. List 5 questions that you can answer from this data.
