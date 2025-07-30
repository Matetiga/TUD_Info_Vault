![[Pasted image 20250512093140.png]]
### Horizontale Abbildung: 
- Alle Klassen haben ihre eigene speziallizierte Tabelle (keine Tabelle wird geteilt)
```sql
(SELECT "Product", id, price, stock FROM products)
UNION
(SELECT "Book", id, price, stock FROM book)
UNION
(SELECT "CD", id, price, stock FROM cd)
```
### Vertikale Abbildung
- Die Kinderklassen haben unterschiedliche Tabellen für ihre eigene Attribute 
	- Das ID in der Produkt Tabelle muss eindeutig sein (so können die Tabelle miteinander verbunden werden)
```sql
-- gesamte extension 
SELECT id, price, stock
FROM product

-- Zusammensetzung der Tabellen 
SELECT id, price, stock, isbn, title, album, artist
FROM (product
LEFT OUTER JOIN book ON product.id = book.id)
LEFT OUTER JOIN cd ON product.id = cd.id
```

### Universalrelation
- Alles wird in einer Tabelle reingepackt. 
	- Die spezielle Attribute jede Kinerklasse machen eine neue Spalte
	- Falls ein Produkt nicht ein spezifisches Attribut hat, wird diese *Zelle mit NULL* gefüllt 
```sql
(SELECT "Product",id,price,stock,NULL AS isbn,NULL AS title,NULL AS album, NULL AS artist FROM products)
UNION
(SELECT "Book",id,price,stock,isbn,title,NULL AS album,NULL AS artist FROM book)
UNION
(SELECT "CD",id,price,stock,NULL AS isbn,NULL AS title,album,artist FROM cd)
```