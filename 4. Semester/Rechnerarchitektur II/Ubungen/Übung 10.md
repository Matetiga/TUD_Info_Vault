## 10.0 Wiederholung Netzwerk
### 10.0.1 Binärbaum
![[Pasted image 20250628133946.png]]

Bestimmung des durchschnittlichen Knotenabstand:
- Jedes Blatt hat daselbe Muster von Pfade
- Pro Knote, die Anzahl an mögliche Pfade bestimmen, die man mit **genau** *n* Sprungen erreichen kann (*auch rückwärts*)
	- Vom Würzelknoten : $\frac{1\cdot 2 + 2\cdot 4 + 3 \cdot 8}{14\cdot 1}$
	- 2. Ebene : $\frac{1\cdot 3 +2 \cdot 5 + 3\cdot 2 + 4 \cdot 4}{14\cdot 2}$
	- 3 Ebene : $\frac{ 1\cdot 3 + 2\cdot 2 + 3 \cdot 3 + 4\cdot 2 + 5\cdot 4 }{14\cdot_{4}}$
	- Blätter: $\frac{1\cdot 1 + 2 \cdot 2 + 3\cdot 2 + 4 \cdot 3 + 5\cdot 2+ 6\cdot 4}{14\cdot 8}$
	- Die Summe alle Brüche gibt : $3.5$
## 10.1 MIMD
### 10.1.1 Klassifizierung nach Flynn
![[Pasted image 20250628141331.png]]

- Unterschied zwischen Cluster und MPP (*Massive Parallel Processing* ): 
	- In MPP Einzelne Komponente sind teil des gesamten Systems 
	- In einem Cluster sind 


### 10.1.2 UMA (1)
![[Pasted image 20250628141314.png]]

### 10.1.3 UMA (2)
busbasierte Mehrprozessorsysteme ohne Caching:
- Skalierbarkeit: Nein, da Von Neumann Bottleneck.
- Datenkohärenz: Ja, da nur ein Speicher

busbasierte Mehrprozessorsysteme mit Caching:
- Skalierbarkeit: Ja, solange Daten im Cache.
- Datenkohärenz: Nein, nur über zusätzliche Protokolle
![[Pasted image 20250628142559.png]]

### 10.1.4 NUMA
![[Pasted image 20250628144603.png]]

### 10.1.6 NCC-NUMA
![[Pasted image 20250628150115.png]]

### 10.1.7 COMA
![[Pasted image 20250628151449.png]]

### 10.1.8 MPP
![[Pasted image 20250628151636.png]]

### 10.1.9 Cluster
![[Pasted image 20250628152011.png]]


## 10.2 MESI
### 10.2.1 Voraussetzungen
![[Pasted image 20250628174254.png]]

### 10.2.2 Statusbits
- M : Modidfied 
- E : Exclusive
- S : Shared
- I : Invalid
![[Pasted image 20250628174502.png]]

### 10.2.3 Steuersignale
![[Pasted image 20250628175014.png]]
- **R** (*Retry*): Dieses Steuersignal wird verwendet, wenn modifizierte Cachelines in den Hauptspeicher zurüchgeschrieben werden müssen, bevor ein andere Prozessor diese dann wieder lesen möchte.
- **I** (*Invalidate*): Dieses Steuersignal wird gesendet, um eine Cacheline in anderen Speichern ungültig zu machen.
- **S** (*Shared*): Dieses Steuersignal wird verwendet, wenn ein Prozessor eine Leseoperation auf eine Cacheline ausführt, die bereits in einem anderem Speicher vorliegt.



### 10.2.4 Zustandsübergangsdiagramm
- **Probe Miss**: Kommt nach einer Read Miss Signal, wenn ein **kein anderes Prozessor** dieselbe address gelesen hat (*Exclusive Signal*)
- **Probe Hit** :  Kommt nach einer Read Miss Signal, wenn ein **anderes Prozessor** dieselbe address gelesen hat (*Shared Signal*)

**Retry Signal**: Wenn ein modifizierter Wert noch nicht im Hauptspeicher geschrieben wird, und *Snoop Read Hit*, wird ein Retry Signal zu den anderen geschickt, sodass sie warten bis der Wert geschireben wird

**Snoop** (Beobachtungen vom gemeinsamen Bus)
- **Read-Hit** Jemand anderes liest es vom Speicher, wir kennen die Cacheline
 - **Write-Hit** Jemand anderes will in den Speicher schreiben, wir kennen die Cacheline

>[!Important]
>Das unten rechts Zustand (S) und *Snoop Read Hit, Shared Signal* sollte eigentlich *Snoop Read Miss, Shared Signal*, da Hit würde bedeuten, dass die Cachezeile in einem anderen Prozessor liegt


![[Pasted image 20250702101257.png]]

### 10.2.5 Zustandsübergänge (1)
>[!Important]
>Um die Aufgabe zu lösen, muss man die Instruktion aus der Sicht jedes Prozessors sehen
>Dann kann man aus dem Zustand, in dem jeden Prozessor sich befindet, die mögliche Zustandsänderungen betrachten 

- In der dritten Übergang geht Prozessor 1, Prozessor 2, Prozessor 3 (S,S,I) zu (S, S, I) noch mal, da (ncah Zustandstabelle) beide Prozessoren machen **Read Hit**
![[Pasted image 20250702115057.png]]


### 10.2.7 Zustandsübergänge (3)
- Prozessor 1: macht **Write Miss** (*von I nach M*)
- Prozessor 2: macht **Snoop Write Hit** (*von E nach I*)
![[Pasted image 20250702115717.png]]


