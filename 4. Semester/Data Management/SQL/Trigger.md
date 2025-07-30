## Syntax
```SQL
CREATE TRIGGER <trigger-name>
BEFORE | AFTER | INSTEAD OF
INSERT | DELETE | UPDATE [OF (<column>, …)]
ON <table-name> or <view-name>
REFERENCING [OLD AS <name>] [NEW AS <name>]
			[OLD_TABLE AS <name>] [NEW_TABLE AS <name>]
FOR EACH ROW | FOR EACH STATEMENT
[WHEN (<condition>)]
BEGIN ATOMIC
<sql-stmt> | <dynamic-compound-sql-stmt>
END
```

### Entfernen von triggern 
```SQL
DROP TRIGGER <trigger-name>
```

### Beispiel 
```SQL
CREATE TRIGGER NeuerAng      -- Triggername
AFTER                        -- Triggeraktivierungszeit
INSERT ON Mitarbeiter        -- Triggerereignis
FOR EACH ROW                 -- Triggergranularität
UPDATE UnternehmensStatistik -- Triggeraktion
SET AnzAng = AnzAng + 1
```

---

## Before Trigger
- zu Überprüfung der Eingabedaten auf Korrektheit 
- Automatisches Generieren von Werten für neu eingefügte Tupel

### Beispiel
```SQL
-- Bringt Anfang und Ende einer Unterrichtsstunde in chronologische Reihenfolge
CREATE TRIGGER CLASS_END
BEFORE INSERT ON CL_SCHED
REFERENCING NEW AS new_row
FOR EACH ROW
BEGIN ATOMIC
	DECLARE t TIME;
	IF new_row.STARTING > new_row.ENDING THEN
		SET t = new_row.ENDING;
		SET new_row.ENDING = new_row.STARTING;
		SET new_row.STARTING = t;
	END IF;
END
```

---

## Instead Of-Trigger
![[Pasted image 20250526172325.png]]