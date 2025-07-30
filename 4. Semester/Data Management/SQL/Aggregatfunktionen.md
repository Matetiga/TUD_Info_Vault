## max() / min() / avg() / count()
- this will select the minimum/max Value of the column Umsatz of the table "R" 
- sum() / avg() folgen dasselbe Syntax
```SQl
SELECT min(Umsatz)
       max(Umsatz)
FROM R
```

---

## SUM() / +
Both operators are used for addition, but have different specifications
### SUM()
- Used to sum **across multiple rows in a table** 
- Used to compute a single value across a group of rows 
```sql
SELECT SUM(column_name) AS total
FROM table_name;
```

### +
- Used to add values **across the same row**
```sql
SELECT column1 + column2 AS row_sum
FROM table_name;
```