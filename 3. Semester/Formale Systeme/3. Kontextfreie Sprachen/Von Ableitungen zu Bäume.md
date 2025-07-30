Sei $G = ⟨V, Σ, P, S⟩$ eine Grammatik und sei $S = w_{0} ⇒ w_{1} ⇒ . . . ⇒ w_{n}$ eine Ableitung
(mit $w_{i} ∈ (V ∪ Σ)^{*}$ für alle $i ∈ {1, . . . , n})$

## Ableitungsbaum Konstruktion 
Wir erhalten den entsprechenden Ableitungsbaum wie folgt:
-  Der Ableitungsbaum wird initialisiert mit einem einzigen **Wurzelknoten S**.
-  Der Baum wird schrittweise konstruiert. Nach $i$ Schritten ergeben die Blätter des Baumes – *gelesen von links nach rechts* – immer genau $w_{i}$.
-  Wenn in einem Ableitungsschritt $w_{i} ⇒ w_{i}+1$ die Regel $V → u$ angewendet wurde, dann erhält der Knoten für $V$ genau $|u|$ Kindknoten, die – von links nach rechts – mit den Symbolen aus u beschriftet werden
 
![[Screenshot from 2024-11-30 13-55-55.png]]