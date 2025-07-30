**Uncomplicated Firewall** 

## Basics
```txt 
$ sudo ufw disable

// to make new rules be implemnted and running
$ sudo ufw reset

$ sudo ufw enable
```
#### Delete Rules
```txt
$ sudo ufw status numbered
$ sudo ufw delete <rule_number>
```

#### Allow basic services
```txt
- SSH: `$ sudo ufw allow ssh`
- HTTP: `$ sudo ufw allow http`
- HTTPS: `$ sudo ufw allow https`
```

---
#### Status
`sudo ufw staus `

---
## UFW Allow Port
`sudo ufw allow 80/udp`
- this allows (**all incoming** *udp*) traffic on port 80

`sudo ufw allow 80/tcp`
- this allows (**all incoming** *tcp*) traffic on port 80
- for example if you are hosting a web page

`sudo ufw allow from <specific_ip> to any port 80`
- allows a *only a specific ip* to connect to port 80

#### Allow multiple ports
`sudo ufw allow 2000:2100/tcp`
- allows from port 2000 to port 2100

`sudo ufw allow 80,443,8080/tcp`
- allows multiple specific ports

---
## Allow SSH 
`sudo ufw allow 22/tcp`
- [[Common Ports]] for SSH is port 20
---

## Allow DNS
`sudo ufw allow 53/tcp`
- [[Common Ports]] for DNS is port 53
---

# UFW Deny Ports
## Deny specific Ports (in)
`sudo ufw deny 25`
- will close tcp and udp 

### Deny multiple ports (in)
`ufw deny 1234:2345`
- deny ports in a range 
---
## Deny specific Ports (out)
will deny the access to specific ports
`sudo ufw deny out to <IP_or_hostname> port 80`
- will deny the access to *a certain web page* (http)

### Delete deny rules (out)
this will delete any rules from port 80, that deny access (tcp)
`sudo ufw delete deny out 80/tcp`
``

