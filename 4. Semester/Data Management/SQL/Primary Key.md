## Definition 
A primary key is a column (or a combination of columns) in a table that **uniquely identifies each row in that table**
- It ensures that no two rows can have the same primary key value
- Enforces Data Integrity -> No NULL values in the primary key columns 
- Only One Primary Key per Table 


### Example
```SQL
CREATE TABLE Kunde
	(KName CHAR(20) PRIMARY KEY,
	KAdresse VARCHAR(50),
	Kto DECIMAL(7))
```
