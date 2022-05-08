# AWS Lambda

- short running and executed in a runtime environment 
- memory( 128-10240MB) is allocated for a function.
- billed for a duration of function
- lambda is stateless
- /tmp as 512MB storage is provided
- function can run upto 15 minutes
- execution role ( iam role) to interact with other AWS services
- serverless applications ( s3, api gateway, lambda)
- Use cases- file processing ( s3, s3 events, lambda,)
- Db triggers ( dynamodb, streams, lambda)
- serverless cron ( eventbridge/cweevnts + lambda)
- realtime stream data processing ( kinesis + lambda)

- support both public and private networking
- vpc based networking - an interface is assigned initially 