A reverse Proxy can distribute the incoming traffic across multiple backend servers
- can handle SSL encryption 
- helps distribute incoming traffic
#### Hides the IP of the backends servers

---
## Work method
- 1. Client tries to access a web page
- 2. Request goes to the reverse proxy instead of directly going to a one backendserver of the web page
- 3. Reverse Proxy determines the best suited server (least busy) and forwards the request to that server
- 4. Server response goes back to the reverse proxy
- 5. Reverse proxy responds the client 

---

### Examples 
- Nginx
- Apache HTTP Server