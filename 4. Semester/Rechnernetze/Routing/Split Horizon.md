A router will not advertise a route back to the neighbor from which it learned that route
- **Benutzt um Schleifen zu vermeiden**
## Working method
- When a router receives a routing update from a neighboring router, it adds the route to its routing table, noting the neighbor as the next hop.
- Under split horizon, the **router will not send that same route information back to the neighbor who sent it**.
	- *Gebe Route nicht über den Weg bekannt, über den sie gelernt wurde*
- This avoids scenarios where routers keep passing the same route information back and forth, potentially causing incorrect or looping routes.


### Example 
- Router A advertises to Router B that it can reach Network X via a certain path.
- Router B updates its routing table with this information, noting Router A as the next hop for Network X.
- When Router B sends its own routing updates, it will not include Network X in the update sent to Router A, because it learned about Network X from Router A.


--- 

# Split Horizon mit Poisoned Reverse
Gebe Route über den Weg, über den sie gelernt wurde, mit Kosten „unendlich“ an