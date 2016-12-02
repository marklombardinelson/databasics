## Example:
# 1 How many users are there?
1.
 - `SQL:`
    SELECT count(\*) from items

 - `ANSWER:`
   100
# 2 What are the titles of the 5 most expensive items?
2.
 - `SQL:`
    Select title, price  FROM items ORDER BY price DESC
 - `ANSWER:`
    9984, 9859, 9790, 9390

# 3 What's the cheapest item in the Books category?
3.
  - `SQL:`
     Select title, price, category  FROM items ORDER BY price ASC
  - `ANSWER:`
     1496

# 4 Who lives at 6439 Zetta Hills, Willmouth, WY?
4.
   - `SQL:`
   SELECT first_name, last_name, street, state  FROM users, addresses where addresses.user_id = users.id and street = '6439 Zetta Hills' and city = 'Willmouth' and state = 'WY'

   - `ANSWER:`
      Corrine Little

# 5 Correct Virginie Mitchell's address to "New York, NY, 10108".
5.
    - `SQL:`
       SELECT addresses.id, first_name, last_name, street, city, state, zip  FROM users, addresses where addresses.user_id = users.id and first_name = 'Virginie' and last_name = 'Mitchell'

       UPDATE addresses SET zip = '10108', city = 'New York, New York', state = 'NY' WHERE id = 41

    - `ANSWER:`
       41 | Virginie     | Mitchell    | 12263 Jake Crossing | New York, NY | 10108

# 6  How much would it cost to buy one of each item in the Tools category?
6.
     - `SQL:`
        SELECT SUM(price) FROM items WHERE category = 'Tools'

     - `ANSWER:`
        7383
# 7 How many total items did we sell?
7.
      - `SQL:`
         SELECT SUM(quantity) FROM orders, items WHERE orders.item_id = items.id

      - `ANSWER:`
         2125

# 8  How much was spent on Books?
8.
       - `SQL:`
          SELECT category,SUM(items.price * orders.quantity) AS spent FROM orders INNER JOIN items ON items.id = orders.item_id GROUP BY items.category, items.price  ORDER BY price ASC

       - `ANSWER:`
          22440

# 9  Simulate buying an item by inserting a User for yourself and an Order for yourself.
9.
        - `SQL:`
           INSERT INTO users (first_name,last_name,email)VALUES ('Mark', 'Lombardi', 'mark@gmail.com')   
           SELECT id FROM users WHERE first_name='Mark' AND last_name='Lombardi'  
           SELECT id, title FROM items   
           INSERT INTO orders (user_id,item_id,quantity,created_at)VALUES (1,82,1,'2015-02-09 00:40:30.515793')

        - `ANSWER:`


#Adventure Mode
---------------------------------------------------------


# 1 What are the titles of the 5 most expensive items?
1.
         - `SQL:`

         - `ANSWER:`

# 2 What are the titles of the 5 most expensive items?
2.
          - `SQL:`

          - `ANSWER:`

# 3 What are the titles of the 5 most expensive items?
3.
                    - `SQL:`

                    - `ANSWER:`
