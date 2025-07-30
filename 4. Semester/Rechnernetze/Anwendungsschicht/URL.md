## Uniform Resource Locator
`protocol://hostname[:port]/directory_path/resource`
- *protocol* : z.B. -> HTTPS, FTP, ...
- *hostname* : DNS_NAME
- *port* ist Optional da für bekannte Protokolle Port schon bekannt (HTTP 80, ...)
- *directory_path/resource* : Identifiziert Ressource beim Ziel


### Pfad basierte Kodierung
z.B. `https://www.tu-dresden.de/ing/cs/sya`
- Einfache Verwaltung von Zertifikate 
- Nur ein DNS-Lookup für die Hauptdomäne (z.B.: `www.tu.dresde.com` und nicht für `www.tu.dresde.com/studium`)
- Besser Erkennung der Hierarchie innerhalb einer Hauptdomäne

### Host basierte Kodierung
z.B.: `https://sya.cs.ing.tu-dresden.de`
- Besser Skalierbarkeit und Verteilung, da jede Subdomain sein eigene Server haben kann (*aber Mehr Servers impliziert dass es teuer ist*)
- Verbesserte Trennunng von Diensten 
- Sicherheitisolierung 
- Komplexe Zertifikatverwaltung 
- Erhöhte DNS-Overhead (Für jede andere Subdomain ist ein DNS-Lookup erforderlich)
