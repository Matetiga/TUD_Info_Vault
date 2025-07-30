
```txt
c3bf44901bf86daa
```


``` txt
ssh -p 2071 root@internet.netd.cs.tu-dresden.de
```


```txt
router# conf t
router(config)# route-map ACCEPT_ALL permit 10
router(config-route-map)#

router(config)# router bgp 71
router(config-router)# neighbor <IP_andere_gruppe> remote-as <AS_ID_Andere_GR>
router(config-router)# neighbor <IP_andere_gruppe> route-map ACCEPT_ALL in
router(config-router)# neighbor <IP_andere_gruppe> route-map ACCEPT_ALL out
HAM_router(config-router)# neighbor <IP_andere_gruppe> next-hop-self

// Dann muss man innerhalb das Interface jedes Router die abgesprochene IP-Address schreiben 
router# conf t
router(config)# interface <Interface_NAME> // es muss so z.B. heißen ext_72_HAM  
router(config)# ip address <unsere_Vereinbarte_IP>
// um die konfigurierte IP-address zu löschen: router(config)# no ip address <IP> 

router(config)# ip route 71.0.0.0/8 Null0

HAM_router# conf t
HAM_router(config)# router bgp 71
HAM_router(config-router)# network 71.0.0.0/8

```




>[!Important]
>The matching behavior of `_` may be unexpected! It works as follows: `_` matches whitespace and the start of the path, but _not_ end the of the path. Additionally, if you want to match whitespace _or_ the end of the path, you need to use the expression `($|_)`. For some reason, `(_|$)` _does not work_; be careful with the order of the symbols.



- Community 1: für Kunden 
- Community 2: für alles andere
- 71:100 Präfix für Kunden 
- 71:200 Präfix für Peers 
- 71:99 Interne Präfix 

### Important 
Be careful not to use a route map with a low sequence number and no match part. This route map would match everything, preventing any other route map from being evaluated. **As a rule of thumb, the lower the sequence number of your route map, the more specific the match part should be**
>[!Question]
>Ist es dann richtig, dass verschiedene `route-maps` denselben Sequenz-Number haben?


>[!Question
>Should the route-map use this kind of logic for the Prefixes that are on our SAME_REGION
```txt
if (prefix == 1.0.0.0/8) AND (community == 15:100):
    set local-preference 1000
elif (prefix == 1.0.0.0/8):
    set local-preference 2000
else:
    deny
```





## Changes 
27.06
-  Neue route-map : DENY_SAME_REGION mit deny 10
	- gemacht, so dass die Pfade von SAME_REGION invertiert werden 
	- kein route-map DENY_SAME_REGION mit permit 10, da route-map IN_FROM_IXP permit 20 gibt 
	- aber dies hier konnte falsch sein, da alle anderen Routen mit 71:200 (Peers)

- `set local-preferences ...` würde für jede Beziehung gesetzt
	- 100 für Provider 
	- 200 für Peer
	- 300 für Kunde
- AS 64 is now reachable with valid path
```txt 
route-map EXPORT_TO_CUSTOMER permit 5
 match ip address prefix-list MY_PREFIXES
 set community 71:99 additive
exit
!
route-map EXPORT_TO_CUSTOMER permit 10
 match community 1
exit

--> verändert zu 
route-map EXPORT_TO_CUSTOMER permit 10
// somit wird einfach alles geschickt 
// dasselbe in ZRH
// es kann sein das nach "route-map EXPORT_TO_CUSTOMER permit 5" ein impliziertes deny all gab, und somit würden alle andere Pfade bevor "route-map EXPORT_TO_CUSTOMER permit 10" verworfen

```


## Questions 
>[!Question]
>Wieso in DRS wird nicht die `community 1` in OUT_TO_IXP weiter gegeben

>[!Question]
>Is it our problem that the other ASes reach our AS with an invalid path 

