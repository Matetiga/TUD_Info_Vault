### Create 
`docker service create --name <service_name> --replicas <number_of_replicas> -p <host_port>:<container_port> <image_name>`

#### scale number of replicas
`docker service scale <service_ID>=<numberof_replicas>`


If you want to connect the service to the somenetwork after it was created, update the service
```
docker service update --network-add somenetwork someservice
```

