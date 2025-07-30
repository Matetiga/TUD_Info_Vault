## 11.1 Zuverlässigkeit
### 11.1.2 Festplatten
- $$\text{Failure}_{ges}=\sum_{c \in Komponent}\frac{1}{MTTF}_{c}$$

$$
\frac{1}{\left( \frac{5}{(1.5 \cdot 10^{6})}+ \frac{1}{750000}+ \frac{1}{1.5 \cdot 10^{6}}+ \frac{1}{250 000}  + \frac{2}{500000} \right)}
$$

### 11.1.3 Redundante Netzteile
*Nehmen Sie an, Sie möchten einen Server an einem einzelnen Stromkreis betreiben. Zur Wahl steht ein Modell mit zwei redundanten Netzteilen mit einer MTTF von 100.000 Stunden je Netzteil. Der Anbieter des Servers garantiert die Lieferung von Ersatznetzteilen so, dass diese innerhalb von 48 Stunden getauscht werden können.*  
*Ein anderes Mod## 11.2.2 Benchmarks Iell wird mit lediglich einem Netzteil betrieben. Dieses hat eine MTTF von 200.000 Stunden. Bei diesem Server können Netzteile innerhalb von 1 Stunde getauscht werden*
$$
\frac{MTTF}{MTTF+MTTR}
$$
- **M**ean **T**ime **T**o **F**ail
- **M**ean **T**ime **T**o **R**epair

Server mit zwei Netzteilen:
- $1-\frac{100000}{100048}=0.0005$
- $0.0005^{2}=0.00000025$
- $1-0.00000025=0.99999975$
Server mit nur einem Netzteil
- $\frac{200000}{200001}$


## 11.2 Leistungsbewertung
### 11.2.1 Einführung
Wenn ein Prozessor doppelt so schnell taktet ist ein Programm in der halben Laufzeit abgearbeitet. (idealisiert)
Dabei gibt es die reine CPU Zeit, wo gezählt wird wie lange der Prozess auf der CPU arbeitet und die Gesamtzeit die ein Programm braucht, mit möglichen Overheads
![[Pasted image 20250707135824.png]]

### 11.2.2 Benchmarks I
![[Pasted image 20250709095223.png]]

### 11.2.3 Benchmarks II
![[Pasted image 20250707143011.png]]

### 11.2.4 Benchmarks III
![[Pasted image 20250707143021.png]]


### 11.2.5 Wichtige Formeln
- 𝑝 Anzahl der Prozessoren
- 𝑇1 : Zeit(-schritte) mit 𝑝=1 Prozessoren
- 𝑇𝑝 : Zeit(-schritte) mit 𝑝>1 Prozessoren
- 𝑍1 : Anzahl der Operationen mit 𝑝=1 (𝑍1=𝑇1)
- 𝑍𝑝 : Anzahl der Operationen mit 𝑝>1 Prozessoren (𝑍𝑝>𝑇1)
![[Pasted image 20250709095942.png]]


### 11.2.6 Amdahl's Gesetz
 1.1 Wie hoch müsste der Anteil der Gesamtzeit sein, welcher im Vektor-Modus berechnet werden könnte, wenn
𝑆=2

gelten soll?
- $S = 2$
- $p=10$
$$
\begin{gather}
S=\frac{1}{(1-f)\cdot \frac{f}{p}}\\
2=\frac{1}{(1-f)\cdot \frac{f}{10}}\\
f=\frac{1-0.5}{0.9}=56\%
\end{gather}
$$
 1.2  Wieviel Prozent der optimierten Ausführungszeit $T_{after}$ wird bei Anwendung des verbesserten Rechnersystems im Vektor-Modus verbracht? _Tipp: Denken Sie hierbei über die Bestandteile der Formel oben nach._
- Da wir jetzt parallelisieren wollen, dann kann man die andere Formel benutzen 
>[!Question]
>Wieso ist 11% 
>Wieso ist f= 100s
>Was passiert wenn man f größer macht 


