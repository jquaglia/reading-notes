# Class 18

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
| Serverless Functions | A serverless function is a programmatic function written by a software developer for a single purpose. It's then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier. |
| Cloud Storage | Cloud storage is a model of computer data storage in which the digital data is stored in logical pools, said to be on "the cloud". The physical storage spans multiple servers, and the physical environment is typically owned and managed by a hosting company. |
| CDN | A content delivery network, or content distribution network, is a geographically distributed network of proxy servers and their data centers. The goal is to provide high availability and performance by distributing the service spatially relative to end users. |

## AWS: API, Dynamo and Lambda

### Amazon API Gateway

What is Amazon API Gateway?

- Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

How does API Gateway work?

- API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends.

How does API Gateway integrate with other AWS services?

- Many AWS services support integration with Amazon API Gateway, including:

  - AWS Lambda: run Lambda functions to generate HTTP API responses.

  - AWS SNS: publish SNS notifications when an HTTP API endpoint is accessed.

  - Amazon Cognito: provide authentication and authorization for your HTTP APIs.

How API Gateway Works:

![diagram of API gateway](https://d1.awsstatic.com/serverless/New-API-GW-Diagram.c9fc9835d2a9aa00ef90d0ddc4c6402a2536de0d.png)

### __Dynamo DB__

Dynamo DB is a hosted NoSQL database offered by AWS.

- DynamoDB supports some of the world’s largest scale applications by providing consistent, single-digit millisecond response times at any scale.

- DynamoDB is serverless with no servers to provision, patch, or manage and no software to install, maintain, or operate.

- DynamoDB supports ACID transactions to enable you to build business-critical applications at scale.

### Dynamoose

Dynamoose is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familar.
