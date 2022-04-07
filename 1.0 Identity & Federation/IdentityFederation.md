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
  - IAM policies variables and tags

- IAM role vs Resource based policy
  - when user/application/service assume a role , original permissions are given up
  - when using a resorurce based policy, principle does not give up permission
  - Resource based policy specifies which pronicple will be accessing the resource

- IAM permission Boundries
  - it defines the boundry of the resource over the IAM policy