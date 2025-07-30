## Stop single containers
`docker stop container_id` / or name given to the docker 


---

## Stop all running containers
`docker stop $(docker ps -q)
- `docker ps -q` : lists all running **containers IDs**

---

### Stop containers in docker compose
**INSIDE THE DIRECTORY WHERE docker-compose.yml is located**
`docker compose down`