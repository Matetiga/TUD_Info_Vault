## For Multi-Host connectivity
`docker network create -d overlay --atachable <net_name>`
- `--atachable` Flag is used so individual containers (**not services**) can connect to the network