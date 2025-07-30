## 07.1 Vektorrrechnen

### 07.1.2 Speicherverschränkung I
![[Pasted image 20250530175153.png]]

### 07.1.3 Speicherverschränkung II
- Die Daten einer Vektorrechnung werden in physischen separaten Speicherbänken gespeichert 

![[Pasted image 20250530175120.png]]

### 07.1.4 Eigenschaften Vektorrechner
![[Pasted image 20250530175230.png]]

---

## 07.2 Arithmetisches Pipelining und Chaining
### 07.2.1 Arithmetische Pipeline Einführung
![[Screenshot from 2025-05-30 17-59-27.png]]

### 07.2.2 Arithmetische Pipeline
1. Exponente Vergleichen
2. Mantisse des kleineren Operanden nach rechts verschieben (>>) bis beide Exponenten gleich sind
3. Festkommaaddition der Mantisse 
4. Normalisierung

### 07.2.3 Arithmetische Pipeline Speedup
Für die Laufzeit ohne arithmetisches Pipelining müssen wir die Multiplikationen seriell hintereinander ausführen, d.h immer eine komplette Multiplikation abwarten und dann erst die nächste anstoßen. Dies ergibt als Formel $𝑛 \cdot 𝑘_{𝑚𝑢𝑙}$. Bei einem Vektorrechner müssen wir nur einmalig ein Instruction Fetch, Instruction Decode und Writeback ausführen, da danach hintereinander ein gleichartiger Befehl, hier die Multiplikation ausgeführt wird. Folglich haben wir als Gesamtformel  $𝑇_{ohne}=𝑛 \cdot 𝑘_{𝑚𝑢𝑙}+𝑛_{io}$

Mit arithmetischem Pipelining stellen wir in jedem Takt eine Multiplikation fertig, wenn die Pipeline eingelaufen ist. Deshalb ist hier die Formel für Pipelining in leicht abgewandelter Form anzuwenden, die allgemeine Formel lautet $𝑇=𝑛+𝑘−1$
Das einzige was hier dazu kommt, sind die 3 Befehle Instruction Fetch, Instruction Decode und Writeback. Der Speedup berechnet sich durch $𝑆=\frac{𝑇_{ohne}}{𝑇_{mit}}$

>[!Question]
>Wieso muss man -1 Substrahieren, wenn man arth. Pipelining oder Chaining benutzt

>[!Important]
>Ohne artihmetische Piplining werden alle MUL Operationen nacheinander durchgeführt. Wenn man das arithmtische Pipelining nimmt, dann werden nur die MUL Operationen (*untereinander im Diagramm*) teilweise Parallel durchgeführt (**wie treppen** je nach einem Takt)

![[Pasted image 20250531193013.png]]

### 07.2.4 Chaining Einführung
- Bei Chaining werden die Ergebnisse nicht zurück in ein Register geschrieben um danach erst wieder von dort geladen zu werden, sondern man gibt das Ergbenis der Multiplikation direkt an die Additionseinheit weiter. Somit fungieren die beiden Operationen, weil direkt aufeinanderfolgend, wie eine zusammenhängende Operation. Deshalb erstzen wir in der Formel k durch $𝑘_{m}+𝑘_{a}$ und betrachten es als eine zusammenhängende Pipeline
![[Pasted image 20250530182748.png]]

### 07.2.5 Chaining Speedup
*Gegeben sei der gleiche Vektorrechner aus Aufgabe "Arithmetische Pipeline Speedup" mit einer Multiplikationseinheit mit 7 Stufen. Die Architektur setzt Vektorregister mit 32 Einträgen um. Die Architektur benötigt zur Verarbeitung der Befehle zusätzlich zur Ausführung der arithmetischen Operation die Schritte Instruction Fetch, Instruction Decode und Writeback. Darüber hinaus wird Befehlspipelining und arithmetisches Pipelining unterstützt.*   
*Zusätzlich ist bekannt, dass die Additionseinheit über 5 Stufen verfügt und Chaining unterstützt wird.*

