**Used to protect data sent over an IP network**
encrypts data at the origin, decrypts them at the destiny
- authenticate their sender and receiver
- verifies data integrity
makes use of [[1. Asymmetric Encryption]] and [[2. Symmetric Encryption]]


## Operation modes
### Transport Mode
- protects the payload of the IP packet
- solo encripta la carga útil de los paquetes

### Tunnel Mode
- cifran todos los datos enviados entre dos puntos de conexión
- útil para transferir datos en redes públicas
- encripta todos los datos (encabezado y carga útil)
#### Tunneling protocoll
Imagine putting a letter (*data*) inside an envelope (*inner protocol*), then putting that envelope inside another envelope (*outer protocol*)
- used in VPNs
- used to bypass firewalls and network restrictions

---

## Uses
- creating VPNs to be able to connect to the server remotely 
	- VPN IPsec -> datos se codifican en la computadora y decodifican en el servidor  
