## 6.1 Kenngrößen und Peak Perfomance
### 06.1.2 Eigenschaften
**IPC:** (Instructions-per-Second) ist unabhängig vom Instruction-Typ, bezieht sich also sowohl auf Sprung, Load-/Store-Befehle, ..., als auch auf Integer- und Floating-Point-Befehle.
**FLOPS:** (Floating-Point-Operations-per-Second) ist die wichtigste Größe im Bereich der Naturwissenschaftlichen Simulationen, als auch im Hochleistungsrechnen. Wie schon in früheren Übungen beobachtet ist diese Größe abhängig von den Verwendeten Befehlssatzerweiterungen (SSE, AVX, ...), die unsere Register erweitern, oder wie im Fall von FMA zwei arithmetische Operationen in einem Befehl vereinen.
**Integer-OPS:** Ist das Gegenstück zu den FLOPS und bezieht sich auf die Integer-Operationen-pro-Sekunde.
**I/O-OPS:** Bezieht sich auf die Ein- und Ausgabe Operationen, pro Sekunde.
![[Pasted image 20250707180329.png]]

### 06.1.3 I/O-OPS (IOPS) Varianten
![[Pasted image 20250707180436.png]]

### 06.1.4 Bewertung von Allzwecksystemen
![[Pasted image 20250707180830.png]]

### 06.1.5 Theoretische Peak-Performance
![[Pasted image 20250707180943.png]]


## 06.2.1 SPARC64 III 
### 06.2.1.1 Peak-Perfomance
![[Pasted image 20250707182215.png]]

### 06.2.1.2 Speicherzugriffsoperationen pro Zeit
Wenn nun alle Operanden und Befehle gleichzeitig aus dem Speicher geholt werden, so brauchen wir:
- 4 Speicherzugriffe für Instruction Fetch (Befehle werden aus dem Speicher geholt)
- $2*4=8 \implies 2\text{ Operanden }∗4\text{ Befehle }=8$ (jede Operation hat 2 Operanden)
- Speicherzugriffe für alle Operanden (jeweils 2 Operanden pro Instruktion)
- 4 Speicherzugriffe zum Zurückschreiben der Ergebniss
![[Pasted image 20250708232121.png]]

### 06.2.1.3 Fused Multiply Add

![[Pasted image 20250707183351.png]]



---
## 06.2.2 Intel Core i7 2600K
*Ein Intel Core i7 2600K  mit vier Kernen und einer Taktfrequenz von 3.4 GHz kann pro Kern und pro Takt vier Instruktionen auf die Ausführungseinheiten aufteilen. Jeder Kern verfügt zudem über sechs Verarbeitungseinheiten, darunter zwei Floating-Point-Einheiten, die AVX unterstützen. Die Verarbeitungsbreite der 256 bit breiten Vektorregister beträgt 256 Bit. Die Befehle werden im 3-Operanden-Format verarbeitet*
### 06.2.2.1 Floating-Point-Peak-Performance

- **Berechnen Sie die Theoretische Floating-Point-Peak-Performance (FPPP) für Double Precision.**
- da double Precision $\to 64 \text{ Bit}$
- 2 Floating Point Einheiten
$$
FPPP= 3.4\cdot 10^{9} \frac{\text{cyc}}{s} \cdot \frac{256 \frac{\text{bit}}{\text{ResultReg}}}{64\frac{\text{bit}}{\text{FResult}}} \cdot 4 \text{ cores} \cdot 2 \frac{\text{ SMIDFPN}}{\text{core}} \cdot 1 \frac{\text{ResultReg}}{\text{SIMD} \cdot \text{cyc}} \cdot 1 \frac{\text{ FLOP}}{Result}= 108.8 \text{ GFLOP}
$$

**Würde die Betrachtung von Hyper-Threading die FPPP beeinflussen?**
- Nein, da FPPP ein Idealfall betracthet wo alle Ressourcen genutzt werden. Mit Hyper threading wurden ungenutzte Prozesse eine Arbeit bekommen, aber es gibt keine die frei ist 

