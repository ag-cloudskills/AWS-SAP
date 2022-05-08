# ECS concepts

- container definition (images, ports)
- task definition ( cpu, memory , network, compatibility ( ec2 or fargate), task role( iam role)to interact with aws resources )
- ECS service definition - capacity and resilience, how many copies of tasks,restart

## ECS cluster types

### EC2 Mode

- Scheduling and orchestration, clustermanager, placementengine
- ECS cluster is created within VPC
- ASG is used for horizontal scaling 
- if control of EC2 is needed

### Fargate

- Scheduling and orchestration, clustermanager, placementengine 
- serverless method
- shared infrastructure
- IP is given from VPC , tasks and services are running in shared platform and injected in VPC ( interface is given from VPC)