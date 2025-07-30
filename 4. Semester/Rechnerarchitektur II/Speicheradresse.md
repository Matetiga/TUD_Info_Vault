## Definition
Eine Speicheradresse ist ein eindeutiger Bezeichner (meist eine Zahl), der einen bestimmten Speicherort im Arbeitsspeicher (RAM) oder in anderen Speichermedien (z. B. Cache) angibt.

### Funktion
Sie wird verwendet, um Daten oder Befehle aus dem Speicher zu lesen oder in den Speicher zu schreiben.

---
## Eigenschaften
**Ort**: Speicheradressen verweisen auf den **Hauptspeicher** (RAM) oder andere Speicherebenen (z. B. Cache, Festplatte).
- **Größe**: Die Adresse ist typischerweise 32 Bit (bei 32-Bit-Systemen, bis zu 4 GB adressierbar) oder 64 Bit (bei 64-Bit-Systemen, sehr großer Adressraum).
- **Zugriff**: Der Zugriff auf Speicheradressen ist relativ langsam, da Daten über den Speicherbus zwischen RAM und Prozessor übertragen werden müssen.
- **Beispiel**: Die Adresse 0x7FFF5FBFF8 könnte auf ein Byte im RAM zeigen, das einen Wert (z. B. 42) enthält.

### Verwendung
Wird in Programmen genutzt, um auf Variablen, Arrays oder andere Daten im Speicher zuzugreifen, z. B. beim Laden einer Variable in ein Register.