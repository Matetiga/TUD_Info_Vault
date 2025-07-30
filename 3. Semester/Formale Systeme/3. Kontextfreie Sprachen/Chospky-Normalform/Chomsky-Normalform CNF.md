
Eine kontextfreie Grammatik $G = ⟨V, Σ, P, S⟩$ ist in **Chomsky-Normalform (CNF)**, wenn alle ihre Produktionsregeln eine der beiden folgenden Formen haben: 
- $A\to BC$ mit $\forall B,C \in V$
- $A\to c$ mit $c \in \Sigma$

---

### Wichtig 
- Grammatiken, deren Sprache **das leere Wort enthalten**, können **nicht in CNF sein**
- Aber wie wir wissen, gibt es in [[ϵ-freier CFGs]] ohnehin höchstens eine Regel $S\to\epsilon$

