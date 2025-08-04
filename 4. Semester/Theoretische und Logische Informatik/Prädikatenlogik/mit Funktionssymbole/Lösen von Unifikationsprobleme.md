Dadurch kann man finden, ob für die *Unifikationsproblem* G ein [[Unifikator#Allgemeinste Unifikator|Allgemeinste Unifikator]] gibt 

## Umformungsregeln 
### Löschen 
- $\{  t \doteq t \} \cup G \to G'$
- ein Term ist gleich zu sich selbst 
### Zerlegung 
- $\{ f (s_{1},\dots , s_{n}) \doteq f (u_{1}, \dots , u_{n})\} \cup G' \to \{ s_{1} \doteq u_{1}, \dots, s_{n} \doteq u_{n} \} ∪ G'$
- Eine Gleichung (auf Parameter $s_{1},\dots ,s_{n}$, $u_{1},\dots ,u_{n}$)
- dann fügt man $n$ Gelichungen mit $s_{1} \doteq u_{1} \text{ bis } $
### Orientierung 
- $\{  t \doteq x \} \cup G' \to \{  x \doteq t \} \cup G'$ falls $x \in V \text{ und } t \not \in V$ 
- Dies folgt nur unter dieser Bedingung da $\doteq$ nicht symmetrisch ist (in gegenstatz zu $=$)

### Eliminierung
- $\{  t \doteq x \} \cup G' \to \{  x \doteq t \} \cup G' \{  x\mapsto t \}$ falls $x \in V$ nicht in $t$ vorkommt

Wenn G danach in [[Gelöste Unifikatorproblem|Gelöste Form]] ist, dann gib $\sigma G$ aus 
- Andernfalls gib aus „nicht unifizierbar"

---
## Beispiel
![[Pasted image 20250625120127.png]]

---

## Korrektheit des Unifikationsproblem
![[Pasted image 20250625122112.png]]

Für $G_{1}$ und $G_{2}$ mit $κ(G_{i}) = ⟨v_{i}, g_{i}, r_{i}⟩$ gilt $G_{1} \succ G_{2}$ gdw.
- $v_{1} > v_{2}$, oder
- $v_{1} = v_{2}$ und $g_{1} > g_{2}$, oder
- $v_{1} = v_{2}$ und $g_{1} = g_{2}$ und $r_{1} > r_{2}$

### Beispiel 
$\langle 4,2,1 \rangle \succ \langle 3,42,23 \rangle \succ \langle  3,42,22 \rangle \succ \langle 3,41,1000 \rangle$
![[Pasted image 20250625123440.png]]