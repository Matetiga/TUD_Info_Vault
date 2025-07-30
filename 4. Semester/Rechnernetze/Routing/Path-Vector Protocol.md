is a type of routing protocol used in computer networks to exchange and maintain routing information between routers, **particularly for inter-domain routing**
- Uses a **Routing Table** with entries for destinations network prefixes
- Each Route is **associated with a path** (*of nodes or AS*) to reach a certain destination
- Path Information is shared with neighbor routers 


### Prevents Routing Loops
If a router receives a route advertisement containing its own identifier (e.g., its AS number in BGP), it discards the route, as this indicates a loop