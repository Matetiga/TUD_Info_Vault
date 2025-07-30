[[FE]]
[[FK]]
- mit Maximum Likelihood
- mit begrenzter Mindestdistanz

---

[[Fehlersyndrom]]
- Jede Codewort muss die folgende Bedingung erfüllen
- $H\cdot b^{T}=0$
- $b^{T}$ ein Codewort
- $H$ => [[Kontrollmatrix]] 

#### Falls Fehler erkannt wird:
$H\cdot b^{T} =s \neq 0$
- Dann ist $s$ **gleich wie einer Spalte im Kontrollmatrix**
- Die **Stelle der Spalte** <span style="color:#ffff00">zeigt</span> die **Stelle von** $b$ die man ändern muss
- <span style="color:#00ff04">Korrekte rekontruktion falls</span>=>
	- $b^{*}_{korr} = a^{*}$
![[WhatsApp Image 2024-07-18 at 19.47.59.jpeg]]

---
### Fehler Mit Sicherheit Erkennbar
$$
w(e)\leq d_{min}-1
$$
- $w(e)$ [[Hamming Gewicht]] von $e$
### Fehler mit Sicherheit Korrigierbar
$$
w(e)\leq \lfloor \frac{d_{min}-1}{2} \rfloor 
$$