$$
\begin{gather}
S_{p}=\frac{T_{1}}{T_{p}}\\
2=\frac{100s}{T_{p}}\\
T_{p}=50s\\
\implies 11 \%
\end{gather}
$$

 1.3 Nehmen Sie nun an (𝑝 bleibt gleich), dass Sie nach einer Messung wissen, dass der Anteil, den das System den Vektor-Modus nutzt, bei 65% liegt. Die Hardware Design Gruppe schätzt, dass Sie mit einer signifikanten Investition in der Lage wären, den aktuellen Speedup zu verdoppeln. Stattdessen wäre auch eine Erhöhung des Anteils an Vektorisierung durch die Compiler Gruppe möglich. Wie hoch müsste der Anteil an Vektorisierung sein, damit ein verdoppelter Speedup erreicht werden kann?

$$
S=\frac{1}{(1-0.65)+\frac{0.65}{10}}=2.41
$$


Nehmen Sie nun ein Programm, bei dem in 40% der Laufzeit Code ausgeführt wird, welcher optimiert werden kann. Ist es möglich einen Speedup von 2 zu erreichen?  _Tipp: Führen Sie eine Grenzwertbetrachtung durch._

- mit $p \to \infty$ (Grenzwertbetrachtung)
$$
S=\frac{1}{(1-0.4)+0.4\cdot p}
$$
Für $S=2$ dann muss **50%** der Laufzeit optimiert werden

### 11.2.8 Prozessor-Performance II
![[Pasted image 20250709102035.png]]

### 11.2.10 Optimierung II
*Für die dritte Aufgabe*
3) Wie viele Bearbeitungsschritte benötigen Sie minimal, um diesen optimierten Algorithmus parallel zu verarbeiten? Nehmen Sie hierfür an, dass eine Operation zwei Eingangsoperatoren in einem Takt verarbeitet. Kommunikationsoverhead wird nicht beachtet.
![[Pasted image 20250709102703.png]]
*Für die parallele Ausführung wird untersucht, welche Teilrechnungen unabhängig voneinander gleichzeitig durchgeführt werden können. Die gleichzeitig bearbeitbaren Schritte werden auf die Prozessoren verteilt, was hier in den Ebenen dargestellt ist. Eine Ebene darf also nicht mehr Berechnungsschritte als Prozessoren enthalten. Die Zahl der Ebenen mit Berechnungsschritten ergibt die Zahl der Schritte im parallelen Ausführungsfall.*
![[Pasted image 20250709102938.png]]


### 11.2.11 Optimierung III
die unten erfragten Kennwerte. Nehmen Sie dabei an, dass der Algorithmus mit **𝑝=4** Prozessoren parallel berechnet werden kann. Die sequentielle Ausführung benötigt **𝑇1=11** Schritte. Runden Sie Fließkommawerte ggf. auf die zweite Nachkommastelle.
>[!Important]
>Diese werte würden mit p=5 berechnet
- $S= \frac{T_{1}}{T_{P}} =\frac{11}{5}=2.2$
- $T_{p}= \frac{T_{1}}{S} =\frac{11}{2.2}=5$
- $E_{P}= \frac{Z_{P}}{Z_{1}} = \frac{2.2}{3}=0.73$
- $R_{P}=\frac{Z_{P}}{Z_{1}}=\frac{11}{11}=1$
- $U_{P}=\frac{Z_{p}}{T_{p}\cdot p}=\frac{1}{5\cdot 4}=\frac{1}{20}$


## 11.3 Befehlsmixe
### 11.3.1 Befehlsmixe

$$
\frac{100}{(0.4\cdot 1)+(0.2 \cdot 1)+(0.105 \cdot 5)+(0.2 \cdot 5)+(0.095 \cdot 9)}=33.56
$$

(2) Architektur 3 ist ähnlich wie Architektur 2, nutzt eine 10% niedrigere Taktfrequenz um trotz höherer Komplexität der Ausführungseinheiten eine ähnliche TDP wie Architektur 1 zu haben. Ist Architektur 3 in der Ausführung des oben genannten Programmes schneller als Architektur 1?

$$
\frac{83.4s}{0.9}=92.66s
$$

(3) Wenn Architektur 3 ein Integer-basiertes Programm ausführt (Keine Fließkommaberechnungen), wobei die Anzahl der Sprünge im Programm ca. 5% der Befehle ausmacht, ist sie dann schneller als Architektur 1?


## 11.4 Roofline Model 
### 11.4.1 Beispiel

$$
1 \text{ core }\cdot 2 \frac{\text{SIMDUnit}}{\text{core}}\cdot 1 \frac{\text{SIMDReg}}{\text{ SIMDUnit} \cdot \text{ cycle}}\cdot \frac{256}{64}
$$


