Jedes [[1. deterministische Endliche Automaten DFA]] hat endlich viele Zustände 
- Manche [[Reguläre Sprachen]] enthalten beliebig lange Wörter
-  Dann muss der DFA beim Einlesen ==einen== Zustand **mehr als einmal besuchen.**
	- also eine **Schleife** 

![[Screenshot from 2024-11-25 11-42-23.png]]

## Für Endliche Sprachen 
Für endliche Sprachen ist die Eigenschaft trivial.
Man wählt n einfach so groß, dass es keine Wörter $z \text{ mit } |z| ≥ n$ gibt, für welche weitere Eigenschaften gefordert werden

### Beispiel
Die Sprache von $b^{*}(ab^{*}ab^{*})^{*}$ (Wörter mit gerader Anzahl **a**$s$). Der Parameter
$n$ aus dem Pumping-Lemma kann 2 sein:
- Wenn z die Form **b**$y$ hat, wähle $u = ϵ, v = b$ und $w = y$.
-  Wenn z die Form **ab**$y$ hat, wähle $u = a, v = b$ und $w = y$.
-  Wenn z die Form **aa**$y$ hat, wähle $u = ϵ, v = aa$ und $w = y$.