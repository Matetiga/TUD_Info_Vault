## L2 East 
### S1
 ```txt
158.71.100.3 
```
### S2
```txt
158.71.100.4
```

### A_NETD
```txt 
158.71.200.3
```

### A_HPC
```txt
158.71.200.5
```

### S_HPC
```txt
158.71.200.6
```


--- 
## Problems 
Wenn man `A_NETD:~# `tcpdump -e -n 'arp'`` nutzt, dann kommen die Packeten in *A_HCP*, aber es kommt keine Response
- Wenn man dasselbe macht, aber ohne Interface zu spezifizieren `A_NETD:~# arping -b 158.71.200.5`, dann bekommt *S_HPC* die Packeten **und schickt Responces zurück**
- dasselbe für `A_NETD:~# arping -I ssh -b 158.71.100.4 `
Keine Response mit `A_NETD:~# arping -I 71-S1 -b 158.71.100.4 `

#### Questions 
- Was ist der Sinn von `<destination>` beim `arping`, 
- Wieso muss man auch ein `destination` angeben, wenn man broadcast macht `-b`

```txt
tcpdump -e -n 'arp'
```
