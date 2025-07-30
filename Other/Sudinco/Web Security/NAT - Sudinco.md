To **allow multiple devices** (with their own private IP) to access the internet with a **single public key**
- one or more private IPs are translated into one or more public IPs 
- masks the port number of the host
- **NAT keeps track** of the internal device (**private IP**) which made the request
	- **response** received at the **public IP**
	- **NAT forwards the response** to the device (**private IP**)