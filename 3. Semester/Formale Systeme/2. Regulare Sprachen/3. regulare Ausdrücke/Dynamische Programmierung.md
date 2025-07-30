![[Screenshot from 2024-11-18 14-27-20.png]]

## Fall k = n
- $L^{n}[i,j]$ ist die Menge aller Wörter zwischen $q_{i}$ und $q_{j}$
- $\alpha^{n}[i,j]=\alpha_{q_{i},q_{j}}$ sind die [[Regulare Ausdrücke]], aus denen wir letztlich die Lösung ermitteln wollen

## Fall k = 0
- dann ist $p_{i}$ eine leere Menge
- $L^{0}[i,j]$ beruht nur auf Läufe ohne Zwischenzuständen
	- Falls $i \neq j$ dann kommen nur Läufe $q_{i}\to ^{a}q_{j}$ in frage
	- Falls $i = j$ dann kommen nur Läufe $q_{i}\to ^{a}q_{i}$ oder $q_{i}(w=\epsilon)$ in frage
- [[Regulare Ausdrücke]] *können* aus **M abgelesen werden**

---

### Teilläufe
Für $\alpha^{k+1}[i,j]$:
- $q_{i}\to q_{k+1} \quad (q_{k+1}\to q_{k+1})^{*} q_{k+1}\to q_{j}$
![[Screenshot from 2024-11-18 14-42-56.png]]

## Beispiele
- Wenn man k erhöht, dann fügt man Zustände hinzu. Somit für $k=2$, **darf man Zustand 2** (*mehrmals*) benutzen 
![[Screenshot from 2024-11-18 18-12-47.png]]![[Screenshot from 2024-11-18 18-12-51.png]]![[Screenshot from 2024-11-18 18-15-01.png]]