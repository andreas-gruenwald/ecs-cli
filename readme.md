# AWS ECS related CLI Tools

This docker container provides an environment to access common 
AWS tools that are used in conjunction with AWS ECS, such as

- aws cli
- ecs-cli
- [AWS copilot](https://github.com/aws/copilot-cli)


## How it works

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
copilot -h
```
