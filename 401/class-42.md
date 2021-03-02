# Class 12

## Review, Research, and Discussion

1. What is the benefit of transforming data into packets?

    - It is well suited to data transmission, as it allows networks to adapt to changing conditions quickly. For example, if one of the network's routers fails, packets can be automatically re-routed to avoid that device. It also makes for scalable data networks, as it allows many users to transmit data at the same time.

1. UDP is often refereed to as a connectionless protocol. Why is this?

    - UDP is a connectionless protocol. No connection needs to be established between the source and destination before you transmit data. UDP does not have a mechanism to make sure that the payload is not corrupted. As a result, the application must take care of data integrity all by itself.

1. Can a socket server application have multiple socket connections?

    - When a server's processes listening to a port that means multiple sockets can simultaneously connect and communicate with the same server-process. ... Note that irrespective of the server's type a server can/should always uses the same initial socket to respond back (no need to allocate another server-port).

1. Can a socket connection application be connected to multiple socket servers?

    - If your program is a client to multiple servers, use one socket per server. You don't need bind for a client socket at all, just connect . I think you are using TCP socket( aren't you?). ... Then reuse port is not so important because your application is a client application, which is the part the start the connection.

1. Can an application be both a socket server and a socket connection?

    - Yes, you have to make sure that it doesn't use the same port at the same time though.

| Term      | Description |
| ----------- | ----------- |
| Observer Pattern | The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods. |
| Listener | An event listener is a procedure or function in a computer program that waits for an event to occur. |
| Event Handler | In programming and software design, an event is an action or occurrence recognized by software, often originating asynchronously from the external environment, that may be handled by the software. Computer events can be generated or triggered by the system, by the user, or in other ways. |
| Event Driven Programming | In computer programming, event-driven programming is a programming paradigm in which the flow of the program is determined by events such as user actions, sensor outputs, or message passing from other programs or threads. |
| Event Loop | In computer science, the event loop is a programming construct or design pattern that waits for and dispatches events or messages in a program. The event loop works by making a request to some internal or external "event provider", then calls the relevant event handler. |
| Event Queue | A queue stores a series of notifications or requests in first-in, first-out order. Sending a notification enqueues the request and returns. |
| Call Stack | In computer science, a call stack is a stack data structure that stores information about the active subroutines of a computer program. |
| Emit/Raise/Trigger | The EventEmitter is a module that facilitates communication/interaction between objects in Node. It basically is puts out the signal for other events to fire off. |
| Subscribe | In software architecture, publish–subscribe is a messaging pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers, called subscribers, but instead categorize published messages into classes without knowledge of which subscribers, if any, there may be. Similarly, subscribers express interest in one or more classes and only receive messages that are of interest, without knowledge of which publishers, if any, there are. |
| database | A database is an organized collection of data, generally stored and accessed electronically from a computer system. Where databases are more complex they are often developed using formal design and modeling techniques. |

## Socket

- Websocket is a communications protocol, providing full duplex communication channels over a single TCP connection.

- Socket.IO is a library which enables real-time and full duplex communication between the Client and the Web servers.

- It uses the websocket protocol to provide the interface. It is divided into two parts, both WebSocket vs Socket.io are event drivenm libraries

  - Client Side: it is the library that runs inside the browser

  - Server Side it is the library for Node.js

### WebSocket

- WebSocket helps in real-time communication between the Client and the web server.

- This protocol helps in transforming to cross-platform in a real time world between the server and the client.

- This also enables the business around the world for real-time web application to enhance and to increase the feasibility.

- The major advantage it stands over an HTTP connection that it provides full duplex communication.

- It provides the full duplex communication which helps in persisting the connection established between the Client and the Web Server.

- It also lives up to the standards and provides the accuracy and efficiency stream events to and from with negligible latency.

- WebSocket removes the overhead and reduce complexity.

- It makes real-time communication effortless and efficient.

### Socket.IO

- It helps in broadcasting to multiple sockets at a time and handles the connection transparently.

- It works on all platform, server or device ensuring the equality, reliability, and speed.

- It automatically upgrades the requirement to WebSocket if needed.

- It is a custom real-time transport protocol implementation on top of other protocols.

- It requires both libraries to be used Client side as well as a server-side library.

- IO works on work-based events. there are some reserved events which can be accessed using the Socket on server side like Connect, message, Disconnect, Ping and Reconnect.

- There are some Client based reserved events like Connect, connect- error, connect-timeout and Reconnect etc.

- I handle all the degradation of your technical alternatives to get full duplex communication in real time.

- It also handles the various support level and the inconsistencies from the browser.

- It also gives the additional feature room support for basic publish infrastructure and thinks like automatic reconnect.

- Currently, AFAIK is the most used one and easier to help with vanilla web sockets.

[back to README](../README.md)
