## Default Free Zone 
Refers to the part of the internet, where routers do not rely on a default route to forward packets
- These routers maintain a **global [[BGP]] routing table** (containing all routing information to reach any publicly routable IP address prefix)
- Routers in the DFZ use BGP attributes (e.g., *AS path, local preference*) to select the best path to a destination. This allows for **fine-tuned routing decisions** based on performance, cost, or policy, rather than blindly forwarding traffic to a default gateway.


### Relationship with BGP
- <span style="color:#ffff00">BGP is the Protocol that enables DFZ</span>
 It exists because BGP allows routers to exchange and maintain the full set of internet routes, enabling the core of the internet to operate without default routes.