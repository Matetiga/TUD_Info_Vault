## Append / Insert new rules
- **Append** -> new rule at the end of the rules 
- **Insert** -> new rule at the beginning of the rules 

Rules are checked in order. If *one rule allows a package*, and it is before *another rule that drops* the same package -> that **package will be accepted** 

---
`-I` -> *Insert*
`-A` -> *Append*
- `PROTOCOL` -> udp/tcp ...
- `entry/exit INTERFACE` -> see with `ip a` **in terminal**
```txt
iptables -I <CHAIN> <-p PROTOCOL> <--sport START_PORT>/<--dport DESTINY PORT> <-s ORIGIN-IP>/<-d DESINY-IP> <-i ENTRY INTERFACE> <-o EXIT INTERFACE> <-j ACCEPT | DROP>

```


## It must be done for INPUT and OUTPUT
- if only a input rule is added, the device is **able to send a message** but the **response is thrown** 
### Rule for Ping
```txt
iptables -A OUTPUT -o enp0s3 -p icmp -j ACCEPT
iptables -A INPUT -i enp0s3 -p icmp -j ACCEPT
```

### Loopback interface \
```text 
iptables -I OUTPUT 1 -o lo -j ACCEPT
iptables -I INPUT 1 -i lo -j ACCEPT
```