## Mit Subqueries 
### IN
- Die Menge von Language wird mit der Menge an Countries (mit der Bedingung, dass sie in der EU sind) verbunden 
```sql
select name, count(name)
from language 
where language.country in (select country from is_Member inner join country on country.code = is_Member.country where is_Member.organization ='EU' and is_Member.type='member') 
group by name
```