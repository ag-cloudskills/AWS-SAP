# IAM
- User access ( long term credentials) and permissions can be given at group level for the users
- STS is used for giving short term credentials 
    - EC2 instance role ( attached to EC2)
    - Service role - API gateway
    - Cross Account role
- Policies
    - AWS managed
    - Customer Managed
    - Inline polices 
    - resource specific policy ( DynamodDB , S3)
    - Combination of allow and not allow can be used , if any specific actions needs to be allowed under one resource 
    - condition operators can be uses for the condition 


