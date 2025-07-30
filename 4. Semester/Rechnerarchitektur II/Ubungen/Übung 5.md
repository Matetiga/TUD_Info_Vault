## 05.0.1 Energiemodelle (Vorlesung 3)
- *Für die Tabelle:* 
	- Es braucht die Werte für die Leistungsaufnahme, wenn 1,...,4  Kerne aktiv sind
	- Falls ein Kern inaktiv ist, dann ist die Leistungsaufnahme (für C6) das Differenz zwischen die Leistungsaufnahme für C3 und $1.2 \cdot \text{Anzahl Kerne}$

*Leistungsaufnahme von Teilen des Prozessors*
- $33.6-(1.2*4+6.9+6.9)$
	- $33.6$ : aus 2 aktive und 2 passive Kerne
		- passive Kerne brauchen $1.2W$
		- aktive Kerne brauchen auch $1.2W$ und $6.9W$ (da es sich in **C0**)

![[Pasted image 20250514093353.png]]

## 05.0.2 Leistungsaufnahme mit steigender Frequenz

$$
\begin{gather}
P_{total} = P_{dyn} + P_{static}\\
31,76W = P_{dyn} +20W\\
P_{dyn} =11,76W
\end{gather}
$$
$$
\begin{gather}
P_{dyn}=\gamma \cdot f \cdot V^{2}\\
11.76 VA = \gamma \cdot 1.2 \cdot 10^{9} \frac{1}{s} \cdot 1.1^{2}V^{2}\\
\gamma = 8.1\cdot 10^{-9} \frac{As}{V}
\end{gather}
$$

$$
\begin{gather}
8.1*10^{-9}*1.6*10^{9}*1.2^{2}+21.82
\end{gather}
$$


---
## 05.3.4 Problemlösung
- *Hardware Multithreading*
	- da die Reorder Buffer eine bestimmte Speicher hat und wenn mehrere Threads es nutzen, dann gibt es weniger Speicher pro Thread. Somit ist wahrscheinlicher, dass kein fehler gemacht wird (da : $0.96^{49}=13.5\%$ Wahrscheinlickeit)

---

## 05.5.1 Assoziativer Cache
Ihr Prozessor hat einen 512 KiB großen Cache, der 4 Wege satz-assoziativ ist. Die Cachezeilen sind 64 Byte lang. Es werden 512 GiB physischer Speicher unterstützt, was sich auf die physischen Adressen auswirkt. Auf Einträge im Cache wird über die physische Adresse zugegriffen (wichtig für Index und Tag

Da $512\text{KiB} \to \frac{512\cdot 1024}{64}=8192$ Cache Zeilen
**Byte select** : $ld(64)=6$
Da es 4 Wege satz-assoziativ ist : $\frac{8192}{4}=2^{11}$
- Also **Index** muss $11$ Bit lang sein
Für **Tag** : $ld(512 \cdot 2^{30})-11-6=22$
- Da : 512 GiByte physischer Speicher