# Deterministisch 
## Zeit beschränkt 
$\mathcal{O}(f)$-*zeitbeschränkt*, wenn es eine Funktion $g ∈ \mathcal{O}( f )$ gibt,
sodass für alle $w ∈ Σ^{*} \text{ gilt }: M$ hält auf Eingabe $w$ nach maximal $g(|w|)$ Schritten

### DTIME(f(n))
- deterministische Time 
	- Klasse aller Sprachen $L$ die durch eine $\mathcal{O}(f)$-*zeitbeschränkte* Turing-Maschine entscheiden werden kann 

>[!Important]
>Die Anzahl der Bänder hat lediglich einen polynomiellen (quadratischen) Einfluss auf die Probleme, die eine zeitbeschränkte TM lösen kann


---
## Raum beschränkt
$\mathcal{O}(f)$-*speicherbeschränkt*, wenn es eine Funktion $g ∈ \mathcal{O}( f )$
gibt, sodass für alle $w ∈ Σ^{*}$ gilt:
- $M$ hält auf Eingabe $w$ und verwendet dabei maximal $g(|w|)$ **Speicherzellen**

### DSPACE(f(n))
- deterministische Raum 
	- Klasse aller Sprachen $L$ die durch eine $\mathcal{O}(f)$-*speicherbeschränkte* Turing-Maschine entscheiden werden kann 


>[!Important]
>Das Halteproblem ist in keiner der Klassen DTIME oder DSPACE rein, da es kein TM gibt, die es entscheiden kann 
>- Die Anzahl der Bänder hat *keinen Einfluss* auf die Probleme, die eine speicherbeschränkte TM lösen kann


---

# Nicht Deterministisch 
### DTIME(f(n))
- nicht deterministische Time 
	- Klasse aller Sprachen $L$ die durch eine $\mathcal{O}(f)$-*zeitbeschränkte* [[Nichtdeterministische TM]] entscheiden werden kann 

### DSPACE(f(n))
- nicht deterministische Raum 
	- Klasse aller Sprachen $L$ die durch eine $\mathcal{O}(f)$-*speicherbeschränkte* [[Nichtdeterministische TM]] entscheiden werden kann 


---

# Beziehungen 
Für jede beliebige Funktion $f: \mathbb{N}\to \mathbb{R}$ gilt :
- (der Konfigurationsgraph ist exponentiell groß aber kann **deterministisch durchgesucht** werden)
### 1. DTime und DSpacce
$$
\text{DTIME}(f) \subseteq \text{DSPACE}(f)
$$
- **Beweis**: Die TM benötigt immer mindestens einen Schritt, um eine zusätzliche Speicherstelle zu beschreiben

### 2. DSpace und DTime
Speicher ist mächtiger als Zeit, da man es mehrfach verwenden kann 
- $\text{DTIME}2^{O(f)}$ umfasst alle Probleme die von einem [[Deterministische Turingmaschine|DTM]] in beschränkte Zeit gelöst werden können, die **asymtotisch** durch $2^{O(f)}$ **beschränkt sind** 
$$
\text{DSPACE}(f) \subseteq \text{DTIME}(2^{O(f)})
$$
### 3. NTime und NSpace
$$
\text{NTIME}(f) \subseteq \text{NSPACE}(f)
$$

### 4. NSpace und DTime
$$
\text{NSPACE}(f) \subseteq \text{DTIME}(2^{O(f)})
$$
