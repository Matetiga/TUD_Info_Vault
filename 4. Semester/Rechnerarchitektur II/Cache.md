## Index
- Sagt uns in welcher Gruppen von Cachezeilen wir suchen mussen 

## Tag
- Mit dem Tag findet man den richtigen Satz in der Cachezeile


---

## Beispiel 
- 32KiB -> 512 Cache Zeilen 
	- ($\frac{32 \cdot 1024 }{64 \text{ Cachezeile Länge}}=512$)
- Für 32-Bit Addressen :
	- $\log_{2}(512)=9$ Bits für **Index**
	- Jede Cache Zeile ist 64 Byte lang -> $\log_{2}(64)=9$ Bits für **Byte select**
	- $32 \ Bit - 9 \ Bit - 6 \ Bit = 17$ Bits für **Tag**
![[Pasted image 20250502175408.png]]