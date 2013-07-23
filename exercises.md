# Exercises 

In order to learn SQL, we'll go through some simple exercises to start

1. Given the following statement:

  ``` sql
  CREATE TABLE `users` (
    `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
    `email` varchar(255) NOT NULL,
    `password` varchar(32) NOT NULL,
    PRIMARY KEY (`id`)
  );
  ```
  * What does the `AUTO_INCREMENT` flag do?
  It helps to generate unique identity for new rows by generating incremental numbers.
  * What does `int(11)` mean?
  An Integer data type with a with a display width of 11 digits.
  * What is `users` in this statement?
  Users is the name of the table.
2. Explain the concept of a primary key.
  It references a column that contains unique values.  This value is used to identify each row and each row must have one.
3. Explain the concept of a foreign key.
  It is a value that references the primary key of another table.  This relationship is used to be able to share data between
  two tables via a common reference point.

## Queries

All the following questions deal with the attached SQL database. Make sure you follow the directions in the Google Doc on how to import the database.

1. Get a list of all the usernames from the users table.
SELECT email FROM users;

2. Get the name of all users who have placed orders for an iPhone
SELECT email 
	FROM users LEFT JOIN shopping_carts ON users.id = shopping_carts.user_id
		WHERE product_id = 1;
3. Get a list of all the users (id's are fine) who have placed orders over 300$. _N.B._ The cost in the products table is in cents, not dollars.
SELECT `user_id`
	FROM shopping_carts LEFT JOIN products ON products.id = shopping_carts.product_id
		WHERE products.cost * shopping_carts.quantity/100 > 300;
