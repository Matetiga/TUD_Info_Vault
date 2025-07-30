## Look for ESTABLISHED connections
```txt
sudo lsof -i -P -n | grep ESTABLISHED
```


---

## List ports in use
`ss -tulna`

`sudo ss -tulpn`

`sudo ss -ltnp`
- for a more concise and relevant information 

`sudo lsof -i :<port_number>`

---
