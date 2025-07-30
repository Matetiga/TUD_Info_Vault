## ![[Hamming Kode - Linearkodes]]
## ![[Anzahl der Kontrollstellen]]

### Beispiel 
Die Datenwort `0110 1010 0111 1011` (mit LSB in der *linken Seite*) muss in Kodewort umgewandelt werden 
 - **01**0**0** 110**0** 1010 0110 **1** 1011
 - jede markierte Bit ist eine Kontrollstelle (gerade Paritätsbit) mit **folgendes Schema**:
	- *Bit 1* prüft die Bits 3,5,7,9,11,13,15,17,19,21
	- *Bit 2* prüft die Bits 3,6,7,10,11,14,15,18,19
	- *Bit 4* prüft die Bits 5,6,7,12,13,14,15,20,21
	- *Bit 8* prüft die Bits 9,10,11,12,13,14,15
	- *Bit 16* prüft die Bits 17,18,19,20,21
 
