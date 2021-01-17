# Class 21

## Node.js

- Node.js is a JavaScript runtime built on Chrome's V8 JS engine

- Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google's V8 JS engine and libuv library

### Node is Built on Google Chrome's V8 JS Engine

V8 engine is the open-source JS engine that runs in Google Chrome and other chromium based browsers. (Ryan Dahl) took the V8 engine and enhanced it with various features, such as file system API, an HTTP library, and a number of operating system-related utility methods.

### Node.js has excellent support for modern JS

Node has excellent support for ES6 and beyond. You don't have to worry about compatibility issues!

### Introducing NPM

Node comes bundled with a package manager called npm. In addition to being _the_ package manager for JS, npm is also the world's largest software registry. There are over 1,000,000 packages of JS code available to download, with billions of downloads per week.

### What is Node.js used for

Node and npm are used for installing(via npm) and running(via Node) various build tools - designed to automate the process of developing a modern JS app.

### Node.js lets us run JS on the server

This was possible way back in 1994 and attempted by Netscape. Node.js is the first implementation to pick up any traction though.

### The Node.js execution model

- In very simplistic terms, when you connect to a traditional server, such as Apache, it will spawn a new thread to handle the request.

- In a language such as PHP or Ruby, any subsequent I/O operations (for example, interacting with a database) block the execution of your code until the operation has completed.

- That is, the server has to wait for the database lookup to complete before it can move on to processing the result. If new requests come in while this is happening, the server will spawn new threads to deal with them.

- This is potentially inefficient, as a large number of threads can cause a system to become sluggish — and, in the worst case, for the site to go down. The most common way to support more connections is to add more servers.

Node.js however is single-threaded. It's also __event-driven__, which means that everything that happens in Node is in reaction to an event. For example, when a new request comes in (one kind of event) the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. When the I/O operation has finished (another kind of event), the server will execute the callback and continue working on the original request. Under the hood, Node uses the libuv library to implement this asynchronous (that is, non-blocking) behavior.

Node's execution model causes the server very little overhead, and consequently it's capable of handling a large number of simultaneous connections. The traditional approach to scaling a Node app is to clone it and have the cloned instances share the workload. Node.js even has a built-in module to help you implement a cloning strategy on a single server.

[this image depicts Node's execution model](https://uploads.sitepoint.com/wp-content/uploads/2012/10/1516152673node_event_loop.png)

### Are there any Downsides?

- Node runs in a single thread does impose some limitations.

- Blocking I/O calls should be avoided, CPU-intensive operations should be handed off to a worker thread, and arrors should always be handled correctly for fear of crashing the entire process.

- Some devs also dislike the callback-based style of coding that JS imposes.(so much so that there’s even a site dedicated to the horrors of writing asynchronous JavaScript)

- With the arrival of native Promises, followed closely by async await, flow control in modern JS has become easier that it ever was.

### What kind of Apps is Node.js suited to?

Node is particularly suited to building applications that require some form of real-time interaction or collaboration - for example, chat sites or apps such as [CodeShare](https://codeshare.io/), where you can watch a document being edited live by someone else.

[back to README](README.md)
