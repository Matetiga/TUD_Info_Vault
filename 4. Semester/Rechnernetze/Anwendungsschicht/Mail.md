## MIME - Multipurpose Internet Mail Extensions
- **Port 25**
neue Header: MIME-Version, Content-Description, Content-Id, Content-
Transfer-Encoding, Content-Type
- Mögliche Types: text, image. audio, video, application 
- Codierung von Binärdaten in Base64:
	- jeweils 6 Bit als ASCII-Zeichen übertragen – 33% Overhead
- Quoted Printable Coding:
	- Nicht-ASCII-Zeichen werden mit „=*XX*“ codiert (*XX* = 2 hexadezimale Ziffern)

## Email Infrastruktur
- Protokolle können via Transport Layer Security (TLS) abgesichert werden
![[Pasted image 20250703115057.png]]
### SMTP - Simple Mail Transport Protocol
- zuverlässiger Nachrichtentransfer
- *Keine Authentifizierung* (**Anfällig für Spam**)
- **Übertragung in Klartext**
- Suche nach Ziel-SMTP-Server über DNS (MX Record)
- Weiterleitung und Auslieferung an Ziel-Serve
![[Pasted image 20250703114735.png]]

### POP3 (Post Office Protocol)
- Abruf aller E-Mails und Attachments (authentisiert)
- Herunterladen der E-Mail → Entlastung des Servers
### IMAP (Internet Message Access Protocol):
- selektiver Abruf (authentisiert)
- E-Mail bleibt auf Server → Abrufen durch mehrere Clients möglich

---
## ESMTP
- Extended Simple Mail Transfer Protocoll
![[Pasted image 20250703115631.png]]