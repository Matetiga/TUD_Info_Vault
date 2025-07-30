Eine Sprache L ist *nachweis-polynomiell* wenn es für sie einen polynomiellen [[Polynomielle Verifikator]] gibt
- L ist genau *nachweis-polynomielle* genau dann, wenn $L \in NP$


---
## Beweise
### =>
Gibt es einen polynomiellen Verifikator, dann gibt es auch eine *polynomiell zeitbeschränkte NTM*, die das Zertifikat rät und anschließend verifiziert

### <=
Gibt es eine polynomiell zeitbeschränkte NTM, so gibt es einen polynomiellen Verifikator, der diese NTM simuliert: Das Zertifikat ist ein akzeptierender Lauf