## 09.1 Unterscheidung
### 09.1.1 Statische Netze
Verbindungsnetzwerke (VN) ermöglichen den Transport von Informationen zwischen den einzelnen Hardwarekomponenten.

- Modulare Strukturen werden bevorzugt, da das Netz keine Möglichkeiten zur Rekonfiguration bietet
- Jeder Knoten besitzt eine bestimmte Anzahl fester Leitungen zu den benachbarten Knoten
- Vermittlungsfunktionen sind kein Bestandteil von statischen Verbindungsnetzwerken
- Das Netzwerk selbst beschränkt sich auf Verbindungsleitungen Vermittlungsfunktionen werden nicht ausgeführt


### 09.1.2 Dynamische Netze
- Verbindungen werden durch **aktive** Koppelelemente innerhalb des *Verbindungsnetzwerks realisiert*
- Vermittlungsfunktionen werden durch diese Koppelelemente **eigenständig** ausgeführt
- Bei mehrstufigen Netzen ist die Verdrahtung zwischen den Schaltstufen oft nicht über das gesamte Netz einheitlich


## 09.2 Kennwerte Statischer Verbindungsnetzwerke
### 09.2.1 Zuordnung

![[Pasted image 20250623160006.png]]


### 09.2.2 Beispielaufgabe
- **Grad d** := Anzahl der Kanten (bzw. Links) pro Knoten
- **Durchmesser k** := Maximaler Abstand zwischen 2 Knoten in Linkverbindungen
                               Maximum über alle kürzesten Pfade zwischen zwei Knoten
- **Halbierungsbreite** := Minimale Kantenausfallzahl für den Zerfall des Netzes in zwei gleichgroße Teile
![[Pasted image 20250623160737.png]]



### 09.2.3 Ziele
![[Pasted image 20250623161339.png]]
![[Pasted image 20250623161321.png]]

### 09.2.4 Ring
|                   | Ring                                                                         |
| ----------------- | ---------------------------------------------------------------------------- |
| Grad              | 2                                                                            |
| Durchmesser       | $\left\lfloor  \frac{N}{2}  \right\rfloor$                                   |
| m.Knotenabstand   | falls N gerade: $\frac{N+1}{4}$ , falls N unegerade : $\frac{N^{2}}{4(N-1)}$ |
| Halbierungsbreite | 2                                                                            |
| Erweiterung       | 1                                                                            |
| Konektivität      | 2                                                                            |

### 09.2.5 Vollständiger Graph

|                   | Vollständiger Graph                                                              |
| ----------------- | -------------------------------------------------------------------------------- |
| Grad              | N-1                                                                              |
| Durchmesser       | 1                                                                                |
| m.Knotenabstand   | $\left\lfloor  \frac{N}{2}  \right\rfloor\left\lceil   \frac{N}{2} \right\rceil$ |
| Halbierungsbreite | 2                                                                                |
| Erweiterung       | 1                                                                                |
| Konektivität      | N-1                                                                              |

### 09.2.6 Stern

|                   | Stern                                                 |
| ----------------- | ----------------------------------------------------- |
| Grad              | N-1, 1                                                |
| Durchmesser       | 2                                                     |
| m.Knotenabstand   | $\frac{1\cdot (N-1)+(N-1)(N-2)\cdot 2}{N\cdot (N-1)}$ |
| Halbierungsbreite | $\lfloor \frac{N-1}{2} \rfloor$                       |
| Erweiterung       | 1                                                     |
| Konektivität      | 1                                                     |

### 09.2.7 Vollständiger Binärbaum

|                   | Vollständiger Binärbaum |
| ----------------- | ----------------------- |
| Grad              | 1,2,3                   |
| Durchmesser       | $(ld(N-1)-1)\cdot 2$    |
| m.Knotenabstand   |                         |
| Halbierungsbreite | 1                       |
| Erweiterung       | N+1                     |
| Konektivität      | 1                       |
### 09.2.8 Quadratischer 2D-Torus

|                   | Quadratischer 2D-Torus                                                         |
| ----------------- | ------------------------------------------------------------------------------ |
| Grad              | 4                                                                              |
| Durchmesser       | $2\cdot \left\lfloor  \frac{\sqrt{ N }}{2}  \right\rfloor$                     |
| m.Knotenabstand   |                                                                                |
| Halbierungsbreite | Falls N Gerade: $2 \cdot \sqrt{ N }$, Falls N ungerade: $2 \cdot \sqrt{ N }+2$ |
| Erweiterung       | $2 \cdot \sqrt{ N }+1$                                                         |
| Konektivität      | 4                                                                              |

### 09.2.9 Hypercube

|                   | Hypercube     |
| ----------------- | ------------- |
| Grad              | $ld(N)$       |
| Durchmesser       | $ld(N)$       |
| m.Knotenabstand   |               |
| Halbierungsbreite | $\frac{N}{2}$ |
| Erweiterung       | N             |
| Konektivität      | $ld(N)$       |


## 09.3 OMEGA-Netz
### 09.3.1 Klassifizierung
Bei einem OMEGA-Netzwerk handelt es sich um ein (**Dynamisches**) Netzwerk, genauer um ein(en) **(zellenbasiertes Netz)** . Ein OMEGA-Netz mit 4 Stufen hat  **(16)** Ein- bzw. Ausgänge


### 09.3.2 Destination Routing
*In destination-tag routing, switch settings are determined solely by the message destination. The most significant bit of the destination address is used to select the output of the switch in the first stage; if the most **significant bit is 0, the upper output is selected, and if it is 1, the lower output is selected**. The next-most significant bit of the destination address is used to select the output of the switch in the next stage, and so on until the final output has been selected.*

Beim Destination Routing hängt unsere Pfadwahl nur vom Ziel ab. Wir können als Schaltstellung direkt die Binärcodierung des Ziels nutzen.

Diese Routing ermöglich **nur anhand der Zieladresse** eine feste Route zu finden, ohne Routingtabellen oder ähnliches

### 09.3.3 XOR Routing
Source und Destination Bits sind zusammen mit XOR-Operation gestellt
- 0 : geht straight 
- 1 : crossed 
For example, if PE 001 wishes to send a message to PE 010, the XOR-tag will be 011 and the appropriate switch settings are: A2 straight, B3 crossed, C2 crossed

### 09.3.4 Blockierung
*Nun schreiben wir für die drei Beispiele die Quell- und Zieladresse in binärer Repräsentation hintereinander  (E1,A6 wird zu 00010110) und untereinander auf. Finden Sie die Stellen, an denen bei den jeweils 2 Schaltungen 4 gleiche Bits haben (z.B. 0110 im ersten Beispiel sind 4 gleiche Bits, die an der vierten Stelle beginnen). Fällt Ihnen bezüglich dieser Stelle(n) etwas auf?*

Für $E_{1}$ nach $A_{6}$ und $E_{14}$ nach $A_{6}$
- 0001**0110**
- 1110**0110**
Letzte 4 Bits sind gleich (Kollision in der vierten Stufe)

Für $E_{1}$ nach $A_{11}$ und $E_{1}$ nach $A_{9}$
- 00**0110**11
- 11**0110**01
Kollision in der zweiten Stufe

Für $E_{1}$ nach $A_{6}$ und $E_{13}$ nach $A_{1}$
- 00010110
- 11010001
Keine Kollision 

## 09.4 Paketvermittlung

### 09.4.1 Pakete
![[Pasted image 20250626110341.png]]
### 09.4.2 Prinzipien
![[Pasted image 20250625104640.png]]