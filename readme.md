# ECS CLI

Run the container:
```bash 
docker run -it agruenwald/ecs-cli bash
```
If you want to mount the cluster configuration files (docker-compose.yml, ecs-params.yml, es-container.env),
use 
```bash 
docker run -it -v ${PWD}:/ecs-cluster agruenwald/ecs-cli bash
```
 
Now you can run:
```bash    
    ews-cli -v
    aws help
```