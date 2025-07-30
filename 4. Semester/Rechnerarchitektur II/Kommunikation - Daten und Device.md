
## Allgemeiner Aufbau 
- Start 
- Senden der Adresse des Target-Devices (7 Bit)
 - Senden ob Zugriff lesend oder schreibend (1 Bit)
- Ack des Target Devices
- Ggf. Senden weiterer Commands und Daten (jeweils 8 Bit + jeweils *Ack* des Target-Devices)
- Abhängig von Command sendet Target-Device Daten (jeweils 8 Bit + *Ack* des Control-Devices)! *Ack* des Control-Devices für Empfang beim Read ist ggf. ein *Nack*
 - Stop

![[Pasted image 20250530170016.png]]

