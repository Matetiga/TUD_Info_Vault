## 4.0.1
*Die Wafer Ihrer Fabrik haben einen Durchmesser von 350 mm und kosten 2.000$ pro Stück. Von 1000 Wafern sind 997 ganz.*
*Die einzelnen Dies sind 20mm * 30mm groß*

*Wie viele Dies passen auf einen Wafer?*
$$
\frac{\pi \cdot \left( \frac{350}{2} \right)^{2}}{20 \cdot 30}-\frac{\pi \cdot 350}{20 \cdot 30 }=128
$$

*Wie viele ganze Dies können Sie im Durchschnitt pro Wafer bekommen?*
$$
128 \cdot 0,997 \cdot \frac{1}{\left( 1+0,008 \cdot \frac{20 \cdot 30}{100} \right)^{14.5}}=64.66
$$
*Welche Kosten entstehen für einen Die*
$$
\frac{2000 \$}{64.66}=30.94
$$

---

## 04.3.1 Fließkommaformate 
- Wenn man 0.6 als Single Precision speichert, dann ist die Mantisse nur 23 Bit lang (somit ist unpräziser)
![[Pasted image 20250507095417.png]]


---
## 04.3.2 Intel Xeon Platinum 8180

*Alle Kerne, AVX-512+FMA, 2 Verarbeitungseinheiten pro Kern*

- $1 \frac{\text{SIMDreg}}{\text{SIMD} \cdot \text{cycle}}$ Da es voll PipeLined ist 
- 28 Cores 
- $2 \frac{\text{ SMIDunit}}{\text{core}}$ Da FMA
$$
28 \text{cores} \cdot 2 \frac{\text{ SMIDunit}}{\text{core}} \cdot \frac{512 \text{ vector length}}{32 \text{ operand length}} \cdot 1 \frac{\text{SIMDreg}}{\text{SIMD} \cdot \text{cycle}} \cdot 2 \frac{\text{FLOP}}{resultat} = 1792
$$
- Dann muss man es mit der minimalen Frequenz (*Base*) multiplizieren , um die minimale Fließkommaperformance in GFLOPs zu bestimmen 
---

##  04.4.1 x86 ISA und Encoding

![[Screenshot from 2025-05-06 15-27-49.png]]
![[Pasted image 20250506152811.png]]
### Struktur des Codes
==Operation  (Wert von Mod + Wert von Reg) Offset==
- Die Werte von Mod/Reg sind in Binär, also dann muss man die miteinander addieren und in hexadezimal darstellen 

 `MOV ebx, [ecx]` -> 0x8B19
- *8B* : da wir eine Adresse im Register laden wollen 
- *19* : kommt aus 00 (**Register Indirekte Adressierung**) + 011 (**EBX**) + 001(**ECX**)
	- $00011001_{2}=19_{16}$

`ADD ebx, [ecx+4]` -> 0x0359*04*
- *03* : da Adresse in register
- *59* : aus 01 (**1-Byte displacement**, 4 passt in 1 Byte) 011(**EBX**) 001(ECX)
	- $01011001_{2}=59_{16}$
- *04* : Offset

`AND eax, ebx` -> 0x21D8
- *21* : Da Register zu Register (dritte Spalte)
- *D8* : aus 11011000 (*es ist in umgekehrte Reihenfolge, da Register ist src2*)
	- *11* : Register Direkte Adressierung 
	- *011* : EBX
	- *000* : EAX

`MOV ebx, [ecx+8]` -> 8B5908
- *8B* : Register und Adresse in Register
- *59* : aus 01011001 
	- *01* : Register indirekte Adressierung
	- *011* : EBX
	- *001* : ECX
- *08* : aus Displacement 

`OR eax, ebx` -> 0x09D8
- *09* : Src1 Register und Src2 Register
- *D8* : aus 
	- *11* : Register direkte adressierung 
	- *011* : EBX (**in umgekehrte Reihenfolge**)
	- *000* : EBA 