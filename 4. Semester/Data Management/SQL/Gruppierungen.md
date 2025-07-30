
## GROUP BY 
- to organize rows with identical values (strings or integers)
- this uses [[Aggregatfunktionen]]
- the table will be organized by to columns, adding all Umsatz values of the same year
```SQL
SELECT Jahr, SUM(Umsatz)
FROM R
GROUP BY Jahr
```

---
## Filter the Group
- `having` Filters the result when "*Group by*" is used, based on [[Aggregatfunktionen]]
	- the following example will group all cities that belong to the same country
	- and calculate the *total_population*
```sql
SELECT country, SUM(population) AS total_population
FROM city
GROUP BY country
HAVING SUM(population) > 5000000;
```