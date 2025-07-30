## Klassen
- Veraltet 
![[Pasted image 20250508115932.png]]


## Packetformat
- Die Packete können **fragmentiert** werden, wenn MTU (*Maximal Transmission Unit*) nicht groß genug ist 
	- Jedes Fragment hat dieselbe "*Common IP Header*" (**Identification**)
- **MF** : *More Fragment* Bit 
	- 1 : falls mehr Fragmente folgen 
	- 0 : falls das letzte of a Datagram 
- **DF** : *Don't Fragment* Bit
	- all router must forward packets **up to a size of 516 Bytes**, everything beyond that is optional
- **Time to Live** : *TTL* , Damit lassen sich Schleifen abbrechen
	- jedes router reduziert TTL bei 1, und bei TTL =1 wird das Packet verworfen
- **Header Checksum** : Schutz nicht die Payload
- **Options** : sind meistens für Sicherheitsgrunden deaktiviert 
![[Pasted image 20250508121247.png]]