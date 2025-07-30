- tener el Software constantemente actualizado 
	- `sudo apt install unattended-upgrades`
	- `sudo dpkg-reconfigure --priority=low unattended-upgrades`
		- mantiente al sistema actualizandolo constantemente

	- cambiar *50unattended-upgrades* para que informe de los paquetes actualizados

- No utilizar root en el servidor 
	- es más seguro usar otro usr y darle privilegios `sudo`
		- `adduser usr_name`
		- `usermod -aG sudo usr_name`

- evitar `ping` al servidor
	- `sudo vim /etc/ufw/before.rules`
	- (añadir linea en "*ok icmp codes for Input*")
		- `-A ufw-before-input -p icmp --icmp-type echo-request -j DROP`
 


Linuxserver.io => Imágenes confiables para containers

##### **Watchtower** => actualización automática de imágenes de contenedores 

---
## SSH
### SSH - Keys 
- copiar llave pública del cliente en servidor 
- crear carpeta: `.ssh`
	 `scp id_rsa.pub lugar_donde_copiar_en_servidor/.ssh/authorized_keys`
- cambiar permisos en el servidor (para que el cliente pueda leer archivos de claves)
	 `chown -R nombre_de_usr:nombre_de_usr .ssh`
#### SSH server
ayuda a prevenir intentos de inicio de bots con contraseñas

`sudo vim /etc/ssh/ssh_config`
- configurar el servidor para que **únicamente** acepte SSH-Keys
	- cambiar: *PasswordAuthentication* yes -> *PasswordAuthentication* **no**

- para que nadie pueda autenticarse como RootUsr
	- cambiar: *PermitRootLogin* yes -> *PermitRootLogin* **no**

luego reiniciar SSH server
`sudo systemctl restart ssh`

---
### Administración de Shell con 2FA
#### Teleport (proxy)
- luego de la autentificación se puede conectar a todos los servidores 
- permite túneles inversos (para firewalls)
- permite ver quién está conectado a qué servidor (y tiempo en él)
- Signal Sing-On para integrarlo con Active Directory

---
## Seguridad de Network
`ss -tuln` -> listado de los puertos en *Listening*

### UncomplicatedFirewall
- ayuda a controlar el tráfico de entrada y salida (no lo escanea)
- no controla las conecciones de docker containers 


### Reverse Proxy
- para desplegar aplicaciones Web con SSL
- Nginx Proxy Manager


### DMZ, VPNs, Access Gateways
- negar el acceso de no confiables networks a interfaces administrativas
- limitar el IP de los servidores a una interfaz protegida por DMZ
#### Cloud instances 
- configurar todas las webs administrativas que esuchen únicamente a una cloud network interna 
- VPN para establecer conexión entre las máquinas
#### WireGuard


### Intrusion Detection System
**Fail2Ban**
- detecta y banea IP con multiples intentos fallidos de inicio al servidor
	- protege de intentos de Brute Force 
`sudo apt install fail2ban`
`sudo systemctl enable fail2ban -now`

`sudo fail2ban-client status sshd`
- lista de IPs baneadas

---
## Limitar Aplicaciones
### AppArmor 
`sudo apparmor_status`
- muestra perfiles para aplicaciones
### Docker
