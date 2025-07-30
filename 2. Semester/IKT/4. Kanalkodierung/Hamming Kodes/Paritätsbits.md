Ist ein zusätliches Bit, welches man zu einem Kodewort hinzufügt, um einfache Fehlererkennung in Datenübertragungen zu ermöglichen
- Die Gesamtanzahl an Bits (inklusiv das Paritätsbit wird berechnet)

## Gerade Parität
<span style="color:#ffff00">Anzahl der "1" bits im Kodewort ist gerade </span>
- `1101001` => **Gerade** anzahl an **1-bits**
- `11010010` => dann **ergänzt man mit Paritätsbit** = $0$
Man will das die Anzahl der Bits im Wort gerade bleibt, deswegen setzt man ein Paritätsbit = 0 falls die Anzahl an Bits schon gerade ist 

## Ungerade Parität 
<span style="color:#ffff00">Anzahl der "1" bits im Kode ist ungerade</span> 
- `1100000` => Gerade Anzahl an 1-bits
- `11000001` => dann **ergänzt man mit Paritätsbit** = $1$
Man will das die Anzahl der Bits im Wort ungerade bleibt, deswegen setzt man ein Paritätsbit = 0 falls die Anzahl an Bits schon ungerade ist 