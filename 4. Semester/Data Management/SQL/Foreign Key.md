Used to establish a relationship between two tables 

## Definition 
A *foreign key is a column* (or set of columns) in one table that **refers to the primary key (or a unique key) in another table**
- It creates a link between the two tables, ensuring referential integrity—meaning the values in the foreign key column must match an existing value in the referenced table’s primary key (or unique key) or be NULL (if allowed)


![[Primary Key#Example]]
### Example

```SQL
CREATE TABLE Auftrag
	(KName CHAR(20) references Kunde,
	Ware VARCHAR(50),
	MENGE INTEGER,
	PRIMARY KEY (Kname, Ware)

-- ODER

CREATE TABLE Auftrag
	(KName CHAR(20),
	Ware VARCHAR(50),
	MENGE INTEGER,
	PRIMARY KEY (Kname, Ware),
	FOREIGN KEY (KName) references Kunde(Kname))
```


---

## Cascade-Änderung 
- Veränderung des Primärschlussels werden in den Tabellen mit dem Fremdschlussel **propagiert**
- On update / on delete
### Beispiel 
```SQL
CREATE TABLE Auftrag
	(KName CHAR(20) references Kunde on update cascade, -- on delete
	Ware VARCHAR(50),
	MENGE INTEGER,
	PRIMARY KEY (KName, Ware))
```


### Set NULL Eingabe 
- Falls Information einer Spalte gelöscht, dann wird es mit NULL gefüllt 
```SQL
CREATE TABLE Auftrag
	(KName CHAR(20) references Kunde on update set null,
	Ware VARCHAR(50),
	MENGE INTEGER,
	PRIMARY KEY (KName, Ware))
```
![[Pasted image 20250526165917.png]]
