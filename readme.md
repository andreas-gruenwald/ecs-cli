# AWS and ECS related CLI Deployment Tools

This docker container provides an environment to access common 
AWS tools that are used in conjunction with AWS ECS, such as

- [aws cli](https://awscli.amazonaws.com/v2/documentation/api/latest/reference/index.html) for any kind of AWS service operation 
- [ecs-cli](https://github.com/aws/amazon-ecs-cli) for deployment of ECS services based on a local development
- [AWS copilot](https://github.com/aws/copilot-cli) for deploying ECS fargate infrastructures (successor of ecs-clir)
- [AWS Nuke](https://github.com/rebuy-de/aws-nuke) for resetting infrastructure

## How it works

Run the container:
```bash 
docker run -it agruenwald/ecs-cli bash
```
If you want to mount the cluster configuration files (docker-compose.yml, ecs-params.yml, es-container.env),
use 
```bash 
docker run -it -v ${PWD}:/ecs-cluster  -v /var/run/docker.sock:/var/run/docker.sock agruenwald/ecs-cli bash
```
 
Now you can run:
```bash    
ews-cli -v
aws help
copilot -h
aws-nuke -h
```
