## Definition
Die Menge von FDs $F_{c}$ wird als kanonische Überdeckung von F bezeichnet, falls folgende Bedingungen erfüllt sind:
 - $F_{c}^{+}=F^{+}$
 - Für alle $\text{FDs } A→B \text{ in } F_{c}$ gibt es **keine überflüssigen** Attribute in A und in B, also 
	 - jede linke Seite der FDs in $F_{c}$ kommt nur einmal vor, d. h. falls $A→B$ und $A→C$, dann wird in $F_{c}$ nur die FD $A→B\cup C$ verwendet
### Überflüssige Attribute durch Links-/ Rechtsreduktion entfernen
- Man löscht ein Attribut von der linken/rechten Seite 
![[Pasted image 20250602141439.png]]

### Beispiel
Menge $F = \{A→B, B→C, A\cup B→C \}$
1. **Linksreduktion** :
	- $C\subseteq Hülle(F, {A\cup B}-{A}) = Hülle(F, B)$? (also man löscht A in $A \cup B \to C$) dann folgt: $F = \{A→B, B→C,B→C \}$
2. **Rechtsreduktion**: 
	- Man fängt mit der ersten Funktionale Abhängikeit
	- Ist B in $A \to B$  löschbar?
		- $B \subseteq Hülle({A→ \emptyset , B→C, B→C},A)$? **Also nein**, da $A \to \emptyset$, somit entählt die Hülle B nicht
	- Ist C in $B\to C$ löschbar?
		- $C \subseteq Hülle({A→ B , B→ \emptyset, B→C},B)$? **Ja**
	-  Ist C in (das andere) $B\to C$ löschbar?
		- $C \subseteq Hülle({A→ B , B→ \emptyset, B→ \emptyset},B)$? **Nein**
3. $B→ \emptyset \text{  wird entfernt, bleibt }{A→B, B→C}$
4. Zusammenfassung nicht möglich 

**Statt A im ersten Schritt zu löschen, wird B gelöscht**
- dies zeigt, dass die Reihenfolge vom Attribut Löschen zu selber Lösung führen
![[Pasted image 20250602150203.png]]