Here are some ways to control where services run:

1. **Node Role**: You can constrain services to run **only on manager or worker** nodes.
2. **Node Labels**: You can add custom labels to nodes and then use these for placement.
3. **Node ID or Name**: You can specify exact nodes by their ID or name.
4. Engine Labels: These are labels that come from the Docker engine itself

### Rules
- Constraints are strict rules. If they can't be met, the service won't deploy.
- Preferences are best-effort. Swarm will try to meet them but may ignore them if necessary

### Example 
###### Web 
- runs only in worker nodes
###### database
- runs only in nodes with label -> *database*
- `docker node update --label-add type=database <node-id>`
###### Monitoring 
- runs only in a specific node called -> *monitoring-node*
```yml
version: '3'

services:
  web:
    image: nginx:latest
    deploy:
      placement:
        constraints:
          - node.role == worker

  database:
    image: postgres:latest
    deploy:
      placement:
        constraints:
          - node.labels.type == database

  cache:
    image: redis:latest
    deploy:
      placement:
        preferences:
          - spread: node.labels.zone

  monitoring:
    image: grafana/grafana:latest
    deploy:
      placement:
        constraints:
          - node.hostname == monitoring-node

networks:
  default:
    driver: overlay
```- Constraints are strict rules. If they can't be met, the service won't deploy.
- Preferences are best-effort. Swarm will try to meet them but may ignore them if necessary