Basiert sich auf [[größter gemeinsamen Teiler]] mit :

$$ggT(a,b)=ggT(b,(a \ \ \mod \ b))$$
- mit $a(x)$ und $b(x)$ folgt:
- 
### Schritte des Algorithmus
1. Starte mit zwei Zahlen $a$ und $b$, wobei $a≥b$
2. Teile $a$ durch $b$ und bestimme den Rest $r$, d. h. $r = a \mod b$
3. Ersetze $a$ durch $b$ und $b$ durch $r$.
4. Wiederhole Schritt 2 und 3, bis $r=0$
5. Der letzte Wert von $b$ ist der ggT.

---

#### Beispiel
- $ggt(56,42)$
	- $56 \mod 42 \equiv 14$
- $ggT(42,14)$
	- $42 \mod 14 \equiv 0$
- somit folgt: $ggt(56,42)=14$