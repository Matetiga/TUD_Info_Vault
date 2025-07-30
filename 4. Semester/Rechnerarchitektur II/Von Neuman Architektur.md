Von-Neumann Rechner beziehen sowohl *Befehle*  als auch *Daten* über einen einzigen *Speicher*. 
- Daher behindern sich die Operationsstufen *Instruction Fetch* und *Operand Fetch* gegenseitig.
- Eine Architektur, die dieses Problem löst ist die *Harvard*-Architektur. Hier werden *Daten* und *Befehle* in getrennten Speichern gehalten.

Von-Neumann Rechner arbeiten Befehle streng *sequenziell* ab.
## Architektur 
![[Pasted image 20250411115408.png]]
### Befehlzyklus (Pipeline)
1. Instruction Fetch
2. Decode
3. Operation Fetch 
4. Execute 
5. Write-Back