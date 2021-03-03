# Class 13

## Review, Research, and Discussion

1. What does it mean that web sockets are bidirectional? Why is this useful?

   - Bidirectional means data flows in both directions, whereas Unidirectional means data flows in only one direction. A socket is created as a bidirectional resource (capable of both sending and receiving), even if it is only used in a unidirectional manner in code. This lets you send and receive data over the same channel.

1. Does socket.io use HTTP? Why?

    - The client will try to establish a WebSocket connection if possible, and will fall back on HTTP long polling if not.

1. What happens when a client emits an event?

    - the server is already listening for the event because the client is connected.

1. What happens when a server emits an event?

    - the client listening responds to the event.

1. What happens if a client “misses” an event?

    - Unhandled messages are just ignored. It's just like when an event occurs and there are no event listeners for that event. The socket receives the msg and doesn't find a handler for it so nothing happens with it.

1. How can we mitigate this?

    - You could avoid missing messages by always having the handlers installed and then deciding in the handlers (based on other state) whether to do anything with the message or not.

| Term      | Description |
| ----------- | ----------- |
|Socket|When you send bytes from a buffer with a normal TCP socket, the send function returns the number of bytes of the buffer that were sent. If it is a non-blocking socket or a non-blocking send then the number of bytes sent may be less than the size of the buffer.|
|Web Socket|With WebSockets, the data that is passed to the send method is always either sent as a whole "message" or not at all. Also, browser WebSocket implementations do not block on the send call.|
|Socket.io|Socket.IO is a JavaScript library for realtime web applications. It enables realtime, bi-directional communication between web clients and servers. It has two parts: a client-side library that runs in the browser, and a server-side library for Node.js. Both components have a nearly identical API.|
|Client|The WebSocket Client origin reads data from a WebSocket server endpoint.|
|Server||
|OSI Model|The Open Systems Interconnection model is a conceptual model that characterises and standardises the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology.|
|TCP Model|The Internet protocol suite is the conceptual model and set of communications protocols used in the Internet and similar computer networks. It is commonly known as TCP/IP because the foundational protocols in the suite are the Transmission Control Protocol and the Internet Protocol|
|TCP|The Transmission Control Protocol is one of the main protocols of the Internet protocol suite. It originated in the initial network implementation in which it complemented the Internet Protocol. Therefore, the entire suite is commonly referred to as TCP/IP.|
|UDP|n computer networking, the User Datagram Protocol is one of the core members of the Internet protocol suite. |
|Packets|In telecommunications and computer networking, a network packet is a formatted unit of data carried by a packet-switched network. A packet consists of control information and user data; the latter is also known as the payload. Control information provides data for delivering the payload.|

## Sockets

### Rooms

- A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients

- rooms are a server-only concept

- You can call join to subscribe the socket to a given channel

- You can call join to subscribe the socket to a given channel

- You can emit to several rooms at the same time

- In that case, a union is performed: every socket that is at least in one of the rooms will get the event once (even if the socket is in two or more rooms).

- You can also broadcast to a room from a given socket

- In that case, every socket in the room excluding the sender will get the event.

### Default Room

- Each Socket in Socket.IO is identified by a random, unguessable, unique identifier Socket#id. For your convenience, each socket automatically joins a room identified by its own id.

- This makes it easy to implement private messages

[back to README](../README.md)