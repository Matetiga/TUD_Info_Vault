## Syntax
```SQL
UPDATE <Relationen-Name>
SET <Attributname> = <Ausdruck> [,
<Attributname> = <Ausdruck>]*
[WHERE <Bedingung>]
```


### Beispiel 
```SQL 
UPDATE Kunde
SET KAdresse = 'Berlin'
WHERE KName = 'Müller'
```