Bendingungen bei einem Feld hizuzufügen

```SQL
CREATE TABLE Auftrag
	(KName CHAR(20) references Kunde,
	Ware VARCHAR(50),
	MENGE INTEGER check between 1 and 100,
	PRIMARY KEY (Kname, Ware))
```


## Bedingungen Ändern 
```SQL
ALTER TABLE <table-name> ADD CONSTRAINT <constraint-name>
| PRIMARY KEY (<attribute-list>)
| FOREIGN KEY (<attr-list>) REFERENCES <table-nm>(<att-list>)
| UNIQUE (<attribute-list>)
| CHECK (<predicate>)
```

## Daten Integrität
- Kardinalität
- Generalsierungsbeziehungen ([[Spezialisierung und Generallisierung]])
- Entitäten haben Datentypen 
### Referenezielle Integrität
- [[Primary Key]]
- [[Foreign Key]]
- [[Foreign Key#Cascade-Änderung|Cascade-Änderung]]
