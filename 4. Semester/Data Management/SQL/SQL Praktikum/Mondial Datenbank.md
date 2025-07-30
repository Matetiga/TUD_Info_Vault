## Aufgaben
### a)
```sql
select NAME, POPULATION from CITY order by population desc
```

### b) 
```sql
select city from located where river IS NOT NULL and lake IS NOT NULL
```

### c)
```sql
select name, population from city where country='D' order by population desc
```

### d)
```sql
SELECT distinct name 
FROM Language, ENCOMPASSES 
where LANGUAGE.COUNTRY = ENCOMPASSES.COUNTRY and continent='Europe'
```

### e)
```sql
/* table of all countries in EU*/
SELECT * 
from is_Member
inner join country
on country.code = is_Member.country
where is_Member.organization ='EU' and is_Member.type='member'

/* Languages in the EU */
select name, count(name)
from language 
where language.country in (select country from is_Member inner join country on country.code = is_Member.country where is_Member.organization ='EU' and is_Member.type='member') 
group by name
```


### f)
```sql
/* All country's capital with more than 30% of the country's population living in the capital*/
select country.name, country.capital, country.population, city.population as city_pop, cast(city.population as double precision)/cast(country.population as double precision) * 100 as average
from city
inner join country
on country.capital = city.name 
where cast(city.population as double precision)/cast(country.population as double precision) * 100  > 30.0 and country.code = city.country
order by average desc
```

### g)
```sql
select name 
from country
where code in (select country
from geo_mountain
inner join mountain
on mountain.name = geo_mountain.mountain
where mountain.height >= 4000)
```


### h)

```sql
select capital_list_country
from city 
inner join(select distinct city.name, city.population as capital_population, country.code, country.name as capital_list_country
from city
inner join country on city.name = country.capital and city.country = country.code) as capital_list
on city.country = capital_list.code
where city.population > capital_list.capital_population
group by capital_list_country

```

### i)
```sql
select country.name,  sum(city.population)
from country
inner join city on country.code = city.country
where city.population > 1000000
group by city.country
order by sum(city.population) desc
```

### j)
```sql

select country.name , borders.length, total.total_sum
from borders
inner join country  on borders.country1 = country.code
inner join (select sum(length) as total_sum
from borders 
where borders.country1 = 'D' or borders.country2 = 'D'
) as total
where borders.country1 = 'D' or borders.country2 = 'D'
group by country.name

```


### k)
>[!Error]
>expected 6, got 4
```sql
/* Tabelle aller Millionstaedten */
select country.name, city.name, city.population
from country
inner join city on country.code = city.country
where city.population > 1000000

/* Tabelle mit Lander und Einwohner Prozentzahl */
select country.code, country.population, million_city.city_name, mill_city_pop, cast(mill_city_pop as double precision)/cast(country.population as double precision) * 100 as percentage
from country
inner join
(select country.code, city.name as city_name, city.population  as mill_city_pop
from country
inner join city on country.code = city.country
where city.population > 1000000) as million_city
on million_city.code = country.code
where cast(mill_city_pop as double precision)/cast(country.population as double precision) * 100 > 30

/* Hasi Answer*/
SELECT DISTINCT COUNTRY.NAME, SUM(CITY.POPULATION), country.population
FROM COUNTRY
INNER JOIN CITY 
ON CITY.COUNTRY = COUNTRY.CODE 
WHERE CITY.POPULATION > 1000000 
GROUP BY COUNTRY.NAME
HAVING SUM(CITY.POPULATION) > COUNTRY.POPULATION * 0.3 
ORDER BY SUM(CITY.POPULATION) // COUNTRY.POPULATION asc
```


### l)
>[!Error]
>expected 12, got 14
```sql
/* counted list with lake amount per country */
select geo_lake.country, count(geo_lake.country)
from geo_lake 
group by geo_lake.country


/* list with countries with more lakes than mountains*/
select *
from 
(select geo_lake.country as c_lakes_country, count(geo_lake.country) as c_lakes_count
from geo_lake 
group by geo_lake.country) as c_lakes
inner join
(select geo_mountain.country as c_mountains_country, count(geo_mountain.country) as c_mountains_count
from geo_mountain
group by geo_mountain.country) as c_mountains
on c_lakes_country = c_mountains_country  
where c_lakes_count > c_mountains_count
order by c_lakes_count desc
```

### m)
```sql
/* amount of neighbors per country */
select border1.code1 as country, border1.c_1 + border2.c_2 as total_neighbors
from (select borders.country1 as code1, count(borders.country1) as c_1
from borders 
group by borders.country1) as border1
inner join (select borders.country2 as code2, count(borders.country2) as c_2
from borders 
group by borders.country2) as border2
on border1.code1 = border2.code2
where border1.c_1 + border2.c_2  > 9 /* for countries with more neighbors than gemany */
order by total_neighbors desc
```

### n)
```sql
select city.name, city.population, country.name
from city 
inner join country
on country.code = city.country
order by population desc
limit 1 /*to limit the amount of entries in the table*/
```