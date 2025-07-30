## Theta Join
Auswahl bestimmter Tupel aus dem kartesischen Produkt 
$𝑅 \Join_{𝑖𝛩𝑗} 𝑆 ≔ 𝜎_{𝐴𝑖Θ𝐵𝑗} (𝑅 × 𝑆)$

---
## Equi Join
$R \Join_{A = E} S$ 
- Dies wird alle Zeilen geben, wo die Spalte A gleich B ist 

--- 

## Natürliches Bund 
Voraussetzung : $A_{1} = B_{1}, ..., A_{k} = B_{k}$ und $A_{j} \neq B_{i}$ für alle j und i mit $k < j \leq r$ und $k < i \leq s$
**Definiert  als :** 
$𝑅 \Join 𝑆 ≔ 𝜋_{𝑖-_{𝑘+1},𝑖_{𝑘+2},….,𝑖_{𝑟+𝑠}} (𝜎_{𝑅.𝐴1=𝑆.𝐵1∧...∧𝑅.𝐴𝑘=𝑆.𝐵𝑘}(𝑅 × 𝑆))$
- Gibt es kein gemeinsames Attribut, so ist das **Ergebnis das kartesische Produkt**
	- Relationen nur ein gemeinsames Attribut
![[Pasted image 20250512102104.png]]

