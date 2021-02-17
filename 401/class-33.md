# Class 03

## Review, Research, and Discussion

1. _Name 3 real world use cases where you’d want to change the request with custom middleware_

    1. Optimization of existing applications

        - Middleware can help developers transform legacy monolithic applications into cloud-native applications, keeping valuable tools active with better performance and more portability.

    1. Intelligent business automation

        - Middleware can help developers, architects, IT, and business leaders automate manual decisions. Automation can improve resource management and overall efficiency.

    1. Data streaming

        - While APIs are one way to share data between applications, another approach is asynchronous data streaming. This replicates a data set in an intermediate store, where the data can be shared among multiple applications. One popular open source middleware tool for real-time data streaming is Apache Kafka.

1. _True or false: The route handler is middleware?_

    - False

1. _In what ways can a middleware function end the process and send data to the browser?_

    - Can use `next()` to pass control to the next middleware function

    - Can use `response` parameter to send data

1. _At what point in the request lifecycle can you “inject” middleware?_

    - Middleware can be 'injected' in between the request and the response of a route

1. _What can cause express to error with “Request headers sent twice, cannot start a second response”_

    - This happens after you have already sent response and try to send it again

| Term      | Description |
| ----------- | ----------- |
| Middleware              |Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle.|
| Request Object          |The request object allows you to submit a POST or GET request to an URL. Essentially it provides a way to make REST API requests to another URL.|
| Response Object         |It is the object which communicates between the server and the output which is sent to the client.|
| Application Middleware  |Middleware that changes the function of the application|
| Routing Middleware      |Middleware that works in between the routes (error handling / validation) |
| Test Driven Development |Test-driven development is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases.|
| Behavioral Testing      |BLACK BOX TESTING, also known as Behavioral Testing, is a software testing method in which the internal structure/design/implementation of the item being tested is not known to the tester. These tests can be functional or non-functional, though usually functional.|

## Express REST API

### Defining classes

- classes are "special functions", and just as you can define function expressions and declarations, the class syntax has two components:

    1. class expressions

    1. class declarations

- to declare a class, you use the `class` keyword with the name of the class("Rectangle" here):

    ```javascript
    class Rectangle {
      constructor(height, width) {
        this.height = height;
        this.width = width;
      }
  }

    ```

#### Hoisting

- an important difference between function declarations and class declarations is that function declarations are `hoisted` and class declarations are not.

- You first need to declare your class and then access it, otherwise code like the following will throw a `ReferenceError`:

```javascript

const p = new Rectangle(); // ReferenceError

class Rectangle {}

```

#### Class Expressions

- a class expression is another way to define a class. Class expressions can be named or unnamed. The name given to a named class expression is local to the class's body. (it can be retrieved through the class's (not an instance's) `name` property, though)

```javascript

// unnamed
let Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name);
// output: "Rectangle"

// named
let Rectangle = class Rectangle2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name);
// output: "Rectangle2"

```

## Express Routing

- Routing refers to how an application's endpoints (URIs) respond to client requests.

- A route method is derived from one of the HTTP methods and is attached to an instance of the express class

- Route paths, in combination with a request method, define the endpoints at which requests can be made.

- Route parameters are named URL segments that are used to capture the values specified at their position in the URL.

- Route handlers - you can provide multiple callback functions that behave like middleware to handle a request.

- Response methods on the response object in the following list can send a response to the client, and terminate the request-response cycle:

  - `res.download()`, `res.end()`, `res.json()`, `res.jsonp()`, `res.redirect()`, `res.render()`, `res.send()`, `res.sendFile()`, `res.sendStatus()`

- `app.route()` you can create chainable route handlers for a route path by using this

- Use the `express.Router` class to create modular, mountable route handlers. A router instance is a complete middleware and routing system; for this reason, it is often referred to as a 'mini-app'.

[back to README](README.md)
