# Class 17

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
| Server Instances | An instance is a single copy of the software running on a single physical or virtual server. If you run two copies of the software on the same physical or virtual server, that counts as two instances. When you run two copies of the software on two different physical or virtual servers, that also counts as two instances. |
| Containers | A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. |
| Cloud Services | Cloud computing is the on-demand availability of computer system resources, especially data storage and computing power, without direct active management by the user. The term is generally used to describe data centers available to many users over the Internet |
| Cloud Architecture | Cloud architecture is the way technology components combine to build a cloud, in which resources are pooled through virtualization technology and shared across a network. ... A front-end platform (the client or device used to access the cloud) A back-end platform (servers and storage) A cloud-based delivery model. |
| AWS | Amazon Web Services is a subsidiary of Amazon providing on-demand cloud computing platforms and APIs to individuals, companies, and governments, on a metered pay-as-you-go basis.  |
| EC2/Beanstalk vs Heroku | Elastic Compute Cloud (EC2) is an Infrastructure as a Service product.(IaaS) Heroku is a _Platform_ as a Service (PaaS) |

## AWS: S3 and Lambda

### S3

- Amazon Simple Storage Service is a n object storage service that offers scalability, data availability, security and performance.

- Scale your storage resources up and down to meet fluctuating demands, without upfront investments or resource procurement cycles.

- Save costs without sacrificing performance by storing data across the S3 Storage Classes, which support different data access levels at corresponding rates.

- Store your data in Amazon S3 and secure it from unauthorized access with encryption features and access management tools.

- S3 gives you robust capabilities to manage access, cost, replication, and data protection.

- Run big data analytics across your S3 objects (and other data sets in AWS) with our query-in-place services.

- Store and protect your data in Amazon S3 by working with a partner from the AWS Partner Network (APN) — the largest community of technology and consulting cloud services providers.

### AWS Lambda

AWS Lambda is a serverless compute service that lets you run code without provisioning or managing servers, creating workload-aware cluster schaling logic, maintaining event integrations, or managing runtimes.

some benefits:

- No servers to manage

- Continuous scaling

- Cost optimized with millisecond metering

- Consistent performance at any scale

How does AWS Lambda work?

- Each Lambda function runs in its own container.

- When a function is created, Lambda packages it into a new container and then executes that container on a multi-tenant cluster of machines managed by AWS.

- Before the functions start running, each function’s container is allocated its necessary RAM and CPU capacity.

- Once the functions finish running, the RAM allocated at the beginning is multiplied by the amount of time the function spent running.

- The customers then get charged based on the allocated memory and the amount of run time the function took to complete.

### CDN

- A Content Delivery Network is a geographically distributed group of servers that work together to provide fast delivery of Internet content.

- CDNs work through servers nerest to the website visitor respond to the request.

- Employing a CDN doesn’t only speed up the delivery of Internet content, it helps protect your website against certain forms of cyber attacks, such as Denial of Service attacks.
