## Stromsparstrategien
#### Power Gating
- $V_{DD}:$ *Versorgerungsspannung* auf 0 setzen 
- Gespeicherte Inhalte des abgeschalteten Prozessorteils gehen verloren

#### Clock Gating 
- Verkleinerung des Faktors $\alpha$ (bei [[#Dynamische Leistungsaufnahme]])
- Gespeicherte Inhalte des abgeschalteten Prozessorteils bleiben bestehen
- Abschalten der Frequenz für einen bestimmten Teil des Prozessors

#### Dynamic Voltage and Frequency scaling 
- Skalierung der Frequenz (die Spannung kann entsprechend auch skaliert werden)
- Senkt statische und dynamische Leistungsaufnahme 
- Zusätzliche Hardware dafür 
---
## Insgesamt Leistungsaufnahme Formel
$$
P_{total}=P_{dynamic} + P_{static}
$$

### Statische Leistungsaufnahme
- $V_{DD}:$ Versorgerungsspannung
- $\beta = I_{sub}+ I_{gate}+I_{junct}+ I_{contention}$
$$
P_{static}=\beta \cdot V_{DD}
$$

### Dynamische Leistungsaufnahme
- $f$ : Frequenz
- $C$ : Kapazität
$$
P_{dynamic}=\alpha \cdot C \cdot V_{DD}^{2} \cdot f + \epsilon
$$