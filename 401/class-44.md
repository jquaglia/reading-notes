# Class 14

## Review, Research, and Discussion

1. What’s the difference between a FIFO and a standard queue?

    - Standard queues provide at-least-once delivery, which means that each message is delivered at least once. FIFO queues provide exactly-once processing, which means that each message is delivered once and remains available until a consumer processes it and deletes it.

1. How can the server be assured a message was properly received?

    - It receives something back from the client (confirmation)

1. What classic design pattern is best represented by event driven programming?

    - The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods

1. How do you test an event driven system?

    - `npm install jest` and write some unit tests or use console logs

| Term      | Description |
| ----------- | ----------- |
|FIFO Queue| a method for organising the manipulation of a data structure – often, specifically a data buffer – where the oldest (first) entry, or 'head' of the queue, is processed first.|
|Pub/Sub|In software architecture, publish–subscribe is a messaging pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers, called subscribers, but instead categorize published messages into classes without knowledge of which subscribers, if any, there may be.|

[back to README](../README.md)
