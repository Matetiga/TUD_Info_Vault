## Basic syntax
- this will select and show only the first name of the list of masculine patients
```SQL
SELECT first_name
FROM patients
WHERE gender="M"
```

---

## Sortierung der Ausgabe
- mit *ORDER BY* ... *asc/desc*
```SQL
SELECT first_name
FROM patients
WHERE gender="M"
ORDER BY first_name asc
```


---

## Duplikate Sortieren 
- with *distinct*
```SQL
SELECT distinct gender
FROM patients
```

---

## Concatenate String 
```SQL
SELECT CONCAT(first_name, ' ' , last_name) AS full_name
FROM patients
```