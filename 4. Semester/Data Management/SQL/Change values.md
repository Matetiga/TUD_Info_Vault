## Syntax
```SQL
UPDATE table_name
SET column_name = new_value
WHERE condition;
```

### Example
- change all Entries of a column with : *NULL* value
```SQL
update patients
set allergies = 'NKA'
where allergies is NULL
```