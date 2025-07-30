## Definition
Switching is the process of transferring Data from a device to another in a network or from one network to  another 

---
## Packet Switching 
Data is **divided into smaller Packets** and transmitted over the network
- Each Packet contains *information about the source and the address*
- Packets may *take different routes to their destination*
### Advantages 
- **Efficient Use Of Bandwidth** : Bandwidth is shared between multiple users. Resources are only allocated when needed
- **Flexible** : can handle a wide range a data rates and packages sizes
- **Scalable** : 
- **Lower Cost**
### Disadvantages
- Schwer vohersagbare Leistung
- Requires Buffers
- Packet overhead

---
## Circuit Switching 
A **communication Path** (or *circuit*) is established between two devices before Data transmission begins
- Commonly used in voice communication because of throughput without additional delay
### Advantages
- **Guaranteed Bandwidth**: Provides a dedicated path for communication ensuring total coverage of bandwidth for the duration of the call
- **Low Latency**: because the path is predetermined. There is no need to establish a connection for each package 
- **Predictable Performance**: there is no competition for resources (bandwidth is reserved)
### Disadvantages
- **Inefficient use of Bandwidth**: Bandwidth is reserved even when no data is being transmitted 
- **Limited scalability**
- **High costs**

---