*Diesmal soll auf 32 Elemente zuerst eine Multiplikation angewendet werden und dann eine Addition.*
![[Pasted image 20250531194355.png]]


---

## 07.3 Leistung 
### 07.3.1 Leistungskurve I
- Die Performance der gesuchten Rechnerart bricht hier immer kurz nach einer fixen Größe und deren Vielfachen ein, woran könnte das liegen? Welcher Rechner hat ein begrenzten Registersatz und muss danach aus dem Speicher neuladen?

- Vektorregister wird voller mit der Zeit, bis es eine zu voll ist  
![[Screenshot from 2025-05-30 18-38-28.png]]

### 07.3.2 Leistungskurve II
- Hier helfen uns die Anzahl an Puffern, die wir im System haben. Sie bestimmen maßgeblich die Kurve mit.
- **Die Kurve fällt immer mit der Zeit, da wenn ein Register voll wird, dann wird noch ein anderes Register genutzt aber was langsamer ist** 
![[Pasted image 20250530184024.png]]

### 07.3.3 Leistungskurve III
Bei  `steigende` Problemgröße sieht man immer wieder Leistungseinbrüche. Diese passieren immer dann, wenn die Problemgröße N genau `(n*V + 1)`  beträgt, also genau `(eins größer ist als)` die Länge des Vektorregisters. Das hängt damit zusammen, dass dann für ein Element nochmal ein komplettes Vektorregister geladen werden muss in dem `(V - 1)`  Plätze nicht belegt sind. Dieser Effekt lässt für `steigende` Problemgrößen nach, da das Nachladen eines weiteren Vektorregisters `(schwächer)`  ins Gewicht fällt, je häufiger das Vektorregister insgesamt nachgeladen werden muss

### 07.3.4 Leistungskurve IV
- Die Caches puffern hier unsere Speicherzugriffe, bis diese die Größe des ersten Caches (L1) überschreiten, usw. Also haben wir hier die 3 erkennbaren "Plateaus" in unserer Kurve.
![[Pasted image 20250530184944.png]]


---

## 07.4 SIMD in aktuellen Prozessoren 
### 07.4.1 Einführung Berechnung in aktuellen Prozessoren
![[Pasted image 20250601130120.png]]


### 07.4.2 Speedup
- n: Anzahl der Prozesse, die durch die Pipeline laufen
- m: Anzahl der Segmente der Pipeline
- ts: Segmentverarbeitungszeit
- k: (gleichlange) Teilprozesse
	- üblicherweise wird die Verarbeitung eines Prozesses durch die Segmente der Pipeline in m (gleichlange) Teilprozesse unterteilt (m = k)
*Nun soll ein Rechner betrachtet werden, der Werte nebenläufig berechnet. Für die Multiplikation werden 7 und die Addition 5 Stufen benötigt. Die Vektorregister sind 4 Einträge lang, der gegebene Rechner beherrscht zusätzlich arithmetisches Pipelining und es stehen zwei SIMD-Einheiten die vier Multiplikationen bzw. Additionen parallel verarbeiten: jeweils einen Wert des Vektorregisters. Zusätzlich gibt es Stufen Instruction Fetch, Instruction Decode und Writeback (IF, ID, WB).*

*Betrachtet werden 32 Elemente, auf die eine Multiplikation gefolgt von einer Addition angewandt werden soll. Dabei gibt es -> Abhängigkeiten zwischen den Daten, sodass die Additionen erst durchgeführt werden können, nachdem sämtliche Multiplikationen berechnet wurden*

Für den Speedup
- $S_{\text{p\_ohne}}=\frac{78}{30}=2.6$

![[Pasted image 20250601125928.png]]


---

## 07.5 Verständnis
### 07.5.1 Zeitlicher Ablauf I
*Von Takt 9 zu Takt 10 ist gut erkennbar, dass wir ohne Write Back der Multiplikation direkt mit der Addition weiter machen können. Dieses Prinzip haben wir in dieser Übung bereits kennengelernt. Ein weiterer Hinweis ist, dass wir für alle Multiplikationen nur genau ein Instruction Fetch und Decode machen müssen.*
![[Pasted image 20250601130322.png]]

