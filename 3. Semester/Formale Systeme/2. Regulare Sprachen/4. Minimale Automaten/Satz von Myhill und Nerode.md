**Wenn L regulär ([[Reguläre Sprachen]]) ist, dann hat $≃_{L}$ endlich viele [[~Äquivalenzklassen]]**
- wenn es unendlich viele Äquivalenzklassen hat, dann ist es **nicht regulär** 
---

Der [[1. deterministische Endliche Automaten DFA]] $M_{L}= \langle Q, \Sigma, \delta, q_{0}, F \rangle$ ist wie gefolgt definiert:
- $Q=\{ [w]_{\simeq} |w \in \Sigma^{*}\}$ ist die (endliche) Menge der ≃Äquivalenzklassen
- $q_{0}=[\epsilon]_{\simeq}$
- $F=\{ [w]_{\simeq} |w \in L\}$
- $\delta([w]_{\simeq},a)=[wa]_{\simeq}$

-  [[1. deterministische Endliche Automaten DFA]] **mit [[totaler Übergangsfunktion]]**
![[Screenshot from 2024-11-21 14-28-31.png]]

## $M_{L}$ Eigenschaften 
-  $M_{L}$ ist Minimal
- $M_{L}$ ist ein [[1. deterministische Endliche Automaten DFA]]
-  $L(M_{L})=L$
- Jedes Zustand von $M_{L}$ ist vom Startzustand aus erreichbar, da: $\delta([\epsilon]_{\simeq}), w=[w]_{\simeq}$
- $\simeq_{M_{L}}=\simeq_{L}$
- $M_{L}$ ist isomorph zu jedem reduzierten Automaten für $L$
