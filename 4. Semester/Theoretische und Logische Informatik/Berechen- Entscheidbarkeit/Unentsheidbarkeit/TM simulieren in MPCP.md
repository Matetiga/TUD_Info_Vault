## Schritte: 
- Das Lösungswort soll wie folgt beginnen: $\#c0\#c1\#c2\#\dots$, wobei $c_{i}$ Konfigurationen kodieren
1. Wir beginnen mit: 
$$
\begin{bmatrix} 
\# \\
\# c_{0} \#
\end{bmatrix}
$$
	also, das obere Wort liegt eine Konfiguration zurück.
2. Wir definieren die Wortpaare so, dass man oben eine Kopie der unteren Konfiguration nur dann erzeugen kann, wenn man gleichzeitig unten die Nachfolgerkonfiguration anfügt.
---

## Regeln 
![[Pasted image 20250425112843.png]]

1. TM geht vom Zustand **q** Zustand **p**, und wandelt das **a** in einem **b**. Und bewegt sich nach Rechts (deswegen steht das **b** links vom Zustand **q**)
2. TM geht vom Zustand **q** Zustand **p**,  und wandelt das **a** in einem **b**. Und bewegt sich nach Links (deswegen steht links vom **c**)
3. TM geht vom Zustand **q** Zustand **p**, und wandelt das **a** in einem **b**. Und bewegt sich nicht 

### Randfälle 
![[Pasted image 20250425113226.png]]


### Kopieregel
- Kopierregeln erlauben uns, den Rest der TM-Konfiguration (die Teile, die nicht nah am
Lese-/Schreibkopf liegen) vom unteren zum oberen Wort zu kopieren

$$
\begin{bmatrix}
x \\
x
\end{bmatrix}
\text{ :für jedes Symbol } x \in \Gamma \cup \{ \# \}
$$
### Startregel
$$
\begin{bmatrix}
\#  \\
\# q_{0}w \#
\end{bmatrix}
\text{ :wobei } q_{0} \text{ der Zustand und } w \in \Sigma^{*} \text{ das Eingabewort ist}
$$

### Schwarzes Loch
Angefangen von der Startregel zwingen uns die Regeln,
Konfigurationen zu kopieren und dabei entweder einen Berechnungsschritt
auszuführen, oder mehr Speicher am rechten Rand zu allozieren
![[Pasted image 20250425114938.png]]