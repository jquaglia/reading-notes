# Class 19

## Review, Research, and Discussion

1. What’s the difference between a FIFO and a standard queue?

    - FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers.

1. How can the server be assured a message was properly received?

    - The client can send an event/message right back to confirm every time a message is received.

1. What classic design pattern is best represented by event driven programming?

    - The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods

1. How do you test an event driven system?

    - You can write unit tests for just about anything. Also, just using different console.logs for different events that fire off is a good way to confirm functionality while building the app.

| Term      | Description |
| ----------- | ----------- |
|Severless API|using API Gateway you can create RESTful APIs that enable real-time two-way communication applications, API Gateway supports containerzied and serverless workloads as well as web applications|
|Triggers|an AWS Lambda resource or resource in another service that you configure to invoke your function in response to lifecycle events, external requests or on a schedule, a function can have multiple triggers|
|Dynamo vs Mongo|Mongo can be deployed anywhere, Dynamo is only available on AWS. Mongo is JSON based document store while Dynamo is limited key-value store with JSON support. Mongo is rich query language, Dynamo is key-value queries|
|Dynamoose vs Mongoose|Dynamoose is a DynamoDB API structured like Mongoose, lets us provide a schema and perform CRUD operations against a DynamoDB table, installed via node and configured based on role|

## SQS vs SNS

### SQS

- Entity Type: Queue (Similar to JMS)

- Message consumption: Pull Mechanism — Consumers poll and pull messages from SQS

- Use Case: Decoupling two applications and allowing parallel asynchronous processing

- Persistence: Messages are persisted for some (configurable) duration is no consumer available

- Consumer Type: All the consumers are supposed to be identical and hence process the messages in exact same way

- Sample applications: Jobs framework. Where the Jobs are submitted to SQS and the consumers at the other end can process the jobs asynchronously. And if the job frequency increases then the number of consumers can be increased for parallel processing

### SNS

- Entity Type: Topic (Pub/Sub system)

- Message consumption: Push Mechanism — SNS Pushes messages to consumers

- Use Case: Fanout — Meaning allowing same message to be processed in multiple ways

- Persistence: No persistence. Whichever consumer is present at the time of message arrival, get the message and the message is deleted. If no consumers available then the message is lost.

- Consumer Type: All the consumers are (supposed to be) processing the messages in different ways

- Sample applications: Image processing. If someone uploads an image to S3 then watermark that image, create a thumbnail and also send a ThankYou email. In that case S3 can send notification to SNS Topic and 3 consumers can be attached to SNS topic. 1st one watermarks the image, 2nd one creates a thumbnail and the 3rd one send a ThankYou email. All of them receiving the same message (image URL) and doing their corresponding processing in parallel.
