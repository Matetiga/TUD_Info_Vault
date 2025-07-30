```txt
sudo docker network create -d macvlan --subnet <network_IP> --gateway <router_IP> -o parent=<host_server_interface_name> <network_name>
```
- to find *host_server_interface_name* -> `ip addr` (in terminal) => <span style="color:#ffff00">enp2s0</span>

The containers will connect directly to the network (**to the switch**)
- They will have their own *Mac Address*
- Own *IP addresses* on the network 

### Network might not be able to have multiple Mac Addresses on one switch port 
- therefore `ping` to other devices **in the network is not possible**
Enable promiscuous mode in network interface
- `sudo ip link set <network_interface_name> promisc` -> might not work
- can be done in **Virtual Box**

---

## Add containers to Mac VLAN
`sudo docker run -itd --rm --network <network_name> --ip <own_IP> --name <container_name> <image_name>`
- **IP address should be specified by ourselves**

---
## Enables to Deploy a web server, without having to expose any ports 
`sudo docker run -itd --rm --network <network name> --ip <container_IP>  --name <container_name> <image_name>`