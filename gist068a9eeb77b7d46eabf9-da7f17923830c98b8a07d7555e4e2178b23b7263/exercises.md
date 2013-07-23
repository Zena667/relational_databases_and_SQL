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
  * What does `int(11)` mean?
  * What is `users` in this statement?
2. Explain the concept of a primary key.
3. Explain the concept of a foreign key.

## Queries

All the following questions deal with the attached SQL database. Make sure you follow the directions in the Google Doc on how to import the database.

1. Get a list of all the usernames from the users table.
2. Get the name of all users who have placed orders for an iPhone
3. Get a list of all the users (id's are fine) who have placed orders over 300$. _N.B._ The cost in the products table is in cents, not dollars.