### 07.5.2 Zeitlicher Ablauf II
*Hier sieht man deutlich den Unterschied zu der vorherigen Abbildung - wir brauchen für jeden neuen Block von Multiplikationen/Additionen ein neues Instruction Fetch, Instruction Decode und Writeback. Außerdem erkennt man, dass 4 Multiplikationen gleichzeitig ausgeführt werden können und diese erst nach einem Write Back von der Addition genutzt werden können. Folglich nutzen wir hier eine SIMD-Erweiterung die uns 4 Multiplikationen/Additionen gleichzeitig ermöglicht.*
![[Pasted image 20250601130440.png]]

### 07.5.3 Zeitlicher Ablauf III
*In dieser Abbildung sehen wir die Ähnlichkeit zur ersten Abbildung (7.5.1). Der einzige Unterschied besteht darin, dass wir hier auf das Write Back der Multiplikation warten müssen, bevor wir mit der Addition anfangen können. Deshalb handelt es sich hier um eine Vektorrechner ohne Chaining.*
- Man erkennt auch die WB der Multiplikation vor dem Beginn der Addition (deswegen auch $n_{io}=4$)

![[Pasted image 20250601130535.png]]



## 07.6
### Encoding auf x86
`MULPS xmm0, [eax]`
- 0F59 (Operation)
- MOD R/M : 00 (*MOD*) 000 (für *mxx0*) 000 (für *eax*) ->$00\  000 \ 000_{2}$ = $00_{16}$ (**in hex**)


`VMULPS ymm7, ymm1, [ecx]`
- man nimmt die Operation : 0x <2-Byte VEX> 59
- <0-Byte VEX> : C5
- <1-Byte VEX> : 1($\overline{R}$)  1($\overline{v_{3}}$) 110 ($\overline{v_{3}},\overline{v_{2}},\overline{v_{1}}$) 1 (für 256-bit) 00 = 1111 0100 = $F4_{16}$
	- man nimmt für $\overline{v_{3}},\overline{v_{2}},\overline{v_{1}}$ das Invers von 1
- MOD R/M : 00 (Mod) 111 (für *ymm7*) 001  (für *ymm1*) = 00 111 001 = $39_{16}$
- Insgesamt : 0x C5 F4 59 39

`VADDPS ymm3, ymm7, ymm5`
-  man nimmt die Operation : 0x <2-Byte VEX> 58
- <0-Byte VEX> : C5
- <1-Byte VEX> : 1($\overline{R}$)  1($\overline{v_{3}}$) 000 ($\overline{v_{3}},\overline{v_{2}},\overline{v_{1}}$) 1 (für 256-bit) 00 = 1100 0100 = $C4_{16}$
	- man nimmt für $\overline{v_{3}},\overline{v_{2}},\overline{v_{1}}$ das Invers von 7
- MOD R/M : 11 (Mod) 011 (für *ymm3*) 101  (für *ymm5*) = 11 011 101 = $DD_{16}$
- Insgesamt : 0x C5 C4 58 DD


**Sequentiell** 
- (8 Byte (Multiplikation) + 8 Byte (Addtion) ) $\cdot$ 4 (Byte Codelänge) = 64 Byte



## 07.7
### Beispiel - Pixel Blending
Um alles sequentiell auszuführen zählen wir die Anzahl an unterschiedlichen Operationen im gegebenen Code (25 Stück). Die einzige Operation, die wir optimieren können, ist `255- x[alpha]`, da diese 4 mal vorkommt. D. h. wir können 3 Operationen davon einsparen. `(25-3=22)`

Für das parallele Verarbeiten teilen wir die Operation in gleichzeitig ausführbare Gruppen ein. So können z.B. `x[r]*x[alpha]` parallel mit `x[g]*x[alpha]` und `x[b]*x[alpha]` ausgeführt werden