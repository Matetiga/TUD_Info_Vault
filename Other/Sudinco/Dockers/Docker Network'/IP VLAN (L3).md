Makes the containers connect directly to the Host
- no **broadcast traffic** 
- layer 3
- **host becomes a router**
- perfect for Isolation layer 3 
	- to be able to connect to this network and to the containers inside => you should go through the host 
	- access the router
	- no need to specify gateway
	- separated networks can talk to each other

`sudo docker network create -d ipvlan --subnet <network_IP> -o parent=<host_server_interface_name> -o ipvlan_mode=l3 --subnet <network_IP> <network_name>`
- creates two networks that use the same physical interface

### Add containers to the network 
`sudo docker run -itd --rm --network <network_name> --ip <ip_for_container>`