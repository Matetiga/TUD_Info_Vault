### Entsteht aus der (transponierten) Redundanten Spalten der Generator matrix
- erlaubt Kodierung
- Fehler Erkennung
- Fehlerkorrektur

## $H_{k \times n}$
- [[Kontrollgleichungen]]
- [[Generatormatrix]]
	- $H=[C^{T}I_{k}]$
	- $G_{l \times n} \to H_{k \times n}$

- die Redundanten Spalten der Kontrolmatrix bilden eine Einheitsmatrix 
- wenn man $a^{*}_{i}$ bekommt, dann muss man die Kontrollstellen hinzufügen

![[WhatsApp Image 2024-06-11 at 16.24.58.jpeg]]

---
## Bestimmungsgleichungen Für Kontrollstellen
#### Wie bestimmt man die Summanden für $k_{1}, k_{2}, k_{3}$?
- Jede **Kontrollspalte** hat nur eine "1" (der Rest ist $0$, da es Teil des Einheitsmatrix ist)
- Man **vergleicht** mit den anderen **informationsstellen der selben Zeile**, und alle die *auch 1 an der Stelle* haben, werden genommen 
### Beispiel
$$
H_{k \times n}=
\begin{pmatrix} 
l_{4}&l_{3}&l_{2}&l_{1}&k_{3}&k_{2}&k_{1}\\
1 & 1 & 1 & 0 & 1& 0&0 \\
1&1&0&1&0&1&0 \\
1&0&1&1&0&0&1 \\
\end{pmatrix}
$$
- nach [[Paritätsbits]] *k* -> muss gelten:
	- $l_{4}+l_{3}+l_{2}+k_{3}=0$
	- somit folgt: 
		- $l_{4}+l_{3}+l_{2}=k_{3}$        da wir in $\text{GF}(2)$ sind

$$
\begin{gather}
k_{3}=l_{4}+l_{3}+l_{2}\\
k_{2}=l_{4}+l_{3}+l_{1}\\
k_{1}=l_{4}+l_{2}+l_{1}
\end{gather}
$$


