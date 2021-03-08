# Class 16

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
|Server|In computing, a server is a piece of computer hardware or software that provides functionality for other programs or devices, called "clients". This architecture is called the client–server model.|
|Pub/Sub|In software architecture, publish–subscribe is a messaging pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers, called subscribers, but instead categorize published messages into classes without knowledge of which subscribers, if any, there may be. Similarly, subscribers express interest in one or more classes and only receive messages that are of interest, without knowledge of which publishers, if any, there are.|
|WRRC|The web is a cycle of requests and responses that flow between clients and servers. Any computer making a request is a client and any computer sending a response is a server. (essentially)|
