## Syntax
``` SQL
INSERT INTO <Relationen-Name>[(<Attributname> [, <Attributname>]*)]
VALUES (<Konstante> [, Konstante]*)
```
oder 
Kopieren der Information aus einer anderen Tabelle
``` SQL
INSERT INTO <Relationen-Name>[(<Attributname> [, <Attributname>]*)]
SELECT … FROM ... WHERE 
```

- Spalten Liste ist Optional, wenn alle Spalten gegebenkommen 
- Man kann mehrere Zeile (Tupeln) auf einmal hinzüfugen, wenn man mehrere Zeile mit `VALUES` schreibt

### Beispiele 
``` SQL
INSERT INTO Kunde(KName, KAdresse, Kto)
VALUES ('Müller', 'Musterhausen', '1.000')
       ('Meier', 'Musterhausen', '2.000')

INSERT INTO Kunde -- Ohne Spaltennamen
VALUES ('Müller', 'Musterhausen', '1.000')
```