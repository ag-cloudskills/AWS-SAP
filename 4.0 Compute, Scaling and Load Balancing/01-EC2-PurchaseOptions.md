# Introduction to global and regional architecture

Flow of Traffic of an application ->WebTier(Loadblancer ,api gateway) -> Compute Tier ( EC2, containers, Lambda) 
Storage tier ( S3, EBS , EFS)
Caching layer(in-memory)
DB Tier
App Services

## EC2 Purchase options

- On demand EC2 ( short term, unknown workloads , no upfront cost, )

- Spot EC2 ( not reliable can be terminated, stateless applications, non time critical)

- Reserved Instances ( long time commitment)
  - Duration (1 year or 3 year)

  - upfront , partial upfront or no upfront

- Dedicated Host ( like physical machine assigned , pay on host not on number of instances, software license based on cores and socket) . host affinity , not shared. Capacity management is not required

- Dedicated Instances - not shared and don't pay for host.extra fees  , one off hourly fees + dedicated instance. FOr compliance and regulatory requirements

- Scheduled Reserved Instances ( minimum 1200 hours and 1 year) , required for only specific hours

- Capacity reservations ( no billing benefit)
  - regional reservations
  - Zonal reservations
  - On-demand capacity reservations

- Savings plan hourly spend
  - compute $ amount
  - ec2 savings plan ( instance family)
