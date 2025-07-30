Sei $(S; \circ)$ eine Permutationsgruppe auf der endlichen Menge $X$
$S_{x}:= \{  \alpha|\alpha \in S, \alpha(x)=x \}$ heißt Stabillisator von $x$ in $S$

- $x \in X$
- $S_{x} \subseteq S$
##### Beispiel
Alle $x_{0} \in S$ die $x_{1} \in S$ unebewegt lassen, z.B.:
- mit : $\{ {id,(12),(13),(23),(123),(132)} \}$
- Stabilisator: $S_{1}=\{ id,(23) \}$ **die zwei Permutationen bewegen** $1$ **nicht**
 
---
#### Stabilisator ist eine [[Untergruppe]] von $(S; \circ)$ da:
- $S_{x} \subseteq S$
- $id \ \in S_{x}$
- Abgeschlossenheit bzgl. $\circ$
- Abgeschlossenheit bzgl. der Inversenbildung
---

### Stabilisator von $S_{x}$ von $x$ in $S$ bestimmt eine [[Äquivalenzrelationen]] $R_{S_{X}}$ in S

### [[Äquivalenzklassen]] von $R_{S_{X}}$ in S sind:
- $[\alpha]_{R_{S_{X}}}=\alpha \circ S_{x}=\{ \alpha \circ \sigma_{x} | \sigma_{x} \in S_{x} \}$

### Faktormenge von $S$ nach $R_{S_{X}}$ ist:
	${G}/{{R_{S_{X}}= \{ [\alpha]_{R_{S_{X}}} | \alpha \in S\}}}= \{  \alpha \circ S_{x} |\alpha \in S\}$
- mit $\alpha \circ S_{x}$ ist die Menge aller Elemente aus $S$ die $x$ auf $\alpha(x)$ abbilden
	- $\alpha \circ S_{x}=\{ \alpha \circ \sigma_{x} |\sigma_{x} \in S_{x} \}= \{  \sigma \in S | \sigma(x)=\alpha(x) \}$
