
Will prevent containers to have their own Mac addresses
- which can cause Problems like [[Mac VLAN]] and the **promiscuous** characteristic (only one Mac Address per port) 

#### Containers will share Mac Addresses with their host and <span style="color:#ffff00">keep a own IP Adress</span> 

---

### Creating a IP VLAN
`sudo docker network create -d ipvlan --subnet <network_IP> --gateway <router_IP> -o parent=<host_server_interface_name> <network_name>`

#### Attaching containers to IP VLAN
`sudo docker run -itd --rm --network <network_name> --ip <own_IP> --name <image_name>`
- we should **specify the IP Address**