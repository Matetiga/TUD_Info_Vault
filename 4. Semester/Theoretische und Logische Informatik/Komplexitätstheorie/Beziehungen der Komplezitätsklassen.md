![[Komplezitätsklassen#Komplezitätsklassen]]

---
## Beziehungen 
- $P \subsetneq \text{Exp}$
- $\text{LogSpace } \subsetneq \text{PSpace}$
- $\text{LogSpace } \subseteq \text{P} \subseteq \text{PSpace} \subseteq \text{Exp}$
- $\text{NTime(f)} \subseteq \text{NSpace(f)} \subseteq \text{DTime}(2^{O(f)})$
- **Nicht bekannt ob** : $\text{NTime}(g) \subseteq \text{DTime}(g)$
- Da $\text{DTM} \subseteq \text{NTM}$ folgt: 
	- $\text{L} \subseteq \text{NL}$
		- $\text{P} \subseteq \text{NP} \subseteq \text{PSpace}$
	- $\text{PSpace} \subseteq \text{NPSpace}$
	- $\text{Exp} \subseteq \text{NExp}$
- Da $\text{Zeit} \subseteq \text{Speicher}$ folgt:
	- $\text{P} \subseteq \text{PSpace}$
	- $\text{NP} \subseteq \text{NPSpace}$
- Da $(N)\text{Speicher} \subseteq 2^{D(\text{Zeit})}$
	- $\text{NL} \subseteq \text{P}$
	- $\text{NPSpace} \subseteq \text{Exp}$
- $\text{NL} \subsetneq \text{PSpace}$
- $\text{ NL } \subseteq \text{DSpace}(\log^{2}n)$
- $\text{P} \subsetneq \text{Exp}$
- $P \subseteq \text{coNP} \cap \text{NP}$
- $\text{NP} \subsetneq \text{NExp}$
- $\text{ NPSpace } = \text{coNPSpace}$
- $\text{ExpTime } \subseteq \text{NExpTime} \subseteq \text{ExpSpace}$
### Wichtige Beziehungen 
#### Satz Immerman
- $\text{NL} = \text{coNL}$

#### Satz von Savich
- $\text{PSpace} = \text{NPSpace}$
	- $\text{ NPSpace } = \text{coNPSpace}$
#### Zusammengefasste Beziehungen
$$
L ⊆ NL ⊆ P ⊆ NP ⊆ PSpace = NPSpace ⊆ Exp ⊆ NExp
$$
---
### Beispiele 
- Eulers Methode um die Existenz von Eulerpfaden zu entscheiden, kann in *LogSpace* implementiert werden: Wir zählen die Kanten jedes Knotens und speichern  die Zahl der Knoten ungeraden Grades, jeweils binär

- Die Suche nach Hamilton-Pfaden ist in *ExpTime*, aber auch in *PSpace*
