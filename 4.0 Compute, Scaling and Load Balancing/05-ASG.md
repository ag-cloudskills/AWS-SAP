# Auto Scaling group

- scaling as well as self-healing 
- launch template of configurations
- minimum, desired and maximum

## Scaling policies 

- manual
- Scheduled scaling
- Dynamic 
  - Simple - metrics
  - Stepped scaling
  - target tracking  ( average metrics)

- Cool down periods to avoid rapid scaling

ASG + LB ->  ASG can use LB health check rather than EC2 status check

- launch and terminate
- AddToLoadBalancer
- AlarmNotification
- AZ rebalance
- HealthCHeck
- Replace Unhealthy
- Scheduled Actions
- Standby

## Lifecyle hooks

- custome actions
- instance are paused within flow
- completelifecycleaction
- eventbridge, sns integration

Scale out event( lifecycle hook)

Pending --> Pending: wait  --> Pending: proceed ---> INService 

Scale in event ( lifecyele hook)

Terminating --> terminating: wait --> terminating: proceed --> Terminated
