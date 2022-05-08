# SNS,SQS
## simple notification service

- Pub/Sub
- Public aws service
- 256k payload
- SNS topics
- Subscribers can be https, email , sqs , mobile puch , sms messages and lambda
- Can be used for notifications
- Filter can be used
- Fanout can be used for multiple SQS queues
- Delivery status
- Delivery retries
- HA and scalable ( managed service by AWS)
- Server side encryption
- Cross account via topic policy

## Simple queue Service

- fully managed service
- FIFO( once delivery and also in order, low performance, 3000 messages per second) or standard queue ( at least once - no order, high performance)
- message size - 256 KB
- visibility timeout ( message is hidden) and reappears if message is not deleted and available for reprocessing , can be 0 sec to 12 hours, default 30sec
- dead letter queue can be used for problem messages, receive comaxreceivecount
- ASG can work on SQS length
- billed based on requests
- short vs long polling
- encryption at rest ( KMS)
- queue policy
- SQS Extended client library  message greater than 256KB , allow large payloads and store the message in s3 and store links in message - ( SQS +s3)
- SQS delay queues- delay seconds , messages are added in queue and will be invisible , 0 -15 mins ( not supported on FIFO), automatically hidden without processing

## Amazon MQ

- open source message broker
- JMS API support, AMQP, MQTT, openwire and Stomp
- one-to-one or one-to-Many
- private service
- 














