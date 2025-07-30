## INNER JOIN
- used to combine **rows of different tables with on a related column** returning only the **rows where there is a match in both** tables

- INNER JOIN .. ON *condition to form the match*
```SQL
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```


---

## OUTER JOIN 
- The table will also include values where there are no match (*NULL values*)

### LEFT OUTER JOIN 
- Returns **all rows from the left table** (the first table in the query) and the **matching rows from the right table**. If there’s no match in the right table, NULL is returned for the right table’s columns

```txt 
Customers:
customer_id | name
------------+--------
1          | Alice
2          | Bob
3          | Charlie

Orders:
order_id | customer_id | amount
----------+------------+--------
101      | 1          | 50
102      | 1          | 75
103      | 2          | 100
```
```SQL
SELECT customers.name, orders.order_id, orders.amount
FROM customers
LEFT OUTER JOIN orders
ON customers.customer_id = orders.customer_id;
```
```txt
name    | order_id | amount
--------+----------+--------
Alice   | 101      | 50
Alice   | 102      | 75
Bob     | 103      | 100
Charlie | NULL     | NULL
```

### RIGHT OUTER JOIN 
- Returns **all rows from the right table** (the second table in the query) and the **matching rows from the left table**. If there’s no match in the left table, NULL is returned for the left table’s columns.
```txt 
Customers:
customer_id | name
------------+--------
1          | Alice
2          | Bob
3          | Charlie

Orders:
order_id | customer_id | amount
----------+------------+--------
101      | 1          | 50
102      | 1          | 75
103      | 2          | 100
```
```SQL
SELECT customers.name, orders.order_id, orders.amount
FROM customers
RIGHT OUTER JOIN orders
ON customers.customer_id = orders.customer_id;
```
```txt
name   | order_id | amount
-------+----------+--------
Alice  | 101      | 50
Alice  | 102      | 75
Bob    | 103      | 100
```
### FULL OUTER JOIN 
- Returns **all rows from both tables**, with NULL in places where there’s no match in the other table. It combines the behavior of LEFT and RIGHT JOINs.
```txt
Customers:
customer_id | name
------------+--------
1          | Alice
2          | Bob
3          | Charlie

Orders: 
order_id | customer_id | amount
----------+------------+--------
101      | 1          | 50
102      | 1          | 75
103      | 2          | 100
104      | 4          | 200
```
```SQL
SELECT customers.name, orders.order_id, orders.amount
FROM customers
FULL OUTER JOIN orders
ON customers.customer_id = orders.customer_id;
```
```txt
name    | order_id | amount
--------+----------+--------
Alice   | 101      | 50
Alice   | 102      | 75
Bob     | 103      | 100
Charlie | NULL     | NULL
NULL    | 104      | 200
```
---