### 06.2.2.2 Speicherbandbreite
- Bestimmung der Bandbreite 
- Da es eine AVX Instruktion, wo zwei Register gelesen werden und in einem geschrieben wird ($a[i]=b[i]+c[i]$)
- *Gesamtdaten pro Instruktion*  : $2 \text{ ReadRegister} \cdot 32 \frac{\text{ Byte}}{\text{Register}} + 1 \text{ WriteRegister} \cdot 32 \frac{\text{ Byte}}{\text{Register}}=96 \text{ Byte}$
- *Datenfluss pro Takt und Kern*  : $96 \text{ Byte } \cdot 2 \frac{\text{ Operation}}{\text{ takt}}= 192 \frac{\text{ Byte }}{\text{Takt}}$
- *Datenfluss pro Sekunde und Kern*  : $192 \frac{\text{Byte}}{\text{Takt}} \cdot 3.4\cdot 10^{9}=6.528 \cdot 10^{11} \text{ Byte}$
- **Gesamtdatenfluss**  $192 \frac{\text{Byte}}{\text{Takt}} \cdot 3.4\cdot 10^{9} \cdot 4 \text{ Kerne}=2.6 \cdot 10^{12} \text{ Byte}$

---

## 06.2.3 AMD Ryzen 9 3950X
*Ein AMD Ryzen 9 3950X mit 16 Kernen und einer Taktfrequenz von 3.5 GHz kann pro Kern und pro Takt vier Instruktionen auf die Floating Point Pipes aufteilen. Jeder Kern verfügt zudem über 11 Verarbeitungseinheiten, darunter vier Floating-Point-Einheiten, die AVX unterstützen. Die Verarbeitungsbreite der 256 Bit breiten Vektorregister beträgt 256 Bit. Die Befehle werden im 3-Operanden-Format verarbeitet*
### 06.2.3.1 Floating-Point-Peak-Performance

$$
FPPP = 3.5\cdot 10^{9} \frac{\text{cyc}}{s} \cdot \frac{256 \frac{\text{bit}}{\text{ResultReg}}}{64\frac{\text{bit}}{\text{FResult}}} \cdot 16 \text{ Kerne} \cdot 4 \text{ FP-Einheiten} = 896 \cdot 10^{9} \text{ FLOPS}
$$

### 06.2.3.2 Floating-Point-Peak-Performance mit FMA

*Zwei der vier Floating-Point Units können FMA Operationen im Format `g[i] = g[i] * h[i] + j[i]` ausführen. Um die dafür nötigen Operanden bereitzustellen, werden jedoch die Operanden-Inputs einer der übrigen Floating-Point Units deaktiviert. Es können also maximal zwei AVX-FMA und eine AVX-ADD Operation im Format `a[i] = b[i] + c[i] `durchgeführt werden¹*

- Anzahl der Operationen = 5, da FMA eine Addition und eine Multiplikation pro Takt ausführen kann (und **zwei FMA-Einheiten**), und **eine nutzbare ADD** (AVX) Einheit 
$$
FPPP_{FMA}=3.5\cdot 10^{9} \frac{\text{ cyc}}{\text{s}} \cdot 16 \text{ kerne} \cdot 5 \text{ Operationen} \cdot \frac{256 \frac{\text{bit}}{\text{ResultReg}}}{64\frac{\text{bit}}{\text{FResult}}}=1120 \text{ GFLOP}
$$

### 06.2.3.3 Speicherbandbreite
##### AVX ohne FMA:
$$
\text{ Bandbreite}= 3.10\cdot 10^{9} \frac{\text{cyc}}{s} \cdot 16 \text{ Cores} \cdot \left( 2 \frac{\text{ Register}_{Read}}{\text{Instruction}_{AVX}} +1 \frac{\text{Register}_{\text{Write}}}{\text{Intruction}_{AVX}} \right) \cdot 32 \text{ Byte} \cdot 4 \text{FP-Einheiten}=21.5 \cdot 10^{12}
$$

##### 2 * AVX mit FMA plus 1 * AVX ohne FMA:
$$
\begin{gather}
\text{Bandbreite} = &\\
 & 3.5\cdot 10^{9} \frac{\text{cyc}}{s} \cdot 16 \text{ Kerne} \\
& \cdot ( 2 \frac{\text{ Instruktion}_{FMA}}{\text{cycle} \cdot \text{Kern}} \left( 3 \frac{\text{ Register}_{\text{Read}}}{\text{Intruction}_{FMA}}+1 \frac{\text{Register}_{Write}}{\text{Intruction}_{FMA}} \right) \\
& +  1 \frac{\text{ Instruktion}_{AVX}}{\text{cycle} \cdot \text{Kern}} \left( 2 \frac{\text{ Register}_{\text{Read}}}{\text{Intruction}_{AVX}}+1 \frac{\text{Register}_{Write}}{\text{Intruction}_{AVX}} \right) ) \\
& \cdot 32 \frac{\text{ Byte}}{Register}\\
& =19.7 \text{ TB/s}
\end{gather}
$$