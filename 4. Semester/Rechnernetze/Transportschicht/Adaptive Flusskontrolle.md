Mit dem Mechanismus wird sicher gestellt, dass der Sender *nicht mehr Daten als was den Empfänger verarbeiten* kann schickt
- Es passt sich dynamisch auf der Netzwerkverbindung und die Kapazität des Empfängers an

## Schritte 
### Schiebefenster
- Empfänger gibt an die Menge an Daten, die er verarbeiten kann (Größe des Speicherplätzes -> **Window Size**)
- Die Window Size gibt an, wie viele Bytes der Sender ohne Bestätigung senden darf
### Senden von Datenpaketen
- Der Sender schickt Datenpakete in Blöcken, die nicht die vom Empfänger angegebene Window Size überschreiten
- Der **Sender hält an**, wenn die **Window Size erreicht ist**, und wartet auf ein ACK vom Empfänger, bevor er weitere Daten sendet

### Empfang und Verarbeitung:
-  Sobald der Empfänger die Daten verarbeitet (z. B. an eine Anwendung weitergeleitet) hat, gibt er *Speicherplatz im Puffer frei* und kann dem Sender eine neue, möglicherweise größere Window Size mitteilen

### Dynamische Anpassung:
- Empfänger kann die Window Size erhöhen/verkleinern (**dynamsiche Anpassung je nach die Platz im Puffer**)
## Beispiel 
![[Pasted image 20250626122641.png]]